#include <math.h>
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <assert.h>
#include <limits.h>
#include <stdbool.h>

int minimumNumber(int n, char* password) {
    
    int L_c = 0;
    int U_c = 0;
    int no = 0;
    int s_c = 0;
    
    int len = strlen(password);
    int i;
    for(i = 0; i<n; i++)
    {
        if(password[i] >= 'a' && password[i] <= 'z')
            L_c++;
        else if(password[i] >= 'A' && password[i] <= 'Z')
            U_c++;
        else if(password[i] >= '0' && password[i] <= '9')
            no++;
        else
            s_c++;
    }
    
    int add = 0;
    if(L_c == 0)
        add++;
    if(U_c == 0)
        add++;
    if(no == 0)
        add++;
    if(s_c == 0)
        add++;
    
    len = len + add;
    
    if(len < 6)
        add = add + 6 - len;
    
    return add;
}

int main() {
    int n; 
    scanf("%i", &n);
    char* password = (char *)malloc(512000 * sizeof(char));
    scanf("%s", password);
    int answer = minimumNumber(n, password);
    printf("%d\n", answer);
    return 0;
}
