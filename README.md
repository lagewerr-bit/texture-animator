#include <iostream>
#include <Windows.h>
using namespace std;

int main() {
    setlocale(0, "");
    
    cout << "\x1b[92m*\x1b[0m Введите размер: ";
    int size;
    cin >> size;
    
    cout << "\x1b[92m*\x1b[0m Введите текстуру 1: ";
    char texture1;
    cin >> texture1;
    
    cout << "\x1b[92m*\x1b[0m Введите текстуру 2: ";
    char texture2;
    cin >> texture2;
    
    cout << "\x1b[92m*\x1b[0m Тип линии (0/1): ";
    short type;
    cin >> type;
    
    short i = 0;
    cout << endl;
    
    while (i < size) {
        Sleep(200);
        if (type == 0) {
            if (i % 2 == 0) {
                cout << "\x1b[94m " << texture1;
            } else {
                cout << "\x1b[94m " << texture2;
            }
        }
        else {
            if (i % 2 == 0) {
                cout << "\x1b[94m " << texture1 << endl;
            } else {
                cout << "\x1b[94m " << texture2 << endl;
            }
        }
        i++;
    }
    
    int _; cin >> _;
}
