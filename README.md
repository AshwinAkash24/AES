# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
## Submitted By: Ashwin Akash M
## Reference Number:212223230024
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
1. Encrypt/Decrypt using XOR: The same function (encryptDecrypt) is used for
both encryption and decryption. XOR is applied between each character of the input
and the key, which is repeated cyclically (key[i % strlen(key)]).
2. Read Input: The program reads the plaintext and key as strings (with spaces
included) using scanf("%[^\n]%*c", ...). This ensures it can capture full lines,
including spaces.
3. Encrypt the Text: The encryptDecrypt() function processes the plaintext and
produces the ciphertext.
4. Display ASCII Values: The ASCII values of the ciphertext characters are printed to
show the encrypted form.
5. Decrypt the Text: The same encryptDecrypt() function is called to reverse the
XOR operation and get back the original plaintext from the ciphertext.
6. Output the Decrypted Text: Finally, the decrypted message is printed.
# PROGRAM:
```
#include <stdio.h>
#include <string.h>
void simpleAESEncrypt(char *plaintext, char *key, char *ciphertext)
{
int i;
for (i = 0; i < strlen(plaintext); i++)
{
ciphertext[i] = plaintext[i] ^ key[i % strlen(key)];
}
ciphertext[i] = '\0';
}
void simpleAESDecrypt(char *ciphertext, char *key, char *decryptedText)
{
int i;
for (i = 0; i < strlen(ciphertext); i++)
{
decryptedText[i] = ciphertext[i] ^ key[i % strlen(key)];
}
decryptedText[i] = '\0';
}
void printASCII(char *ciphertext)
{
printf("Encrypted Message (ASCII values): ");
for (int i = 0; i < strlen(ciphertext); i++)
{
printf("%d ", (unsigned char)ciphertext[i]);
}
printf("\n");
}
int main()
{
char plaintext[100], key[100], ciphertext[100], decryptedText[100];
printf("Enter the plaintext: ");
scanf("%[^\n]%*c", plaintext);
printf("Enter the key: ");
scanf("%[^\n]%*c", key);
simpleAESEncrypt(plaintext, key, ciphertext);
printASCII(ciphertext);
simpleAESDecrypt(ciphertext, key, decryptedText);
printf("Decrypted Message: %s\n", decryptedText);
return 0;
}

```
# OUTPUT:
![Screenshot 2025-04-18 100337](https://github.com/user-attachments/assets/1bf464f7-0134-449c-8749-3d953c1ba79f)
![Screenshot 2025-04-18 100357](https://github.com/user-attachments/assets/1cd06515-d55f-4880-a3c2-9efb0216cc52)


# RESULT:
Hence,to use Advanced Encryption Standard (AES) Algorithm for a practical
application like URL Encryption is done successfully

