# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

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
int main()
{
  char text[100];
  int key, i;
  printf("Enter text: ");
  scanf("%s", text);
  printf("Enter key: ");
  scanf("%d", &key);
  for(i = 0; text[i] != '\0'; i++)
  {
   text[i] = text[i] + key;
  }
  printf("Cipher Text: %s", text);
  return 0;
}
```

## OUTPUT:

<img width="773" height="871" alt="image" src="https://github.com/user-attachments/assets/2b42c72c-8564-4cdc-8e4d-a485922d0301" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
