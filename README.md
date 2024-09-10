# calculator
calculator
#include <iostream>
using namespace std;
double calculator(char oper, int a, int b)  {
	switch (oper) {
	case '+':
		return a + b;
	case '-':
		return a - b;
	case '*':
		return a * b;
	case '/':
		if (b == 0) {
			cout << "Деление на ноль запрещено " << endl;
		}
		return a / b;
	default:
		cout << "Ошибка: Такого не знаю" << endl;
		return 0;
	}
	}
int main() {
	setlocale(LC_ALL, "Russian");
	char oper;
	int a, b;
	cout << "Выберите одну из операций (+, -, *, /): ";
	cin >> oper;
	cout << "Выберите два числа " << endl;
	cin >> a >> b;
	int result = calculator(oper, a, b);
	if (oper == '/') {
		cout << a << "/" << b << "=" << result << endl;
	}
	else if (oper == '+') {
		cout << a << "+" << b << "=" << result << endl;
	}
	else if (oper == '*') {
		cout << a << "*" << b << "=" << result << endl;
	}
	else if (oper=='-') {
		cout << a<< "-" << b << "=" << result << endl;
}
		return 0;
	}
