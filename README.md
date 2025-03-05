# Answer
answer of some of question
## 目录
  -[米哈游24春招](#米哈游24春招实习笔试)
  




  ## 米哈游24春招实习笔试


```
int main()
{
	int n = 0;
	cin >> n;
	int map[13000], a[13000];
	for (int i = 1; i <= n; i++){
		cin >> a[i];
		map[i] = i;//记录初始位置
	}

	int sum = n;
	while (sum--) {
		set<int>st;//统计
		for (int i = 1; i <= n; i++) {
			if (a[i] == 1) {//向右
				map[i] = min(n + 1, map[i] + 1);
			}
			else {//向左
				map[i] = max(0, map[i] - 1);
			}
			if (map[i] >= 1 && map[i] <= n) {
				st.insert(map[i]);
			}
		}
		cout <<n-st.size() << " ";
	}

	system("pause");
	return 0;
}
```




