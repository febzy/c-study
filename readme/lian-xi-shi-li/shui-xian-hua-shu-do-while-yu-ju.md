# 水仙花数（do while语句）

```cpp
#include<iostream>
#include<math.h>
using namespace std;

int main() {

	//水仙花数：一个三位数，每个位数的三次幂之和等于它本身
	//例：1^3 + 5^3 + 3^3=153
	//使用do while语句，写出所有的3位数水仙花数

	//定义一个最小的三位数，循环加到999
	int num = 100;
	int Ge = 0;
	int Shi = 0;
	int Bai = 0;


	do {
		//分离每一位
		/*Ge = num % 10;
		Shi = (num % 100 - Ge) / 10;
		Bai = (num % 1000 - Shi * 10 - Ge) / 100;*/
		Ge = num % 10;
		Shi = (num / 10) % 10;
		Bai = num / 100;
		if (num == (pow(Ge, 3) + pow(Shi, 3) + pow(Bai, 3))) {
			cout << num << endl;
			cout << Ge << "^3 + " << Shi << "^3 + " << Bai << "^3 = " << num << endl;
		}
		num = num + 1;
	} while (num < 1000);

	system("pause");
	return 0;
}
```
