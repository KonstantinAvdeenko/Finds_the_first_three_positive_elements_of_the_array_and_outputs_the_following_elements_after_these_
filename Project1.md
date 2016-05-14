#include <tchar.h>
#include <iostream>
#include <string>
#include <ctime>
using namespace std;

int _tmain(int argc, wchar_t argv[]) // функция поддержки разного кода
{
	srand(time(NULL)); // генератор псевдослучайных чисел
	setlocale(LC_ALL, "Russian"); // русская локализация 
	int arr[30];
	for (int i = 0; i < 30; i++) // заполнение и вывод всех эл-тов массива рандомными числами 50% которых отрицательные
	{
		arr[i] = rand() % 100 - 50;
		cout << " " << arr[i];
	}
	int s = 0;
	for (int i = 0; i < 30; i++)
	if (arr[i]>0)   
	{
		s = s + 1; 
		if (s == 3) // при нахождении трех первых положительных элементов массива
		{
			cout << endl;
			cout << " " << i + 1; // вывод следующих элементов за тремя найденными положительными элементами массива
		}
	}


	cin.get(); // окончание работы с потоками
	return 0;
}