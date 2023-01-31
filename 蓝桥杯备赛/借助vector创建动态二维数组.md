# 借助vector创建动态二维数组

```cpp
#include<iostream>
#include<vector>

using namespace std;

int main()
{
	int n,m;
	cin>>n>>m;
	
//输入 
	vector<vector<int>> vec(n);
	
	for(int i=0;i<n;i++)
	{
		for(int j=0;j<m;j++)
		{
			int x;
			cin>>x;
			vec[i].push_back(x);
		}
	}

//法二	
//	vector<int> t;
//	int x;
//	for(int i=0;i<n;i++) {
//		for(int j=0;j<m;j++)
//		{
//			cin>>x;
//			t.push_back(x);
//		}
//		vec.push_back(t);
//		t.clear();
//	}

//输出 
	for(int i=0;i<n;i++)
	{
		for(int j=0;j<m;j++)
		{
			cout<<vec[i][j]<<" ";
		}
	cout<<endl;
	}
} 
```

