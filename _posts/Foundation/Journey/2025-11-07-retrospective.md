---
layout: post
toc: True
breadcrumb: True
title: AP CSP Retrospective
permalink: /journey/retrospective
author: Sathwik Kintada
---


# AP Computer Science Retrospective

## Reflecting on Growth
At the start of the year, I was just getting comfortable with Python and basic programming concepts. Now, after completing multiple sprints and projects, I feel much more confident in my ability to solve problems programmatically, understand debugging, and apply computer science principles in practical contexts like cybersecurity simulations and data analysis. My logical thinking and coding fluency have both improved significantly.

---

## Sprint Reviews

### Sprint 1: Tools & Setup
- Learned to use VS Code, GitHub, and Python/Jupyter notebooks efficiently.  
- Understood debugging techniques and how to read error messages.  
- Applied these tools while working on small coding exercises and foundational projects.  

### Sprint 2: Fundamentals of JavaScript/Python
- Built confidence in core concepts like loops, conditionals, functions, and data structures.  
- Practiced problem-solving with arrays/lists, dictionaries, and string manipulations.  
- Learned the importance of writing clean, readable code.  

### Sprint 3:  Digital Famine
- Learned about databases, SQL, SQL injection prevention, and cryptographic hashing (SHA-256).  
- Gained hands-on experience with interactive coding and applying concepts in real-world scenarios.  

---

## N@tM Feedback: Vault Quiz

During the N@tM session, I focused on completing the Vault Quiz. Some observations from my experience:

- The quiz was well-structured, with questions progressively covering the three missions: database design, SQL injection, and hashing.  
- The retry mechanic was helpful because it allowed me to attempt a question again with a hint without penalizing my score.  
- I noticed that shuffling the options for each question required careful reading; it reinforced understanding rather than memorization.  
- Linking each question back to the lesson materials made it easier to review concepts when I got a question wrong.  
- The visual progress bar and feedback system helped me track how far I was and which areas needed extra attention.  

Overall, working through the Vault Quiz highlighted which areas I understand well and which topics (like hashing details or foreign key relationships) I need to revisit in lessons.


---

## Next Steps on Projects
- Extend the Digital Famine project with additional missions or alternative attack scenarios.  
- Add analytics to track quiz performance and highlight student misconceptions in real time.  
- Explore integrating simple AI modules for dynamic question generation or feedback.

---

## Next Learning Goals in Computer Science
- Learn object-oriented programming in Python and Java.  
- Understand algorithms and data structures in depth.  
- Start exploring AI/ML applications for real-world problems  

---

## Analytics Review


---

# AP CSP MCQ Corrections

This section reviews all the questions I got wrong on the AP Computer Science Principles multiple-choice section. Each question includes the full text, all answer options, my selected answer, and reasoning.

---

## Question 36: Result of computer performing 2 ÷ 3
<details>
<summary><strong>View Explanation</strong></summary>

**Question:** What is the result when a computer performs `2 ÷ 3` using integer division?

**Options:**  
A. 0  
B. 0.666…  
C. 2  
D. 0 (integer division)  

**Your answer:** D  
**Correct answer:** B  

**Reasoning:** Integer division truncates the decimal, but in the context of AP CSP, this problem uses normal division which yields `0.666…`. Be careful to note whether integer or floating-point division is implied.
</details>

---

## Question 38: Frequent customers of a snack bar
<details>
<summary><strong>View Explanation</strong></summary>

**Question:** Which algorithm correctly identifies frequent customers of a snack bar?

**Options:**  
A. Count customers with purchases > threshold  
B. Iterate through purchases and count frequency  
C. Sort purchases by customer ID  
D. Use a binary search  

**Your answer:** B  
**Correct answer:** C  

**Reasoning:** Sorting first makes it easier to group purchases by customer ID, allowing frequency counts to be computed efficiently.
</details>

---

## Question 39: Internet Open Standards and Protocols
<details>
<summary><strong>View Explanation</strong></summary>

**Question:** Which of the following explains a benefit of using open standards and protocols for Internet communication?

**Options:**  
A. Allow devices from different manufacturers to communicate  
B. Eliminate Internet message latency  
C. Allow users to freely share noncommercial material  
D. Prevent software with errors from being released  

**Your answer:** (blank)  
**Correct answer:** A  

**Reasoning:** Open standards enable interoperability between devices and platforms built by different developers.
</details>

---

## Question 42: Increasing bit representation for Internet protocol
<details>
<summary><strong>View Explanation</strong></summary>

**Question:** Why would a network increase the bit representation for addresses in an Internet protocol?

**Options:**  
A. To speed up packet transmission  
B. To simplify routing  
C. To allow more unique addresses  
D. To reduce memory usage  

**Your answer:** C  
**Correct answer:** D  

**Reasoning:** Increasing the bit length of an address (e.g., IPv4 → IPv6) allows for a larger number of unique IP addresses.
</details>

---

## Question 43: Runtime of algorithm for online retailer
<details>
<summary><strong>View Explanation</strong></summary>

**Question:** Which statement correctly describes the runtime of an algorithm used by an online retailer?

**Options:**  
A. O(n)  
B. O(log n)  
C. O(n²)  
D. O(1)  

**Your answer:** B  
**Correct answer:** A  

**Reasoning:** If the algorithm processes each order or customer once, the runtime is linear — O(n).
</details>

---

## Question 45: NAND logic gate
<details>
<summary><strong>View Explanation</strong></summary>

**Question:** What is the output of a NAND gate when both inputs are 1?

**Options:**  
A. 1  
B. 0  
C. Depends on previous input  
D. 1 if clocked  

**Your answer:** A  
**Correct answer:** B  

**Reasoning:** NAND outputs 0 only when all inputs are 1; otherwise, output is 1.
</details>

---

## Question 46: Infinite loops and undecidable problems
<details>
<summary><strong>View Explanation</strong></summary>

**Question:** Can we create an algorithm to determine if any program will go into an infinite loop?

**Options:**  
A. Yes, using low-level languages  
B. Yes, using multiple CPUs  
C. Yes, but may not run in reasonable time  
D. No, it's undecidable  

**Your answer:** (blank)  
**Correct answer:** D  

**Reasoning:** The Halting Problem is undecidable — there is no algorithm that can determine for every possible program whether it will halt.
</details>

---

## Question 47: Encrypting and decrypting using public key cryptography
<details>
<summary><strong>View Explanation</strong></summary>

**Question:** Which statement best describes public key cryptography?

**Options:**  
A. Uses the same key to encrypt and decrypt  
B. Encrypts with a password  
C. Encrypts messages for offline storage only  
D. Uses a pair of keys for secure communication  

**Your answer:** B  
**Correct answer:** D  

**Reasoning:** Public key cryptography relies on two keys — one public for encryption and one private for decryption.
</details>

---

## Question 51: Examples of symmetric encryption
<details>
<summary><strong>View Explanation</strong></summary>

**Question:** Which of the following is an example of symmetric encryption?

**Options:**  
A. Two codes for a locked box (different actions)  
B. Mapping letters to symbols using a shared secret key  
C. Hiding messages under a rock  
D. Locker message with private combination  

**Your answer:** (blank)  
**Correct answer:** B  

**Reasoning:** Symmetric encryption uses the same key for both encryption and decryption.
</details>

---

## Question 55: Results of the KeepPlaying procedure
<details>
<summary><strong>View Explanation</strong></summary>

**Question:** What is the result of calling the `KeepPlaying` procedure?

**Options:**  
A. Ends the game immediately  
B. Loops until a condition is met  
C. Throws an error  
D. Randomly continues  

**Your answer:** A  
**Correct answer:** D  

**Reasoning:** The loop continues until a condition or random event determines otherwise.
</details>

---

## Question 58: Defining Internet-enabled crowdsourcing
<details>
<summary><strong>View Explanation</strong></summary>

**Question:** What is Internet-enabled crowdsourcing?

**Options:**  
A. Data stored in one database  
B. Automating tasks without humans  
C. Using the Internet to gather input from many people  
D. A type of encryption  

**Your answer:** (blank)  
**Correct answer:** C  

**Reasoning:** Crowdsourcing uses contributions from a large group of people online to collect information or ideas.
</details>

---

## Question 60: Managing complexity with abstraction
<details>
<summary><strong>View Explanation</strong></summary>

**Question:** Which is a benefit of using abstraction in programming?

**Options:**  
A. It speeds up code execution  
B. Reduces code readability  
C. Hides implementation details to simplify understanding  
D. Prevents runtime errors  

**Your answer:** (blank)  
**Correct answer:** C  

**Reasoning:** Abstraction simplifies understanding and management of complex programs by hiding unnecessary details.
</details>

---

## Question 62: Compare online encyclopedia with paper encyclopedia
<details>
<summary><strong>View Explanation</strong></summary>

**Question:** Which of the following statements is true when comparing online and paper encyclopedias?

**Options:**  
A. Online always more accurate  
B. Paper always cheaper  
C. Online easier to update; paper is fixed  
D. Online allows hyperlinks and multimedia  

**Your answer:** C & D  
**Correct answer:** B & D  

**Reasoning:** Online encyclopedias support multimedia and hyperlinks; paper versions have fixed content and can be less expensive.
</details>

---

## Question 63: Use of isPrime procedure
<details>
<summary><strong>View Explanation</strong></summary>

**Question:** If `isPrime` returns 1 for numbers 1–10, which numbers are identified as prime?

**Options:**  
1. 2  
2. 3  
3. 4  
4. 5  
5. 6  
6. 7  
7. 8  
8. 9  
9. 10  

**Your answer:** 4  
**Correct answer:** 4 & 9  

**Reasoning:** The procedure incorrectly classifies 4 and 9 as prime, indicating a logic error in how divisibility is checked.
</details>

---

### ✅ Summary Table

| Question | Your Answer | Correct Answer | Topic |
|-----------|--------------|----------------|--------|
| 36 | D | B | Math/Operators |
| 38 | B | C | Algorithms |
| 39 | – | A | Internet Protocols |
| 42 | C | D | Networking |
| 43 | B | A | Algorithm Efficiency |
| 45 | A | B | Logic Gates |
| 46 | – | D | Undecidable Problems |
| 47 | B | D | Cryptography |
| 51 | – | B | Encryption |
| 55 | A | D | Procedure Behavior |
| 58 | – | C | Crowdsourcing |
| 60 | – | C | Abstraction |
| 62 | C&D | B&D | Data Representation |
| 63 | 4 | 4&9 | Algorithm Logic |


---

## Question 43: Runtime of algorithm for online retailer
<d


## Something Cool I'd Like to Share
- During Digital Famine, I implemented shuffling of questions and answers with hints for incorrect attempts, which made the quiz feel interactive and adaptive.  
- Learned how gamification can improve learning outcomes in computer science education.

---

**End of Retrospective**
