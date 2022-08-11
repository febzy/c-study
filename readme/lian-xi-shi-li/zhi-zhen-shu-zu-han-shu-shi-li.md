# 指针数组函数示例

```cpp
// Some code
#include<iostream>
using namespace std;

void swap1(int* a, int* b);
void sort1(int* arr, int length);

void swap1(int* a, int* b) {
	int temp;
	temp = *a;
	*a = *b;
	*b = temp;
}

void sort1(int* arr, int length) {
	for (int i = 0; i < length - 1; i++) {
		for (int j = 0; j < length - i - 1; j++) {//注意冒泡排序公式
			if (arr[j] > arr[j+1]) {
				swap1(&arr[j], &arr[j+1]);//注意函数调用用括号，不要写成中括号
			}
		}
	}
}

int main() {

	//1.创建数组
	int arr[] = { 4,3,6,9,1,2,10,8,7,5 };
	int length = sizeof(arr) / sizeof(arr[0]);

	//2.函数实现冒泡排序
	sort1(arr, length);

	//3.输出排序后数组
	cout << "排序后数组：" << endl;
	for (int i = 0; i < length; i++) {//输出时按照长度，不用-1
		cout << arr[i] << endl;
	}

	system("pause");
	return 0;
}
```
