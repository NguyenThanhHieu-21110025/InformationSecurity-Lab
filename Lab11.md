# 21110025 - Nguyễn Thành Hiếu
# Lab#11 Encrypt Large Message


## Lab Environment
### OpenSSL

*Setup OpenSSL:*

<img width="726" alt="lab11-1.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-1.jpg">

<img width="726" alt="lab11-2.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-2.jpg">

<img width="726" alt="lab11-3.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-3.jpg">


## Task 1 : Encrypt and Decrypt Text file
*Encrypt:*

<img width="726" alt="lab11-4.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-4.jpg">

*Decrypt:*

<img width="726" alt="lab11-5.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-5.jpg">


## Task 2: Encryption Mode – ECB vs. CBC

<img width="726" alt="lab11-14.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-14.jpg">


*Key AES-256: 2e58e1796105f695722a2262895bdd18b2c3ebd65c863c457895fe768bbfa886*

<img width="726" alt="lab11-6.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-6.jpg">


*16-byte (hex) initialization vector: 0b27f7cbb5a1e1163116d4064e479bf2*

<img width="726" alt="lab11-7.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-7.jpg">

*Replace the header of the encrypted picture with that from the original picture by using Linux dd command.*

<img width="726" alt="lab11-8.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-8.jpg">

<img width="726" alt="lab11-9.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-9.jpg">


*Encrypt body.bin with AES-256-CBC*

<img width="726" alt="lab11-10.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-10.jpg">

*Combine header.bin and encrypted_body.bin to create partially_encrypted.bmp:*


<img width="726" alt="lab11-11.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-11.jpg">

*Encryption file:*

<img width="726" alt="lab11-12.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-12.jpg">

*Decrypt partially_encrypted.bmp to restore body.bin*

<img width="726" alt="lab11-13.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-13.jpg">

*origin.bmp*

<img width="726" alt="lab11-15.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-15.jpg">

*Here is the image “whale.bmp” after encryption using ECB mode:*

<img width="726" alt="lab11-16.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-16.jpg">

<img width="726" alt="lab11-17.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-17.jpg">

*Each block is encrypted with the same key and an independent algorithm, so the encrypted file still retains some of its original structure, making it less secure for data encryption.*

*Here are the results when using CBC mode:*

<img width="726" alt="lab11-18.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-18.jpg">


<img width="726" alt="lab11-19.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-19.jpg">


*After encryption, the image is completely distorted. This method is safer because it performs XOR before encrypting the blocks.*


## Task 3 : Encryption Mode – Corrupted Cipher Text
*Create a text file of at least 64 bytes*

<img width="726" alt="lab11-20.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-20.jpg">

*Encrypt text files with AES-256*
*ECB*

<img width="726" alt="lab11-21.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-21.jpg">

*CBC*

<img width="726" alt="lab11-22.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-22.jpg">

*CFB*

<img width="726" alt="lab11-23.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-23.jpg">

*OFB*

<img width="726" alt="lab11-24.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-24.jpg">

*Corrupting a byte in an encrypted file*

*ECB*

<img width="726" alt="lab11-25.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-25.jpg">

*CBC*

<img width="726" alt="lab11-26.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-26.jpg">

*CFB*

<img width="726" alt="lab11-27.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-27.jpg">

*OFB*

<img width="726" alt="lab11-28.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-28.jpg">

*Decrypt corrupted encrypted files*

<img width="726" alt="lab11-29.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-29.jpg">

<img width="726" alt="lab11-30.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-30.jpg">

*ECB*

<img width="726" alt="lab11-31.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-31.jpg">

<img width="726" alt="lab11-32.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-32.jpg">


*CBC*

<img width="726" alt="lab11-33.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-33.jpg">

<img width="726" alt="lab11-34.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-34.jpg">


*CFB*

<img width="726" alt="lab11-35.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-35.jpg">

<img width="726" alt="lab11-36.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-36.jpg">


*OFB*

<img width="726" alt="lab11-37.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-37.jpg">

<img width="726" alt="lab11-38.jpg" src="https://github.com/NguyenThanhHieu-21110025/InformationSecurity-Lab/blob/main/images/lab11-38.jpg">

### Conclusion on the Impact of Errors in Different Encryption Modes

1. **ECB (Electronic Code Book)**:
   - An error in a single byte only affects that byte during decryption.
   - Without error propagation, the ECB mode is prone to revealing patterns in the original data.

2. **CBC (Cipher Block Chaining)**:
   - An error in a single byte affects the current block and the subsequent block during decryption.
   - Error propagation helps obscure the pattern of the original data better.

3. **CFB (Cipher Feedback)**:
   - An error in a single byte affects the current byte and the subsequent byte during decryption.
   - Error propagation is similar to CBC but operates on individual bytes.

4. **OFB (Output Feedback)**:
   - An error in a single byte only affects that byte during decryption.
   - Without error propagation, similar to ECB, but safer in terms of hiding the pattern of the original data.

### Summary:
- **ECB** is not suitable for data with repeating patterns due to its susceptibility to pattern leakage.
- **CBC** and **CFB** propagate errors, which helps hide patterns but can corrupt more data if errors occur.
- **OFB** protects data patterns better than ECB without error propagation, affecting only the corrupted byte.























