# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER
## Name: THEJA SREE G
## reg no: 212224110056
## dept : CSE (IOT)
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

int main()
{
    char text[100];
    int key, i;

    printf("Enter the Plain Text: ");
    scanf("%s", text);

    printf("Enter the Key: ");
    scanf("%d", &key);

    // Encryption
    for(i = 0; text[i] != '\0'; i++)
    {
        if(text[i] >= 'A' && text[i] <= 'Z')
        {
            text[i] = ((text[i] - 'A' + key) % 26 + 26) % 26 + 'A';
        }
        else if(text[i] >= 'a' && text[i] <= 'z')
        {
            text[i] = ((text[i] - 'a' + key) % 26 + 26) % 26 + 'a';
        }
    }

    printf("Cipher Text: %s\n", text);

    // Decryption
    for(i = 0; text[i] != '\0'; i++)
    {
        if(text[i] >= 'A' && text[i] <= 'Z')
        {
            text[i] = ((text[i] - 'A' - key) % 26 + 26) % 26 + 'A';
        }
        else if(text[i] >= 'a' && text[i] <= 'z')
        {
            text[i] = ((text[i] - 'a' - key) % 26 + 26) % 26 + 'a';
        }
    }

    printf("Decrypted Text: %s\n", text);

    return 0;
}


```

## OUTPUT:
<img width="372" height="161" alt="image" src="https://github.com/user-attachments/assets/e2352cf2-df1d-4d32-a264-0c455a10bc2e" />



## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
