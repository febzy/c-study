# 猜数字游戏（while语句）

```
#include<iostream>
using namespace std;

int main() {

	//添加随机数种子，利用当前系统时间生成随机数
	srand(time(NULL));
	//srand((unsigned int)time(NULL));
	
	//使用while语句做猜数字游戏

	int success = rand()%100 + 1;
	int input;

	cout << "让我们来猜数字吧！请输入一个数字：" << endl;
	cin >> input;
	while (success != input) {
		if (success > input) {
			cout << "猜错了，要更大才行！" << endl;
			cin >> input;
		}
		if (success < input) {
			cout << "猜错了，要更小才行！" << endl;
			cin >> input;
		}
	}

	cout << "恭喜你，猜对了！" << endl;

	system("pause");
	return 0;
}
```
