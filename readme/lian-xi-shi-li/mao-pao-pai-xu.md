# 冒泡排序

```cpp
// Some code
#include<iostream>
using namespace std;

int main() {

	//冒泡排序
	//排序总轮数 = 元素个数 - 1
	//每轮对比次数 = 元素个数 - 排序轮数 - 1 = 排序总轮数 - 排序轮数

	int arr[] = { 4,2,8,0,5,7,1,3,9 };
	int length = sizeof(arr) / sizeof(arr[0]);
	//int end = length - 1;
	
	//外层循环次数为排序总轮数
	for (int i = 0; i < length - 1; i++) {
		/*cout << arr[i] << "/" << arr[i + 1] << endl;
		system("pause");*/
		//内层循环次数为每轮对比次数
		for (int j = 0; j < length - i - 1; j++) {
			if (arr[j] > arr[j + 1]) {
				int temp = arr[j];
				arr[j] = arr[j + 1];
				arr[j + 1] = temp;
			}
			
		}
	}

	////错误点，while的条件需要注意真假，为真执行，为假跳出
	//while (end != 0) {
	//	//错误点，循环次数应该等于总长度-1，因为最后一次不用对比了
	//	for (int i = 0; i < length - 1; i++) {
	//		/*cout << arr[i] << "/" << arr[i + 1] << endl;
	//		system("pause");*/

	//		if (arr[i] > arr[i + 1]) {
	//			temp = arr[i];
	//			arr[i] = arr[i + 1];
	//			arr[i + 1] = temp;
	//		}
	//	}
	//	end--;
	//}
	

	for (int i = 0; i < length; i++) {
		cout << arr[i] << endl;
	}

	system("pause");
	return 0;
}
```
