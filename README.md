<h1>Decrypt an encrypted message</h1>


<h2>Description</h2>

Previously, you learned about cryptography and how encryption and decryption can be used to secure information online. You were also introduced to the Caesar cipher, one of the earliest cryptographic algorithms used to protect people’s privacy.

As a security analyst, it’s important that you understand the role of encryption to secure data online and that you’re familiar with the right security controls to do so.

In this lab activity, you’ll be guided through some basic cryptographic activities using Linux commands to decrypt files and reveal hidden messages.

<h2>Environments Used </h2>

- <b>Linux</b>

<h2>Scenario:</h2>

In this scenario, all of the files in your home directory have been encrypted. You’ll need to use Linux commands to break the Caesar cipher and decrypt the files so that you can read the hidden messages they contain.

Here’s how you’ll do this task: 

- First, you’ll explore the contents of the home directory and read the contents of a file.

- Next, you’ll find a hidden file and decrypt the Caesar cipher it contains.

- Finally, you’ll decrypt the encrypted data file to recover your data and reveal the hidden message.

<h2>Tutorial walk-through:</h2>

<h3>Task 1. Read the contents of a file</h3>

The lab starts in your home directory, /home/analyst, as the current working directory.

In this task, you need to explore the contents of your home directory and read the contents of a file to get further instructions.

1. Use the ls command to list the files in the current working directory.
   
Two files, Q1.encrypted and README.txt, and a subdirectory, caesar, are listed:

<img src="" height="80%" width="80%"/>

The README.txt file contains an important message with instructions you need to follow.

2. Use the cat command to list the contents of the README.txt file.
   
The message in the README.txt file advises that the caesar subdirectory contains a hidden file.

In the next task, you’ll need to find the hidden file and solve the Caesar cipher that protects it. The file contains instructions on how to recover your data.







<h2>Conclusion</h2>

You now have practical experience in using basic Linux Bash shell commands to

- list hidden files
- decrypt a Caesar cipher
- decrypt an encrypted file

  
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
