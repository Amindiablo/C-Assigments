#include <iostream>
#include <algorithm>
using namespace std;

double calculateAverage(int array[], int size) {
    int sum = 0;
    for (int i = 0; i < size; i++) {
        sum += array[i];
    }
    return static_cast<double>(sum) / size;
}

struct Person {
    string firstName;
    string lastName;
    int age;
};

int findMax(int array[], int size) {
    return *max_element(array, array + size);
}

int findMin(int array[], int size) {
    return *min_element(array, array + size);
}

int mod(int a, int b) {
    return a % b;
}

int main() {
    int numbers[] = {4, 10, 400, 2000, 0};
    int size = sizeof(numbers) / sizeof(numbers[0]);
    cout << "Average: " << calculateAverage(numbers, size) << "\n";
    
    Person people[] = {
        {"Reza", "Moghaddam", 25}, {"Sara", "Ahmadi", 30}, {"Ali", "Ranjbar", 22},
        {"Shayan", "Kazemi", 28}, {"Mina", "Sadeghi", 24}, {"Neda", "Rahimi", 35},
        {"Ailin", "Hosseini", 21}, {"Arian", "Jafari", 27}, {"Foad", "Moradi", 29},
        {"Rozhina", "Khanlari", 26}
    };
    int ages[10];
    for (int i = 0; i < 10; i++) ages[i] = people[i].age;
    cout << "Average Age: " << calculateAverage(ages, 10) << " Years Old\n";
    
    int randomNumbers[] = {44, 55, 68, 298, 43, 10, 2};
    int numSize = sizeof(randomNumbers) / sizeof(randomNumbers[0]);
    cout << "Biggest Number: " << findMax(randomNumbers, numSize) << "\n";
    cout << "Smallest Number: " << findMin(randomNumbers, numSize) << "\n";
    
    int a, b;
    cout << "Enter two numbers: ";
    cin >> a >> b;
    cout << "Modulus: " << mod(a, b) << "\n";
    
    return 0;
}
