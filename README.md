#include <iostream>
using namespace std;

// Función de ordenamiento burbuja
void burbuja(int arreglo[], int n) {
    for (int i = 0; i < n - 1; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            if (arreglo[j] > arreglo[j + 1]) {
                // Intercambiar elementos
                int temp = arreglo[j];
                arreglo[j] = arreglo[j + 1];
                arreglo[j + 1] = temp;
            }
        }
    }
}

// Función para imprimir el arreglo
void imprimirArreglo(int arreglo[], int n) {
    for (int i = 0; i < n; i++) {
        cout << arreglo[i] << " ";
    }
    cout << endl;
}

// Función principal con prueba del método burbuja
int main() {
    // Arreglo de prueba
    int datos[] = {64, 25, 12, 22, 11};
    int n = sizeof(datos) / sizeof(datos[0]);

    cout << "Arreglo original: ";
    imprimirArreglo(datos, n);

    // Llamar al algoritmo de burbuja
    burbuja(datos, n);

    cout << "Arreglo ordenado: ";
    imprimirArreglo(datos, n);

    return 0;
}
#include <iostream>

unsigned long long factorial(int n) {
    if (n == 0 || n == 1) {
        return 1;
    } else {
        return n * factorial(n - 1);
    }
}

int main() {
    int numero;

    // Solicitar al usuario que ingrese un número entero
    std::cout << "Ingrese un número entero para calcular su factorial: ";
    std::cin >> numero;

    // Calcular el factorial
    unsigned long long resultado = factorial(numero);

    // Mostrar el resultado
    std::cout << "El factorial de " << numero << " es: " << resultado << std::endl;

    return 0;
}
