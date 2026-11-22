# Network Walks Internship – Week 3

**Intern Name:** Avinash Chilamathuru  
**Internship:** Network Walks  
**Batch ID:** B084  
**Week:** 3  
**Essential Module 1:** W3-PM1 – Password Cracking with JTR  
**Essential Module 2:** W3-PM2 – Password Cracking with Network Walks Tools

---

## 1. Introduction

During Week 3 of the Network Walks Cybersecurity Internship, I worked on password auditing and recovery techniques using John the Ripper and Network Walks' online password-cracking tools.

The main objective of these practical exercises was to understand how password-protected PDF files store password hashes and how password-auditing tools use wordlists to test possible passwords.

I completed both essential modules using the internship-provided PDF samples and documented the practical process with screenshots.

## 2. Environment and Tools Used

**Operating System:** Kali Linux  
**Additional Platform:** Web Browser

**Tools Used:**
- John the Ripper (JTR)
- pdf2john
- Kali Linux Terminal
- Network Walks Hash Calculator
- Network Walks Password Cracker
- Web Browser

---

# 3. W3-PM1 – Password Cracking with John the Ripper (JTR)

## Objective

The objective of this practical was to understand how John the Ripper can be used to audit the password protection of PDF files by extracting their password hashes and testing possible passwords.

## Tools Used

- Kali Linux
- John the Ripper
- pdf2john
- Terminal

## Practical Work

### 3.1 Locating the Encrypted PDF File

First, I opened the Downloads directory in Kali Linux and located the internship-provided encrypted PDF sample.

I checked the available files and selected the PDF required for the password-auditing exercise.

**Command Used:**

```bash
cd ~/Downloads
ls
```

### 3.2 Extracting the PDF Password Hash

After locating the encrypted PDF, I used the `pdf2john` utility to extract its password hash.

The extracted hash was redirected into a text file named `hash1.txt`. This file was used as input for John the Ripper.

**Command Used:**

```bash
pdf2john "My Locked PDF1.pdf" > ~/hash1.txt
```

The extracted hash contains information required by the password-auditing tool to perform the recovery process.

### 3.3 Running John the Ripper

After extracting the hash, I executed John the Ripper by providing the generated hash file.

**Command Used:**

```bash
john ~/hash1.txt
```

John the Ripper loaded the PDF password hash and started testing possible password combinations using its available password candidates and wordlist.

<img width="1600" height="724" alt="WhatsApp Image 2026-11-22 at 4 22 18 PM (1)" src="https://github.com/user-attachments/assets/02c04a39-0178-422e-aba4-a82236f3668c" />


### 3.4 Recovering the Password

After processing the available password candidates, John the Ripper successfully recovered the password for the sample PDF.

The terminal displayed the recovered password along with the corresponding PDF filename.

I also tested the process with another provided PDF sample and observed a successful password recovery.

<img width="1600" height="415" alt="WhatsApp Image 2026-11-22 at 4 22 19 PM (2)" src="https://github.com/user-attachments/assets/3cb26dee-02d7-4e53-99f9-a98671b55dc1" />


### 3.5 Verifying the Recovered Password

After obtaining the recovered password, I used it to open the encrypted PDF and verify that the file could be accessed.

The successful recovery confirmed that the password-auditing process worked for the provided training samples.

### 3.6 Capturing the Internship Flags

During the practical exercise, I also captured the completion flags displayed by the internship challenge.

These screenshots serve as additional evidence of completing the assigned JTR activities.

<img width="1600" height="649" alt="WhatsApp Image 2026-11-22 at 4 22 18 PM (2)" src="https://github.com/user-attachments/assets/5d6e81cc-f7e6-4c65-810e-8401159e3367" />


<img width="1600" height="719" alt="WhatsApp Image 2026-11-22 at 4 22 19 PM (3)" src="https://github.com/user-attachments/assets/34b87419-c00e-4479-a85a-31681e133f11" />


<img width="1600" height="659" alt="WhatsApp Image 2026-11-22 at 4 22 18 PM" src="https://github.com/user-attachments/assets/92305804-0a57-4083-b56b-5d11f7117011" />



## PM1 – Learning Outcome

By completing this practical, I learned:

- How encrypted PDF files can be processed for password auditing.
- How to extract PDF password hashes using `pdf2john`.
- How to provide extracted hashes to John the Ripper.
- How wordlists help in testing possible passwords.
- How to verify password recovery by opening an encrypted PDF.
- The importance of strong and unpredictable passwords.

---

# 4. W3-PM2 – Password Cracking with Network Walks Tools

## Objective

The objective of this practical was to understand how Network Walks' Hash Calculator and Password Cracker tools can be used to extract a PDF password hash and perform a password-recovery exercise.

## Tools Used

- Network Walks Hash Calculator
- Network Walks Password Cracker
- Web Browser
- Internship-provided encrypted PDF sample

## Practical Work

### 4.1 Opening the Network Walks Hash Calculator

First, I opened the Network Walks Hash Calculator through the official internship-provided tool page.

I selected the PDF option and uploaded the encrypted PDF sample provided for the PM2 exercise.

The tool processed the file locally in the browser and generated a password hash.

### 4.2 Extracting the PDF Hash

After selecting the PDF, the Hash Calculator identified that the document was encrypted and displayed the extracted PDF hash.

I copied the complete hash generated by the tool for the next step.

<img width="1600" height="735" alt="WhatsApp Image 2026-11-22 at 4 22 17 PM" src="https://github.com/user-attachments/assets/023701eb-a694-4f0e-a1af-0ef1365b0f93" />


### 4.3 Using the Network Walks Password Cracker

After extracting the hash, I opened the Network Walks Password Cracker.

I pasted the copied PDF hash into the provided input area and started the password-recovery process.

The tool began testing possible password candidates and displayed the progress of the process.

### 4.4 Successful Password Recovery

After the password-testing process was completed, the tool displayed a successful password match.

I used the recovered password to unlock the internship-provided PDF sample and verify the result.

<img width="1600" height="724" alt="WhatsApp Image 2026-11-22 at 4 22 17 PM (1)" src="https://github.com/user-attachments/assets/c4d9d24d-5331-47aa-afa0-02c032b994cb" />


### 4.5 Capturing the Completion Evidence

After successfully completing the exercise, I captured the challenge completion screen as evidence.

<img width="1600" height="709" alt="WhatsApp Image 2026-11-22 at 4 22 19 PM (1)" src="https://github.com/user-attachments/assets/a485b9ae-951c-43c5-8841-7b482d45d700" />


## PM2 – Learning Outcome

Through this practical, I learned:

- How to use the Network Walks Hash Calculator.
- How to identify password-protected PDF files.
- How PDF password hashes are generated and extracted.
- How to submit an extracted hash to a password-cracking tool.
- How password candidates are tested during recovery.
- How to verify a recovered password by opening the protected document.

---

# 5. Challenges and Troubleshooting

During the practical exercises, I explored different approaches to password recovery and understood the importance of following each step carefully.

Some important points I learned during the process were:

1. The PDF hash must be extracted correctly before it can be processed by John the Ripper.
2. The complete hash must be copied without missing or modifying any characters.
3. The password recovery process depends on the available password candidates and wordlists.
4. The recovered password must be verified by opening the corresponding encrypted PDF.
5. Different PDF samples can produce different password hashes and recovery results.

These practical activities helped me become more familiar with Linux terminal commands and password-auditing workflows.

---

# 6. Ethical Considerations

All practical activities were performed using the PDF samples provided for the Network Walks internship.

The exercises were carried out strictly for educational purposes to understand password security and auditing techniques.

No personal documents, third-party files or unauthorized accounts were targeted during these activities.

---

# 7. Conclusion

In Week 3, I gained practical experience with two different approaches to PDF password auditing: John the Ripper in Kali Linux and the Network Walks online password-cracking tools.

I learned how to extract password hashes, process them using password-auditing tools, test possible passwords and verify successful recovery.

Working with both command-line and browser-based tools helped me understand the basic workflow behind password auditing and the importance of using strong passwords to protect sensitive information.

Overall, these exercises improved my familiarity with Kali Linux, password hashes, wordlists and practical cybersecurity tools.

---

**End of Week 3 Practical Work**
