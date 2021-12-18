# Lecture-5-Exercises

#include <iostream>
#include <ctype.h>
#include <string>
using namespace std;


//Temperature conversion
        int main() {

          char type = 0;
          double temp = 0;
          string strInput;
          char szInput[16] = { 0 };

          cout << "Press 'f' to convert fahrenheit to celsius. Press 'c' to convert celsius to fahrenheit: "; cin >> type;

          switch (type) {
          case 'f':
          case 'F':
            cout << "You have choose fahrenheit to celsius, Enter the temperature: ";
            cin >> strInput;
            strcpy_s(szInput, strInput.c_str());

            if (isalpha(szInput[0])) {
              system("cls");
              cout << "INVALID" << endl;
            }
            else {
              temp = atof(szInput);
              cout << "in Fahrenheit: " << temp << endl;
              cout << "in Celsius: " << temp - 32 * 0.5556;
            }

            break;
          case 'c':
          case 'C':

            cout << "You have choose celsius to fahrenheit, Enter the temperature: "; cin >> strInput;
            strcpy_s(szInput, strInput.c_str());
            if (isalpha(szInput[0])) {
              system("cls");
              cout << "INVALID" << endl;

            }
            else {
              temp = atof(szInput);
              cout << "in Celsius: " << temp << endl;
              cout << "in Fahrenheit: " << (temp * 1.8)+32;
            }
            break;
          default:
            system("cls");
            cout << "INVALID INPUT" << endl;
            break;
          }


          return 0;
        }
