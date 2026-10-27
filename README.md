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
#include <string.h> 
 
int main() 
{ 
    char text[100], enc[100], dec[100]; 
    int key, i; 
 
    printf("Enter the plain text: "); 
    scanf(" %[^\n]", text); 
 
    printf("Enter the key: "); 
    scanf("%d", &key); 
 
    key = ((key % 26) + 26) % 26; 
 
    for (i = 0; text[i] != '\0'; i++) 
    { 
        if (text[i] >= 'A' && text[i] <= 'Z') 
        { 
            enc[i] = (text[i] - 'A' + key) % 26 + 'A'; 
            dec[i] = (enc[i] - 'A' - key + 26) % 26 + 'A'; 
        } 
        else if (text[i] >= 'a' && text[i] <= 'z') 
        { 
            enc[i] = (text[i] - 'a' + key) % 26 + 'a'; 
            dec[i] = (enc[i] - 'a' - key + 26) % 26 + 'a'; 
        } 
        else 
        { 
            enc[i] = text[i]; 
            dec[i] = text[i]; 
        } 
    } 
 
    enc[i] = '\0'; 
    dec[i] = '\0'; 
 
    printf("\nPlain Text: %s", text); 
    printf("\nEncoded Text: %s", enc); 
    printf("\nDecoded Text: %s\n", dec); 
 
    return 0; 
} 
```

## OUTPUT:
<img width="787" height="352" alt="Screenshot 2026-10-22 092516" src="https://github.com/user-attachments/assets/6ad7cd16-8f29-47ea-8647-d40e4084bc34" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
