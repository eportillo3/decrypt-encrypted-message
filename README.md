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

<img src="https://i.imgur.com/7IGbFLK.png" height="80%" width="80%"/>

The README.txt file contains an important message with instructions you need to follow.

2. Use the cat command to list the contents of the README.txt file.
   
The message in the README.txt file advises that the caesar subdirectory contains a hidden file.

<img src="https://i.imgur.com/kbd8zNn.png" height="80%" width="80%"/>

In the next task, you’ll need to find the hidden file and solve the Caesar cipher that protects it. The file contains instructions on how to recover your data.

<h3>Task 2. Find a hidden file</h3>

In this task, you need to find a hidden file in your home directory and decrypt the Caesar cipher it contains. This task will enable you to complete the next task.

1. First, use the cd command to change to the caesar subdirectory of your home directory:

2. Use the ls -a command to list all files, including hidden files, in your home directory.
   
This will display the following output:

<img src="https://i.imgur.com/4PrZpfi.png" height="80%" width="80%"/>

Hidden files in Linux can be identified by their name starting with a period (.).

3. Use the cat command to list the contents of the .leftShift3 file.

<img src="https://i.imgur.com/e2U5toR.png" height="80%" width="80%"/>


The message in the .leftShift3 file appears to be scrambled. This is because the data has been encrypted using a Caesar cipher. This cipher can be solved by shifting each alphabet character to the left or right by a fixed number of spaces. In this example, the shift is three letters to the left. Thus "d" stands for "a", and "e" stands for "b".

4. You can decrypt the Caesar cipher in the .leftshift3 file by using the following command:

<img src="https://i.imgur.com/r0tCjg7.png" height="80%" width="80%"/>

<img src="https://i.imgur.com/MJ0UEpg.png" height="80%" width="80%"/>


In this case, the command tr "d-za-cD-ZA-C" "a-zA-Z" translates all the lowercase and uppercase letters in the alphabet back to their original position. The first character set, indicated by "d-za-cD-ZA-C", is translated to the second character set, which is "a-zA-Z".

<img src="https://i.imgur.com/iSyMKaq.png" height="80%" width="80%"/>

5. Now, return to your home directory before completing the next task.

<h3>Task 3. Decrypt a file</h3>

Now that you have solved the Caesar cipher, in this task you need to use the command revealed in .leftshift3 to decrypt a file and recover your data so you can read the message it contains.

1. Use the exact command revealed in the previous task to decrypt the encrypted file:

openssl aes-256-cbc -pbkdf2 -a -d -in Q1.encrypted -out Q1.recovered -k ettubrute

Although you don't need to memorize this command, to help you better understand the syntax used, let's break it down.

In this instance, the openssl command reverses the encryption of the file with a secure symmetric cipher, as indicated by AES-256-CBC. The -pbkdf2 option is used to add extra security to the key, and -a indicates the desired encoding for the output. The -d indicates decrypting, while -in specifies the input file and -out specifies the output file. The -k specifies the password, which in this example is ettubrute.

2. Use the ls command to list the contents of your current working directory again.

<img src="https://i.imgur.com/oz7ZtgJ.png" height="80%" width="80%"/>

The new file Q1.recovered in the directory listing is the decrypted file and contains a message.

3. Use the cat command to list the contents of the Q1.recovered file.

<img src="https://i.imgur.com/rJV1Cgq.png" height="80%" width="80%"/>


<h2>Conclusion</h2>

Great work! You now have practical experience in using basic Linux Bash shell commands to

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
