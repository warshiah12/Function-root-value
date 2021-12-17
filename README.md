# Function-root-value
#using functions to find the root value from 1-10
#include<iostream>
#include<math.h>
using namespace std;
void number(int root)  //function definition
{
	cout << "\n\t\t\t\t\tRoot value from 1-10 is given below " << endl;
	for (int j = 1; j <= 10; j++)   //using for loop to find the root value from 1 till 10
	{
		double number = 1.0 / j;
		double rootval = pow(root, number);
		cout << "\t\t\t\t\t" << j << " root value of " << root << " is : " << pow(root, number) << endl;
	}
	cout << "\n\t\t\t\t\tYOU HAVE REACHED THE END OF THE CODE\n\n";
}
int main()   //main function
{
	int userinput;   //declaring a variable 'userinput' with datatype integer
	cout << "\n\t\t\t\t\tEnter a number: ";
	cin >> userinput;
	while (cin.fail() != 0)  //if user enters any other character except for number then it will ask the user to enter the number again
	{
		cout << "\t\t\t\t\t\aInvalid Data.\n\t\t\t\t\tEnter number again ";
		cin.clear();
		cin.ignore();
		cin >> userinput;
	}
	number(userinput);  //function call
	return 0;
}
