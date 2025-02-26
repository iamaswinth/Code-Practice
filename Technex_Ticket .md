# Technex Ticket

![Technex Ticket](https://media-hosting.imagekit.io//65505ebf62ac4587/IMG_20250226_223619.jpg?Expires=1835199993&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=XjTP1RX6jACm5xp1AtoThQ3Ax9ubF4yL6iXK0qmk9H7NHN0hhSSLmC5mD9aYVB2j6efufloyUjskMN3lwltM-01uzbaz6X-61ws9haBH41AszboO2qfRQE9tLL~WvL1klrNr1DxPws8X8PeAYnt1fDxR7494HVqxzk4dhY-hTBiDRFiAwGV0hC9k-EUezeU~OPNZSh1MU4-lc~x7ldoeeBXz91m01HgAuJDrTq7DSMUpO0g417UNrg38sdqv6UL7ku3BhssZQZmbe9TzxRUYuNwxlOTVl2188K~upn17rvTAaxW~K2nkhFjkxnOr0CCwAvCssq3JGhz-iGiqTcCzIQ__)

### My Code :

```c++
#include <bits/stdc++.h>
using namespace std;

void Ticket(int N)
{
    vector<int> arr;

    for (int i = 1; i <= N; i++)
    {
        arr.push_back(i);
    }

    int cnt = 1;

    while (arr.size() >= 1)
    {

        if (arr[0] == N || (arr[2] == N && arr.size() > 2))
        {
            break;
        }

        if (arr.size() > 2)
        {
            arr.erase(arr.begin() + 2);
        }
        arr.erase(arr.begin());

        cnt++;

        for (int i = 0; i < arr.size(); i++)
        {
            cout << "arr :" << arr[i] << " ";
        }

        cout << endl;
    }

    cout << "cnt :" << cnt << endl;
}

int main()
{
    int T;
    cin >> T;

    while (T--)
    {
        int N;
        cout << endl;
        cin >> N;

        Ticket(N);
    }

    return 0;
}

```

## My Input / Output :

```
5

1
cnt :1

2
arr :2
cnt :2

3
cnt :1

4
arr :2 arr :4  // After Removing the 1st and 3rd element
arr :4
cnt :3

5
arr :2 arr :4 arr :5
cnt :2
```


## Explanation :

I used **(arr vector)** to store the values.

```c++
vector<int> arr;
for (int i = 1; i <= N; i++) {
    arr.push_back(i);
}
```

Initialized Counter.

```c++
int cnt = 1;
```

Checking If N Gets a Ticket.

```c++
if (arr[0] == N || (arr[2] == N && arr.size() > 2)) {
    break;
}
```

Removing 3rd and 1st People from the Queue.

```c++
if (arr.size() > 2) {
    arr.erase(arr.begin() + 2);
}
arr.erase(arr.begin());
```

Debugging Output

```c++
for (int i = 0; i < arr.size(); i++) {
    cout << "arr :" << arr[i] << " ";
}
cout << endl;
```
