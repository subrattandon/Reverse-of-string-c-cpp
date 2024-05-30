#include <iostream>
using namespace std;

int main() {
    double num1, num2;
    char op;
    double result;  


    cout << "Enter first number: ";
    cin >> num1;
    cout << "Enter second number: ";
    cin >> num2;
    cout << "Enter operator (+, -, *, /, %): ";
    cin >> op;


    if (op == '+') {
        result = num1 + num2;
    } else if (op == '-') {
        result = num1 - num2;
    } else if (op == '*') {
        result = num1 * num2;
    } else if (op == '/') {
        if (num2 != 0) {
            result = num1 / num2;
        } else {
            cout << "Error! Division by zero." << endl;
            return 1; 
        }
    } else if (op == '%') {
        if (num2 != 0) {
            int int_num1 = num1;  
            int int_num2 = num2;  
            result = int_num1 % int_num2;
        } else {
            cout << "Error! Division by zero." << endl;
            return 1; 
        }
    } else {
        cout << "Invalid operator!" << endl;
        return 1; 
    }


    cout << "Result: " << result << endl;

    return 0;
}
