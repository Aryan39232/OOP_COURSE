#include <bits/stdc++.h>
using namespace std;

int prime(int n)
{
    int m = n / 2, flag = 0 , K;
    for (int i = 2; i <= m; i++)
    {
        if (n % i == 0)
        {
            K = 0;
            flag = 1;    
            break;  
        }
    }
    if (flag == 0)
    {
        K = 1;
    }    

    return K;    
}

int main(void)
{
    ios_base::sync_with_stdio(false);
    cin.tie(NULL);

    int T, sa, en;
    scanf("%d", &T);
    for (int i = 0; i < T; i++)
    {
        int K = 0;
        scanf("%d %d", &sa, &en);
        // for (int j = sa; j <= en; j++)
        int j = sa;
        while (j <= en)
        {
            if (prime(j + 2) == 1)
            {
                K += 1;
                j += 2;
            }
            else
            {
                K += 1; 
                j ++;
            }
        }
        if(prime(en+1) == 1){
            K ++ ;
        }
        printf("%d\n",K - 1);
    }

    return 0;
}
