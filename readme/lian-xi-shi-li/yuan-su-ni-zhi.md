# 元素逆置

```
// Some code
#include<iostream>
using namespace std;

int main() {
	//元素逆置
	//定义一个数组，将数组内数字逆置

	int arr[] = { 1,2,3,4,5,6,7,8 };

	int start = 0;
	//错误点，相除得到数组长度但是最后一个值是长度-1
	int end = sizeof(arr) / sizeof(arr[0]) - 1;
	int length = sizeof(arr) / sizeof(arr[0]);

	cout << "当前数组为" << endl;
	for (int i = 0; i < length; i++) {
		cout << arr[i] << endl;
	}

	cout << "数组长度为：" << end << endl;

	//逆置操作，设置start和end，设置temp为中间值
	//在start < end情况下，交换两个数
	int temp = 0;
	while (start < end) {
		temp = arr[start];
		arr[start] = arr[end];
		arr[end] = temp;

		start++;
		end--;
	}


	cout << "逆置数组为" << endl;
	for (int i = 0; i < length; i++) {
		cout << arr[i] << endl;
	}




	system("pause");
	return 0;
}
```
