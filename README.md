# Nodos-a-pila
Tarea de programación.

//============================================================================
// Name        : nodostarea.cpp
// Author      : stephanie chamo
// Version     :
// Copyright   : Your copyright notice
// Description : Hello World in C++, Ansi-style
//============================================================================

#include <iostream>
#include <stdio.h>
#include <stdlib.h>
using namespace std;

struct Nodo{
	int informacion;
	struct Nodo *siguiente;
};

int main (){
	struct Nodo *tope;
	struct Nodo *nuevo;
	tope=NULL;

	int dato;
	int cantidad;
	int i=0;

	cout <<"Ingrese la cantidad de nodos:" << endl;
	cin >> cantidad;

	while (i<=cantidad){
		nuevo = (struct Nodo *) malloc (sizeof (struct Nodo));
		nuevo->siguiente=tope;

		cout << "Ingrese el dato: " << endl;
		cin >> dato;


		nuevo->informacion=dato;
		tope=nuevo;
		i++;
	}

	while (nuevo!=NULL){
		cout << nuevo->informacion << endl;
		nuevo = nuevo->siguiente;
	}
	return 0;
}
