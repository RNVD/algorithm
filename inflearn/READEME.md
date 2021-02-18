# 기초

11번

```c++

#include<iostream>
#include<stdio.h>

using namespace std;

int main()
{
	int n, tmp, count=0;
	scanf("%d",&n);
	
	for(int i =1  ;i <=n;i++)
	{
		tmp=i;
		while(tmp>0)
		{
			tmp=tmp/10;
			count++;
		}
	}
}

```

13번

```c++

#include<iostream>
#include<stdio.h>

using namespace std;

int main()
{
	vector <int> v(10);
	int n,a,tmp,max=-1, st;
	scanf("%d",&n);
	
	tmp = n;
	while(tmp>0)
	{
		a=tmp%10;
		v[a]++;
		tmp= tmp/10;
	}
	//vector<int>::iteraotr it;
	for(int i =0;i<v.size();i++)
	{
		if(v[i]>=max) // i가 0부터 올라가니깐 같으면 그냥 i 값 새로넣는게 더 큰거임
			{
				max= v[i]; 
				st=i;
			}
	}
	printf("%d",st);
	
}

```

14번

```c++
#include<iostream>
#include<string>
#include<stdio.h>

using namespace std;

int reverse(int x)
{
	string s = to_string(x);
	reverse(s.begin(),s.end());
	return stoi(s);
}
bool isPrime(int x)
{
	bool isP;
	int count=0;
	for(int i = 1 ; i<=x;i++)
	{
		if(x%i==0)
			count++;
	}
	if(count==2)
		isP=true;
		
	return isP;
}
int main()
{
	int n,k,r;
	scanf("%d",&n);
	for(int i = 0 ; i<n;i++)
	{
		scanf("%d",k);
		r=reverse(k);
		if(isPrime(r))
			printf("%d ",&r);
	}
}


```

15번

```c++
#include<iostream>
#include<stdio.h>

using namespace std;

int main()
{
	int n,cnt=0,count;
	scanf("%d",&n);
	
	for(int i = 1 ; i<=n;i++)
	{
		count=0;
		for(int j = 1 ; j<=i;j++)
		{
			if(i%j==0)
				count++;
		}
		if(count==2)
			cnt++;
	}
	printf("%d",cnt);

}


```



16번

```c++

#include<string>
#include<vector>
#include<algorithm>

using namespace std;

int main()
{	
	vector<string> v;
	for(int i=0 ; i<2;i++)
		scanf("%s",v[i]);
	
	sort(v[0].begin(),v[0].end());
	sort(v[1].begin(),v[1].end());
	
	if(v[0].compare(v[1]))
		printf("YES");
	else
		printf("NO");
	
}

```

