# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER
### NAME: KIRUTIKA K R
### REG NO: 212224230128
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
<img width="456" height="227" alt="image" src="https://github.com/user-attachments/assets/90323553-10cd-4615-b6ed-de2e8c83a0ae" />



## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
