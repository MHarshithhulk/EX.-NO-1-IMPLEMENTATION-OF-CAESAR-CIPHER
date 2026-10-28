# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER                                                                                                    
## NAME: HARSHITH M 
## REG NO. : 212224040206
## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
# ENCRYPTION:
```c
#include <stdio.h>

int main()
{
    char str[100];
    int key, i;

    scanf("%s", str);
    scanf("%d", &key);

    for(i = 0; str[i] != '\0'; i++)
    {
        if(str[i] >= 'A' && str[i] <= 'Z')
            str[i] = (str[i] - 'A' + key + 26) % 26 + 'A';
        else if(str[i] >= 'a' && str[i] <= 'z')
            str[i] = (str[i] - 'a' + key + 26) % 26 + 'a';
    }

    printf("%s", str);

    return 0;
}
```
# DECRYPTION:
```C
#include <stdio.h>

int main()
{
    char str[100];
    int key, i;

    printf("Enter text: ");
    scanf("%99s", str);

    printf("Enter key: ");
    scanf("%d", &key);

    for(i = 0; str[i] != '\0'; i++)
    {
        if(str[i] >= 'A' && str[i] <= 'Z')
            str[i] = (str[i] - 'A' - key % 26 + 26) % 26 + 'A';
        else if(str[i] >= 'a' && str[i] <= 'z')
            str[i] = (str[i] - 'a' - key % 26 + 26) % 26 + 'a';
    }

    printf("Decrypted value: %s", str);

    return 0;
}
```
## OUTPUT:
## ENCRYPTION:
<img width="1915" height="1132" alt="image" src="https://github.com/user-attachments/assets/698355f0-9a99-4c42-8356-2e38529f1fa1" />


## DECRYPTION:
<img width="1917" height="1087" alt="image" src="https://github.com/user-attachments/assets/5b27935c-cb09-43cf-a185-d59d809755c7" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
