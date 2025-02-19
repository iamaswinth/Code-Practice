# Bigger is Better

![Question](https://media-hosting.imagekit.io//4b8430a80a804140/IMG_20250220_000744.jpg?Expires=1834598413&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=uqcMwofB1K-NcKMeOxzZwNvV8tFqEW9shXaa5bKZjAeAPc4JIYErZvF6B5uXdSqOBZYj-gCM8M0eHLbX572BnDZ-GejC7KrMVwxphA2DLXmMx9Y3KesGPyhMt78-GFJTMjz0qNiveTIITbGFmCoDcyofeeP85vkEOd4IcT6VR-RskrefQQHieRNigOvkz107AV1BcBwRKmD4pluQQm78uKrSPf8MGjQopY2xsWDvhHgaERPMpXcH1EqFf3MmEAU~qeEpnDPBBqVvRUrZP-Kk0fIUCrilQd-UhZpnQAXp743Ns~CeOMFArDJrz2W0TCk4Kda7PC4uXdcdpYi8V02bJA__)

## Code :

```c++
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
