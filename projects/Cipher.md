---
layout: project
type: project
image: img/Cipher/cipher.PNG
title: "Caesar Cipher and Vigenere cipher"
date: 2021
published: true
labels:
  - Cipher
  - Java
---

<div align="center">
  <img width="350px" height="200px" src="../img/Cipher/ccipherEncode.PNG" class="img-thumbnail" >
  <img width="300px" height="200px" src="../img/Cipher/ccipherDecrypt.PNG" class="img-thumbnail" >
 
</div>

This is an encryption and decryption program. There are two types of cipher in this program. The first one is Caesar cipher. Which is a simple method of encoding messages. To encrypt you just need to set a password(an integer and represent the number of slots shift to the right). For example, you encrypt "a" with password "3" and then the encoded result is "d". To decrypt would need to enter the encrypted message with the password(this time shift left). Enter "d" with password "3" and you will get the original message you have entered which in this case is "a". To encrypt you don't have to shift right. You can also shift left but just have to make the decryption shift the opposite way of encryption.



<div align="center">
  <img width="300px" height="250px" src="../img/Cipher/vcipherEncode.PNG" class="img-thumbnail" >
  <img width="300px" height="250px" src="../img/Cipher/vcipherDecrypt.PNG" class="img-thumbnail" >
 
</div>
The second type of cipher is the Vigenere cipher. Which is another shift encoder. To encrypt you need to add the value(position of letter in alphabet -1 because Computer science is 0 based) of the letter you want to encode with the letter of the key you have set up. For example, encrypt "abc" with the key "key". Process: (a=0, b=1, c=2, k=10, e=4, y= 24) first letter "a": 0+10=10 which becomes "k", the second letter"b": 1+4=5 which becomes "f", last letter "c" = 2+24=26 but it is equal 26 so you need to take the modulo of 26 (26%26) which is 0 and become "a". 
Result: "kfa" For decryption, it is the opposite of encryption. You subtract the key value from the encrypted letter value.



This program was an assignment for AP computer science A. This was the first time I was introduced to some kind of encryption and decryption. It took me a long time to finish that assignment. It is not the concept that is hard. It is having it bit of trouble with the scanner skipping lines. So the program could not receive the input needed to perform encryption and decryption.




Source: <a href="https://replit.com/@yc2003/Final-cipher1"><i class="large github icon "></i>Link to my source code</a>
