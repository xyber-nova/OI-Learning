取出数组中前 $k$ 个数字.

# [[桶排序]]解法
```cpp
vector<int> a(n);for(auto &i:a)cin>>i; //读入数据
vector<int> buk(<a 中数字的最大值>);
for(auto &i:a)buk[i]++;

vector<int> ans;
for(auto &c:buk)
{
	for(int i=1;i<=c;i++)ans.push_back(i);
	if(ans.size()>=k)break;
}
```