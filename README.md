# NETWORKWALKS--CLARK-B084-WK3-CYBERSECURITY
# NetworkWalks Lab: PDF Hash Extraction & Dictionary Password Cracking

Practical cybersecurity lab exercise focused on extracting `$pdf$` hashes from password-protected PDF files, running dictionary attacks using web-based lab tools and **Johnny** (GUI for John the Ripper), and analyzing password strength against common wordlists.

> **Disclaimer:** Performed strictly on test/lab files in an authorized educational environment for learning defensive and offensive security concepts.

---

## Overview & Objectives

In this lab, I explored how password-protected PDFs expose cryptographic hash structures that can be audited via dictionary attacks:
- Extract crackable `$pdf$` hashes from encrypted PDF documents.
- Run dictionary attacks against extracted hashes using wordlists.
- Compare browser-based lab tools (**NetworkWalks**) with local desktop tooling (**Johnny** / John the Ripper).
- Observe how predictable or weak passwords are recovered quickly during dictionary matching.

---

## Tools & Environment

- **NetworkWalks Hash Calculator:** Used to extract crackable hashes from password-protected PDFs.
- **NetworkWalks Password Cracker (Dictionary Attack Lab):** Used to test a `$pdf$` hash against a built-in wordlist (100 passwords) and observe real-time candidate matching.
- **Johnny (John the Ripper):** Used to load PDF hash files/formats and crack test PDF passwords locally (`100% (3/3: 3 cracked, 0 left)`).
- **Sample Test Files:** Encrypted PDFs (`My Locked PDF1.pdf`, `My Locked PDF2.pdf`, `My Locked PDF3.pdf`) and exported hash/output files.

---

## Step-by-Step Workflow

### 1. PDF Hash Extraction
- Prepared password-protected test PDF files (`My Locked PDF1.pdf`, `My Locked PDF2.pdf`, `My Locked PDF3.pdf`).
- Used the PDF hash extraction workflow to obtain `$pdf$...` hash strings suitable for password auditing tools.

### 2. Dictionary Attack via NetworkWalks
- Pasted the extracted `$pdf$` hash for `My Locked PDF2.pdf` into the **NetworkWalks Password Cracker** lab.
- Ran a dictionary attack using the built-in 100-word list, monitoring candidate attempts until a match was found (`password1` matched at attempt 91/100).

### 3. Local Cracking & Verification with Johnny
- Loaded the PDF hashes into **Johnny** and ran password cracking across the test entries.
- Verified cracked results across all 3 PDFs (`good-luck`, `password1`, and `1qaz2wsx`), confirming 100% completion (`3/3 cracked`).

---

## Key Takeaways

- **Weak & common passwords fail fast:** Dictionary and pattern-based passwords (such as common words, keyboard walks, or default-style strings) are quickly identified once a hash is extracted.
- **Hash extraction is only half the story:** Understanding how hashes are formatted and tested helps security practitioners choose stronger passphrases and harden access controls.
- **Tooling variety matters:** Testing across both interactive web labs and local John the Ripper/Johnny workflows reinforces how different interfaces report progress, formats, and results.

---

## Screenshots / Artifacts Included

- Hash extraction & hash calculator interfaces
- Encrypted PDF files and extracted `.txt` hash files
- NetworkWalks dictionary cracker setup and cracked password output (`password1`)
- Johnny password cracking table showing cracked PDF entries (`good-luck`, `password1`, `1qaz2wsx`)
