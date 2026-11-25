# Word_Palindrome_Checker
a code where we can check if palindrome or not 


#include <stdio.h>

int main() {
    char words[100];
    int size = 0;

    printf("Enter a word: ");
    scanf("%s", words);

    while (words[size] != '\0') {
        size++;
    }

    /*print sa original*/
    printf("%s\n", words);

    /*print pabaliktad*/
    for (int i = size - 1; i >= 0; i--) {
        printf("%c",words[i]);
    }
    printf("\n");

    /*para ma check if palindrome*/
    int tail = size - 1;
    int ispalindrome = 1;
    for (int head = 0; head < size/ 2; head++) {
        if (words[head] != words[tail]) {
            ispalindrome = 0;
            break;
        }
        tail--;
    }
        if (ispalindrome == 1)
        printf("Palindrome\n");
        else 
        printf("Is NOT Palindrome\n");
    
    return 0;
}

    
