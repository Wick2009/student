---
# YML definition of metadata for file, used by GH pages
layout: base
title: Background with Object
description: Use JavaScript to have an in motion background.
# these are the locations of images in this Game
sprite: images/platformer/sprites/AlienSprite.png
background: images/platformer/backgrounds/alien_planet1.jpg
permalink: background
---

<!-- HTML for where Game is stored -->
<canvas id="world"></canvas>

<!-- Script logic for the Game -->
<script>
  // Get the canvas element from the HTML and set up drawing context
  const canvas = document.getElementById("world");
  const ctx = canvas.getContext('2d');
  // Create image objects for background and sprite
  const backgroundImg = new Image();
  const spriteImg = new Image();
  // Set image sources using metadata from YML at the top of the file
  backgroundImg.src = '{{page.background}}';
  spriteImg.src = '{{page.sprite}}';

  // Track when both images are loaded before starting the game
  let imagesLoaded = 0;
  backgroundImg.onload = function() {
    imagesLoaded++;
    startGameWorld();
  };
  spriteImg.onload = function() {
    imagesLoaded++;
    startGameWorld();
  };

  // This function starts the game only after both images are loaded
  function startGameWorld() {
    if (imagesLoaded < 2) return;

    // GameObject is a base class for anything drawn on the canvas
    class GameObject {
      constructor(image, width, height, x = 0, y = 0, speedRatio = 0) {
        this.image = image;
        this.width = width;
        this.height = height;
        this.x = x;
        this.y = y;
        this.speedRatio = speedRatio;
        // Speed is based on a ratio and the global game speed
        this.speed = GameWorld.gameSpeed * this.speedRatio;
      }
      // Update position or state (to be customized by subclasses)
      update() {}
      // Draw the object on the canvas
      draw(ctx) {
        ctx.drawImage(this.image, this.x, this.y, this.width, this.height);
      }
    }

    // Background class scrolls the background image to create motion
    class Background extends GameObject {
      constructor(image, gameWorld) {
        // Fill entire canvas
        super(image, gameWorld.width, gameWorld.height, 0, 0, 0.1);
      }
      update() {
        // Move background to the left and wrap around for infinite scroll
        this.x = (this.x - this.speed) % this.width;
      }
      draw(ctx) {
        ctx.drawImage(this.image, this.x, this.y, this.width, this.height);
        ctx.drawImage(this.image, this.x + this.width, this.y, this.width, this.height);
      }
    }

    // Player class represents the moving sprite (UFO)
    class Player extends GameObject {
      constructor(image, gameWorld) {
        const width = image.naturalWidth / 2;
        const height = image.naturalHeight / 2;
        const x = (gameWorld.width - width) / 2;
        const y = (gameWorld.height - height) / 2;
        super(image, width, height, x, y);
        this.baseY = y;
        this.frame = 0;
      }
      update() {
        // Make the sprite float up and down using a sine wave
        this.y = this.baseY + Math.sin(this.frame * 0.05) * 20;
        this.frame++;
      }
    }

    /* Game World is master class/object for the entire game
    * the game loop is inside 
    */
    // GameWorld manages the canvas, game objects, and the main loop
    class GameWorld {
      static gameSpeed = 500;
      // images enter the world
      constructor(backgroundImg, spriteImg) {
        this.canvas = document.getElementById("world");
        this.ctx = this.canvas.getContext('2d');
        this.width = window.innerWidth;
        this.height = window.innerHeight;
        // Set canvas size to fill the window
        this.canvas.width = this.width;
        this.canvas.height = this.height;
        this.canvas.style.width = `${this.width}px`;
        this.canvas.style.height = `${this.height}px`;
        this.canvas.style.position = 'absolute';
        this.canvas.style.left = `0px`;
        this.canvas.style.top = `${(window.innerHeight - this.height) / 2}px`;

        // Game objects are created 
        // Add background and player to the game
        this.objects = [
         new Background(backgroundImg, this),
         new Player(spriteImg, this)
        ];
      }
      // This keeps game alive and runing
      // Main game loop: updates and draws all objects, then repeats
      gameLoop() {
        this.ctx.clearRect(0, 0, this.width, this.height);
        for (const obj of this.objects) {
          obj.update();
          obj.draw(this.ctx);
        }
        requestAnimationFrame(this.gameLoop.bind(this));
      }
      // Start the game loop
      start() {
        this.gameLoop();
      }
    }

    // Create the game world and start the animation
    const world = new GameWorld(backgroundImg, spriteImg);

    // starts the game world
    world.start();
  }
