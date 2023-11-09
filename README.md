# Codechef_starters_107_Div3

# Pending Assignments
<details>
<summary>Python</summary>

```python
t = int(input())
for _ in range(t):
    a, b, c = map(int, input().split())
    print("YES" if a * b <= 1440 * c else "NO")
```
</details>

<details>
<summary>Cpp</summary>

```cpp
#include <iostream>
using namespace std;

int main() {
	int t,a,b,c;
	cin>>t;
	while(t--)
	{
	    cin>>a>>b>>c;
	    cout<<(a*b<=1440*c?"YES":"NO")<<endl;
	}
	return 0;
}
```
</details>


<details>
<summary>Java</summary>

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int t = scanner.nextInt();
        for (int i = 0; i < t; i++) {
            int a = scanner.nextInt();
            int b = scanner.nextInt();
            int c = scanner.nextInt();
            System.out.println(a * b <= 1440 * c ? "YES" : "NO");
        }
    }
}

```
</details>

<!-- Second Question -->
# Rock Paper Scissor

<details>
<summary>Python</summary>

```python
t = int(input())
for _ in range(t):
    n = int(input())
    A = input()
    B = input()
    
    counter1 = counter2 = 0
    
    for i in range(n):
        if (A[i] == 'R' and B[i] == 'P') or \
           (A[i] == 'S' and B[i] == 'R') or \
           (A[i] == 'P' and B[i] == 'S'):
            counter2 += 1
        elif (A[i] == 'R' and B[i] == 'S') or \
             (A[i] == 'P' and B[i] == 'R') or \
             (A[i] == 'S' and B[i] == 'P'):
            counter1 += 1

    num = 0
    if counter2 >= counter1:
        num = ((counter2 - counter1) // 2) + 1
        print(num)
    else:
        print(0)

```

</details>

<details>
<summary>Cpp</summary>
  
```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    int t;
    cin >> t;

    while (t--) {
        int n;
        cin >> n;

        string A ;
        cin >> A ;
        string B ;
        cin>> B;

        int counter1 = 0, counter2 = 0;

        for (int i = 0; i < n; i++) {
            if ((A[i] == 'R' && B[i] == 'P') ||
            (A[i] == 'S' && B[i] == 'R') || 
            (A[i] == 'P' && B[i] == 'S'))
            {
                counter2 ++;
            }
            else if ((A[i] == 'R' && B[i] == 'S') ||
            (A[i] == 'P' && B[i] == 'R') ||
            (A[i] == 'S' && B[i] == 'P'))
            {
                counter1 ++;
            } 
            
        }

        int num = 0;
        if (counter2 >= counter1) {
            num = ((counter2 - counter1) / 2) + 1;
            cout << num << endl;
        } 
        else 
            cout << 0 << endl;
        
    }

    return 0;
}

```

</details>
<!-- Java -->
<details>
<summary>Java</summary>

```Java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int t = scanner.nextInt();

        while (t-- > 0) {
            int n = scanner.nextInt();
            String A = scanner.next();
            String B = scanner.next();

            int counter1 = 0, counter2 = 0;

            for (int i = 0; i < n; i++) {
                if ((A.charAt(i) == 'R' && B.charAt(i) == 'P') ||
                    (A.charAt(i) == 'S' && B.charAt(i) == 'R') ||
                    (A.charAt(i) == 'P' && B.charAt(i) == 'S')) {
                    counter2++;
                } else if ((A.charAt(i) == 'R' && B.charAt(i) == 'S') ||
                           (A.charAt(i) == 'P' && B.charAt(i) == 'R') ||
                           (A.charAt(i) == 'S' && B.charAt(i) == 'P')) {
                    counter1++;
                }
            }

            int num = 0;
            if (counter2 >= counter1) {
                num = ((counter2 - counter1) / 2) + 1;
                System.out.println(num);
            } else {
                System.out.println(0);
            }
        }
    }
}

```
</details>

# OR Permutation

<details>
<summary>Python</summary>

```python
t = int(input())
for _ in range(t):
    n = int(input())
    for i in range(n, 0, -1):
        print(i, end=" ")
    print()

```
</details>

<details>
<summary>Cpp</summary>

```cpp
#include <iostream>
using namespace std;

int main() {
	int t;
	cin>>t;
	while(t--){
	    int n;
	    cin>>n;
	    for(int i=n;i>=1;i--){
	        cout<<i<<" ";
	    }
	    
	    cout<<endl;
	}
	return 0;
}
```
</details>

<details>
<summary>Java</summary>

```Java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int t = scanner.nextInt();

        while (t-- > 0) {
            int n = scanner.nextInt();
            for (int i = n; i >= 1; i--) {
                System.out.print(i + " ");
            }
            System.out.println();
        }
    }
}

```
</details>

# Save People

<details>
    <summary>Python Code</summary>

```
        def solve():
        n, m, x, y = map(int, input().split())
        mul = n * m
        print(max(mul - x * m, mul - (n - x + 1) * m, mul - y * n, mul - (m - y + 1) * n))
    
        t = int(input())
        for _ in range(t):
            solve()


```
</details>


<details>
  	<summary>C++</summary>
  
```
        #include <iostream>
        #include <algorithm>
        #include <vector>
        #include <math.h>
        #include <set>
        #define rep(i,a,b) for(int i=a; i<b; i++)
        
        using namespace std;
        
        typedef long long ll;
        
        void solve(){
            ll n,m,x,y; cin>>n>>m>>x>>y;
            ll mul=n*m;
            cout<<max({mul-x*m,mul-m*(n-x+1),mul-y*n,mul-n*(m-y+1)});
            cout<<"\n";
        }
        
        int main(){
           ios_base::sync_with_stdio(false);
           cin.tie(NULL); cout.tie(NULL);
           int t; cin>>t; while(t--)solve();
           return 0;
        }
```
</details>


<details>
	<summary>JAVA</summary>
  
```

      import java.util.Scanner;

      public class Main {
          public static void main(String[] args) {
              Scanner sc = new Scanner(System.in);
              int t = sc.nextInt();
      
              while (t-- > 0) {
                  long n = sc.nextLong();
                  long m = sc.nextLong();
                  long x = sc.nextLong();
                  long y = sc.nextLong();
      
                  long mul = n * m;
                  long result = Math.max(Math.max(mul - x * m, mul - (n - x + 1) * m), Math.max(mul - y * n, mul - (m - y + 1) * n));
      
                  System.out.println(result);
              }
          }
      }


```
</details>
