# Lecture-5-Exercises
**//Biography**
                #include <iostream>
                #include <string>
                using namespace std;



                int main() {
                    string address;
                    string user;
                    int age;
                    cout << "Enter your name: ";
                    getline(cin, user);
                    cout << "\nEnter your address: ";
                    getline(cin, address);
                    cout << "\nEnter your age: "; cin >> age;
                    while (cin.fail()) {
                        cout << "Invalid input. Try again" << endl;
                        cin.clear();
                        cin.ignore();
                        cin >>age;
                    }
                    system("cls");
                    cout << "Your name is: " << user;
                    cout << "\n\nYour age is: " << age;
                    cout << "\n\nYour address is: " << address;
                        return 0;
                }

**//Temperature Conversion**
                #include <iostream>
                #include <ctype.h>
                #include <string>
                using namespace std;



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
  
  
**  //Circles**
          #include <iostream>
        #include <string>
        using namespace std;
        int main()
        {
            double radius, area, circumference;
            cout << "Enter the radius to calculate the area and circumference of the circle: "; cin >> radius;
        while (cin.fail()) {
            cout << "Invalid input. Try again" << endl;
            cin.clear();
            cin.ignore();
            cin >> radius;
        }
            area = 3.14 * radius * radius;
            circumference = 2 * 3.14 * radius;
            cout << "The area of the circle is: " << area << endl;
            cout << "The circumference  of the circle is: " << circumference << endl;
        }

