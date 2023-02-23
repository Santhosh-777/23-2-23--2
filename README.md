#include <stdio.h>

int main() {
    int n1, n2, count = 0;
    
    printf("Enter the value of n1: ");
    scanf("%d", &n1);
    
    printf("Enter the value of n2: ");
    scanf("%d", &n2);
    
    printf("Odd numbers between %d and %d (excluding the third odd number):\n", n1, n2);
    
    for (int i = n1; i <= n2; i++) {
        if (i % 2 == 0) {
            continue; // skip even numbers
        }
        count++; // increment the count for odd numbers
        if (count == 3) {
            count = 0; // reset the count after skipping the third odd number
            continue; // skip the third odd number
        }
        printf("%d\n", i);
    }
    
    return 0;
}
