# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:
```
Name: K Hasini
Reg: 212224240074
```

```
#include <stdio.h>
#include <string.h>

void xor_encrypt_decrypt(char *input, char *key) {
    int input_len = strlen(input);
    int key_len = strlen(key);

    for (int i = 0; i < input_len; i++) {
        input[i] = input[i] ^ key[i % key_len];
    }
}

int main() {
    char text[100];
    char key[100];

    // Step 1: Get the text input
    printf("Enter the text to encrypt: ");
    scanf("%s", text);    // Take user input

    printf("You entered: %s\n", text);

    // Step 2: Get the key input
    printf("Enter the key: ");
    scanf("%s", key);

    printf("Key entered: %s\n", key);

    // Step 3: Encrypt the text
    xor_encrypt_decrypt(text, key);
    printf("\nEncrypted text: %s\n", text);

    // Step 4: Decrypt the text
    xor_encrypt_decrypt(text, key);
    printf("Decrypted text: %s\n", text);

    return 0;
}

```

# OUTPUT:
![image](https://github.com/user-attachments/assets/e3dfd1f3-1051-4900-bc4b-ffb490ea00c8)

# RESULT:

The Program is implemented successfully


