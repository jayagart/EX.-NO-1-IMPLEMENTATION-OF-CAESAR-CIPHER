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
#include <ctype.h>
int main()
{
char plain[100], cipher[100];
int key, i, length;
printf("Enter the plain text: ");
scanf("%99s", plain);
printf("Enter the key value: ");
scanf("%d", &key);
key = ((key % 26) + 26) % 26;
printf("\nPLAIN TEXT: %s", plain);
length = strlen(plain);
printf("\nENCRYPTED TEXT: ");
for (i = 0; i < length; i++)
{
cipher[i] = plain[i];
if (isupper(plain[i]))
cipher[i] = ((plain[i]- 'A' + key) % 26) + 'A';
else if (islower(plain[i]))
cipher[i] = ((plain[i]- 'a' + key) % 26) + 'a';
}
cipher[length] = '\0';
printf("%s", cipher);
printf("\nDECRYPTED TEXT: ");
for (i = 0; i < length; i++)
{
plain[i] = cipher[i];
if (isupper(cipher[i]))
plain[i] = ((cipher[i]- 'A'- key + 26) % 26) + 'A';
else if (islower(cipher[i]))
plain[i] = ((cipher[i]- 'a'- key + 26) % 26) + 'a';
}
plain[length] = '\0';
printf("%s\n", plain);
return 0;
}
```

## OUTPUT:
<img width="360" height="142" alt="image" src="https://github.com/user-attachments/assets/f13a2679-3166-45a3-83a6-95c1f1609ddd" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
