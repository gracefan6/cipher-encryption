# Cipher and Encryptions

This project allows encryption and decryption with caesar ciphers, random substitution ciphers, vigenere ciphers, and RSA encryption. This program was written as a part of CS 2112 (fall 2020) at Cornell University. Due to academic intergrity concerns, I am unable to publicly publish the full repository of thie project. I, instead, posted a jar file of the project. To view the full contents of the code, please email fan123.me@gmail.com for requests. 

# How to run the program

The user should be able to provide commands of the following form via the console:
```
java -jar <YOUR_JAR> <CIPHER_TYPE> <CIPHER_FUNCTION> <OUTPUT_OPTIONS>
```
## Cipher type
The user can specify the type of ciphers using the following flags: 
- ```--caesar <shift_param>:``` Create a new Caesar cipher with the given integer shift pa- rameter.
- ```--random:``` Create a new monoalphabetic substitution cipher with a randomly chosen permutation of the alphabet.
- ```--vigenere <key>:``` Create a new Vigenere cipher with the given keyword. The key- word is given as a string of maximum length 128 characters.
- ```--rsa:``` Create a new RSA cipher.
- ```--monoLoad <cipher_file>:``` Load a monoalphabetic substitution cipher (caesar or random) from the file specified.
- ```--vigenereLoad <cipher_file>:``` Load a Vigenere cipher from the file specified.
- ```--rsaLoad <file>:``` Create an RSA encrypter/decrypter from the public/private key pair stored in the file specified.

## Cipher function
At most one of the following options may also be specified by the user.
- ```--em <message>:``` Encrypt the given string using the specified cipher scheme.
- ```--ef <file>:``` Encryptthecontentsofthespecifiedfileusingthespecifiedcipherscheme. 
- ```--dm <message>:``` Decrypt the given string using the specified cipher scheme.
- ```--df <file>: ```Decryptthecontentsofthespecifiedfileusingthespecifiedcipherscheme.

## Output options
Finally, the user may add as many of the following output flags as they wish.
- ```--print:``` Print the result of applying the cipher (if any) to the console.
- ```--out <file>:``` Print the result of applying the cipher (if any) to the specified file. 
- ```--save <file>:``` Save the current cipher to the specified file.
