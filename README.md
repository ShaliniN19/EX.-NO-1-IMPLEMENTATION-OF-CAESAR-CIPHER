# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER
## NAME: SHALINI N
## REG NO: 212224040305

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```
#include <stdio.h>
#include <string.h>
#include <ctype.h>

void encrypt(char text[], char key[]) {
    int i, j = 0;
    int keyLen = strlen(key);

    for (i = 0; text[i] != '\0'; i++) {
        if (isalpha(text[i])) {
            char base = isupper(text[i]) ? 'A' : 'a';
            text[i] = ((text[i] - base) +
                       (toupper(key[j % keyLen]) - 'A')) % 26 + base;
            j++;
        }
    }
}

void decrypt(char text[], char key[]) {
    int i, j = 0;
    int keyLen = strlen(key);

    for (i = 0; text[i] != '\0'; i++) {
        if (isalpha(text[i])) {
            char base = isupper(text[i]) ? 'A' : 'a';
            text[i] = ((text[i] - base) -
                       (toupper(key[j % keyLen]) - 'A') + 26) % 26 + base;
            j++;
        }
    }
}

int main() {
    char text[1000], key[100];

    printf("Enter text: ");
    fgets(text, sizeof(text), stdin);
    text[strcspn(text, "\n")] = '\0';

    printf("Enter key: ");
    scanf("%s", key);

    char encrypted[1000];
    strcpy(encrypted, text);

    encrypt(encrypted, key);
    printf("Encrypted Text: %s\n", encrypted);

    decrypt(encrypted, key);
    printf("Decrypted Text: %s\n", encrypted);

    return 0;
}
```

## OUTPUT:

<img width="1258" height="762" alt="image" src="https://github.com/user-attachments/assets/820e9126-6560-4a8f-bcf8-ef04d2facd34" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
