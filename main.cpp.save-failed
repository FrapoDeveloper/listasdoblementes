#include <iostream>
#include <bits/stdc++.h>
using namespace std;

struct Nodo
{
    int dato;
    Nodo *sig;
    Nodo *ant;
};

typedef struct Nodo *Tlista;
typedef struct Nodo *pNodo;

Tlista lista = NULL;

void Imprimir(Tlista);
void Insertar(Tlista &);
void Final(Tlista &);

int main()
{
    int opc;
    while(1)
    {
        cout << "L I S T A S  D O B L E S" << endl
             << "1) Insertar al incio" << endl
             << "2) Insertar al final" << endl
             << "10) Salir" << endl
             << "Seleccione Opcion: ";
        do
        {
            cin >> opc;
        }while(opc < 1 && opc > 10);

        switch(opc)
        {
        case 1:
            Insertar(lista);
        break;

        case 2:
            Final(lista);
        break;

        case 10:
            exit(0);
        break;

        default:
            cout << "Opcion Invalida" << endl;
            system("pause");
            system("cls");
        break;
        }
    }
}

void Imprimir(Tlista lista)
{
    pNodo q = lista;

    while(q != NULL)
    {
        cout << q -> dato << " ";
        q = q -> sig;
    }

    cout << endl;
    system("pause");
    system("cls");
}

void Insertar(Tlista &lista)
{
    pNodo q = new struct Nodo ;
    int x;

    cout << "Introduce el dato: ";
        cin >> x;

    q -> dato = x;

    if(lista == NULL)
    {
        lista = q;
        q -> sig = NULL;
        q -> ant = NULL;
    }
    else
    {
        q -> sig = lista;
        q -> ant = lista -> ant;
        lista -> ant = q;
    }

    Imprimir(lista);
}

void Final(Tlista &lista)
{
    pNodo q = new struct Nodo ;
    int x;

    cout << "Introduce el dato: ";
        cin >> x;

    q -> dato = x;

    if(lista == NULL)
    {
        lista = q;
        q -> sig = NULL;
        q -> ant = NULL;
    }
    else
    {
        q -> sig = lista -> sig;
        lista -> sig = q;
        q -> ant = lista;
    }

    Imprimir(lista);
}

