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

## Examples
1. Make a new Caesar cipher with shift parameter 15, apply it to the provided message, output the result to file encr.txt, and save the cipher to file ca15:
```java -jar <your_jar> --caesar 15 --em "ENCrypt␣Me!" --out encr.txt --save ca15```
2.  Loadamonoalphabeticsubstitutioncipherfromfileca15,useittodecryptthemessage in file encr.txt, and print the result to the console:
```java -jar <your_jar> --monoLoad ca15 --df encr.txt --print```
3. Create an RSA encrypter/decrypter, use it to encrypt the given message, save the ci- phertext to a file encr.txt, and save the key in a file mykey.txt:
```java -jar <your_jar> --rsa --em "rsa␣is␣alright,␣i␣guess" --out encr.txt --save mykey.txt```
4.  Load an RSA key from a file mykey.txt, use it to decrypt the ciphertext in the file encr.txt, print the resulting plaintext, and also save the plaintext to a file decr.txt:
```java -jar <your_jar> --rsaLoad myKey.txt --df encr.txt --out decr.txt --print```
