#include <iostream>
#include <vector>
using namespace std;

class Array {
private:
    vector<double> data;

public:
    // Конструктор класса Array, принимающий размерность массива
    Array(int size) : data(size) {}

    // Метод для заполнения массива элементами
    void fillArray() {
        for (int i = 0; i < data.size(); ++i) {
            cin >> data[i];
        }
    }

    // Метод для вывода элементов массива
    void printArray(const char* name) const {
        cout << name << "= ";
        for (double num : data) {
            cout << num << " ";
        }
        cout << endl;
    }

    // Перегрузка операторов для арифметических операций с массивами
    Array operator+(const Array& other) const {
        Array result(data.size());
        for (int i = 0; i < data.size(); ++i) {
            result.data[i] = data[i] + other.data[i];
        }
        return result;
    }

    Array operator-(const Array& other) const {
        Array result(data.size());
        for (int i = 0; i < data.size(); ++i) {
            result.data[i] = data[i] - other.data[i];
        }
        return result;
    }

    Array operator*(const Array& other) const {
        Array result(data.size());
        for (int i = 0; i < data.size(); ++i) {
            result.data[i] = data[i] * other.data[i];
        }
        return result;
    }

    Array operator/(const Array& other) const {
        Array result(data.size());
        for (int i = 0; i < data.size(); ++i) {
            if (other.data[i] != 0) {
                result.data[i] = data[i] / other.data[i];
            } else {
                cerr << "Ошибка: деление на ноль!" << endl;
                exit(1);
            }
        }
        return result;
    }

    Array operator*(double scalar) const {
        Array result(data.size());
        for (int i = 0; i < data.size(); ++i) {
            result.data[i] = data[i] * scalar;
        }
        return result;
    }

    // Перегрузка операторов для проверки равенства и неравенства массивов
    bool operator==(const Array& other) const {
        return data == other.data;
    }

    bool operator!=(const Array& other) const {
        return data != other.data;
    }
};

int main() {
    int size;
    //cout << "Введите размерность массивов: ";
    cin >> size;

    Array array1(size);
    Array array2(size);

    //cout << "Введите элементы массива 1:" << endl;
    array1.fillArray();

    //cout << "Введите элементы массива 2:" << endl;
    array2.fillArray();

    double scalar;
    //cout << "Введите скалярную величину: ";
    cin >> scalar;

    array1.printArray("massiv1");
    array2.printArray("massiv2");

    // Выполнение арифметических операций и вывод результатов
    Array sum = array1 + array2;
    sum.printArray("summa");

    Array diff = array1 - array2;
    diff.printArray("raznost");

    Array product = array1 * array2;
    product.printArray("proizv");

    Array division = array1 / array2;
    division.printArray("delenie");

    Array multScalar1 = array1 * scalar;
    multScalar1.printArray("mult chislo massiv1");

    Array multScalar2 = array2 * scalar;
    multScalar2.printArray("mult chislo massiv2");

    // Проверка на равенство и неравенство
    if (array1 == array2) {
        cout << "massivy ravny" << endl;
    } else {
        cout << "massivy ne ravny" << endl;
    }

    return 0;
}
