# Cool Subsequence

> **As of to my underStanding**

### How to find a subSequence !

<<<<<<< HEAD

![Question 1](https://iili.io/2mOnjJ1.png)

![Question 2](https://iili.io/2mOnXUP.png)


If the SubSequence is only 2 Element, Then this will give the correct out.


=======
If the SubSequence is only 2 Element, Then this will give the correct out.

1
5
10 20 30 40 50
10 30
>>>>>>> 2fcfc10 (Initial commit)

| Input                       | Output       |
| --------------------------- | ------------ |
| 1 <br/>5<br/>10 20 30 40 50 | 2 <br/>10 30 |

```c++
#include<bits/stdc++.h>

using namespace std;

void compute(){
int n;
cin >> n;

    vector<int> arr(n);
    unordered_set<int> elemets;

    for(int i = 0; i < n; i++){
        cin >> arr[i];

        elemets.insert(arr[i]);
    }

    for(int i = 0; i < n; i++){
        for(int j = i + 1; j < n; j++){
            unordered_set<int> avgs;

            vector<int> subSeq = {arr[i], arr[j]};

            // cout << arr[i] << " " << arr[j] << endl;


            avgs.insert(arr[i]);
            avgs.insert(arr[j]);
            avgs.insert((arr[i] + arr[j]) / 2);

            for(int avg : avgs){
                if(elemets.find(avg) != elemets.end()){
                    cout << subSeq.size() << endl;

                    for(int s : subSeq){
                        cout << s << " ";

                    }
                    return;


                }

                else{
                    break;
                }
            }

        }
    }

}

int main(){
int t;
cin >> t;
while (t--)
{
compute();
}

    return 0;

}
```

# If 3 SubSequence

_In the Code I am having some error, if you know please help me !_

> **The Expected output is**

| Input                          | Output       |
| ------------------------------ | ------------ |
| 1 <br/>9<br/>8 4 2 1 3 2 5 8 2 | 3 <br/>2 2 8 |

> **But Waht I am getting is**

| Input                          | Output       |
| ------------------------------ | ------------ |
| 1 <br/>9<br/>8 4 2 1 3 2 5 8 2 | 3 <br/>8 2 1 |

**If You know Please Help !!**

```c++
#include<bits/stdc++.h>

using namespace std;

void compute(){
    int n;
    cin >> n;

    vector<int> arr(n);
    unordered_set<int> elemets;

    for(int i = 0; i < n; i++){
        cin >> arr[i];

        elemets.insert(arr[i]);
    }

    for(int i = 0; i < n; i++){
        for(int j = i + 1; j < n; j++){
            for(int k = j + 1; k < n; k++ ){
                unordered_set<int> avgs;

                vector<int> subSeq = {arr[i], arr[j], arr[k]};

                // cout << arr[i] << " " << arr[j] << endl;


                avgs.insert(arr[i]);
                avgs.insert(arr[j]);
                avgs.insert(arr[k]);
                avgs.insert((arr[i] + arr[j]) / 2);
                avgs.insert((arr[i] + arr[k]) / 2);
                avgs.insert((arr[j] + arr[k]) / 2);
                avgs.insert((arr[i] + arr[j] + arr[k]) / 3);

                bool valid = true;
                for(int avg : avgs){

                    if(elemets.find(avg) == elemets.end()){
                        valid = false;
                        break;
                    }
                }

                if(valid){
                    cout << subSeq.size() << endl;
                    for(int s : subSeq){
                        cout << s << " ";
                    }
                    return;
                    break;
                }

            }

        }
    }

}

int main(){
    int t;
    cin >> t;
    while (t--)
    {
        compute();
    }

    return 0;
}
```

### Note: GPT is a BITCH !!
