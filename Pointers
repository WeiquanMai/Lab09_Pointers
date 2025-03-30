/*
CSC237- C++ 
Project Name: Pointers
Student: Weiquan Mai
Date: February 28, 2025
Due Date: March 5, 2025
Description: This program asks user for an integer, and then dynamically allocates an array for that size.
Program then asks user to populate the array, finds the maximum integer entered into the array, and displays the maximum integer.
*/

#include <iostream>
#include <iomanip>

using namespace std;

// Function Prototypes
void populateIntegerArray(int* arrayPtr, int arraySize);
void displayIntegerArray(int* arrayPtr, int arraySize);
int findMaximumInteger(int* arrayPtr, int arraySize);

int main()
{
	// Variables
	int arraySize;
	int* arrayPtr;
	int maxInt = 0;

	// Ask user for input
	cout << "Enter desired array size: ";
	cin >> arraySize;
	
	// Dyamically allocate memory to create desired array
	arrayPtr = new int[arraySize];
	cout << "arrayPtr = " << arrayPtr << endl;
	
	// Call function prototypes
	populateIntegerArray(arrayPtr, arraySize);
	displayIntegerArray(arrayPtr, arraySize);
	maxInt = findMaximumInteger(arrayPtr, arraySize);
	
	// Display maxInt
	cout << "Maximum integer in array is: " << maxInt << endl;

	// Release dynamic memory
	cout << "DELETING array at arrayPtr = " << arrayPtr << endl;
	delete[] arrayPtr;

	// Exit program
	cout << "Exit the program.";
	return 0;
} // End of function main

// Function to ask for user input to populate created array
void populateIntegerArray(int* arrayPtr, int arraySize)
{
	for (int i = 0; i < arraySize; i++)
	{
		cout << "Enter value for array element " << i << ": ";
		cin >> *(arrayPtr + i);
	}
} // End of function populateIntegerArray

// Function to display data collected in populated array
void displayIntegerArray(int* arrayPtr, int arraySize)
{
	int fieldWidth = 30;
	// Display column headings
	cout << "Array Address" << setw(fieldWidth) << "Array Element in Decimal" << setw(fieldWidth) << "Array Element in Hex" << endl;
	cout << "_____________" << setw(fieldWidth) << "________________________" << setw(fieldWidth) << "____________________" << endl;

	// for loop to display results
	for (int i = 0; i < arraySize; i++)
	{
		cout << (arrayPtr + i) << ":  "  
		 << "arrayPtr[" << i << "] = " << setw(12) << arrayPtr[i]
		 << setw(12) << "(Hex " << hex << uppercase << setfill('0') << setw(8) << arrayPtr[i] << ")" << endl;

		//Reset fill character to space and output to decimal
		cout << setfill(' ');
		cout << dec;
	}
} // End of function displayIntegerArray

// Function to find maximum integer in populated array and return maximum integer to main
int findMaximumInteger(int* arrayPtr, int arraySize)
{
	int largestSoFar = *(arrayPtr);

	// for loop to determine largest number in array
	for (int i = 1; i < arraySize; i++)
	{
		if (arrayPtr[i] > largestSoFar)
		{
			largestSoFar = arrayPtr[i];
		}
	}

	return largestSoFar;
} // End of function findMaximumInteger
