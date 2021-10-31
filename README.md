# -implementation-from-scratch
manual implementation of Array Based List
#include<iostream>
#include <algorithm> 
#include <unordered_map>
#include <vector>
#include <stack>
#include <queue>
#include <deque>
#include<string>
#include <set> 
#include <map> 
#include <cmath>
#include <valarray>
using namespace std;
class arraylist {
	int* arr;
	int maxsize, length;
public:
	arraylist(int s)
	{
		if (s < 0)		maxsize = 0;
		else	maxsize = s;
		length = 0;
		arr = new int[maxsize];

	}
	bool isempty()
	{
		return length == 0;
	}
	bool isfull()
	{
		return length == maxsize;
	}

	int getsize()
	{
		return length;
	}
	void print()
	{
		for (int i = 0; i < length; i++)
		{
			cout << arr[i] << endl;
		}
	}

	void insertat(int pos, int item)
	{
		if (isfull())
			cout << "the list is full";
		else if (pos<0 || pos>maxsize)
			cout << "out of the range";
		else
		{
			for (int i = length; i >= pos; i--)
			{
				arr[i] = arr[i - 1];
				arr[pos] = item;
				length++;

			}
		}
	}







};
int main()
{
	
	
	return 0;
}

