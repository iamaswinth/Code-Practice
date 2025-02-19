# Bigger is Better   

![Question 1](https://i.ibb.co/fYKBBfjC/Screenshot-2025-02-19-233309.png)

![Question 2](https://i.ibb.co/nNtNkNKP/Screenshot-2025-02-19-233322.png)

## Code :

``` c++
#include <bits/stdc++.h>
using namespace std;

string lexicoRes(int N, string A)
{
    string P = A;

    while (true)
    {

        bool modified = false;

        for (int i = N - 1; i >= 0; i--)
        {
            if (P[i] != 'z')
            {
                P[i]++;
                modified = true;
                break;
            }
        }

        if (!modified)
            return "-1";

        string revP = P;

        reverse(revP.begin(), revP.end());

        if (P > A && revP > A)
        {
            return P;
        }
    }
}

int main()
{
    // your code goes here
    int T;
    cin >> T;

    while (T--)
    {
        int N;
        string A;
        cin >> N >> A;

        cout << lexicoRes(N, A) << endl;
    }
    return 0;
}
```

## Input
```
4
8
codechef
4
five
1
z
7
rallets
```

## Output
```
topcoder
four
-1
specter
```