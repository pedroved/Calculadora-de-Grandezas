#include<stdio.h>
#include<stdlib.h>
#include<iostream>
#include<string>
#include<cmath>

using namespace std;

int main(){
	
	int num ; 
	
	float t, r, i, p;
	cout << "Digite 1 para calcular a tensao:\n";
	cout << "Digite 2 para calcular a Resistencia:\n";
	cout << "Digite 3 para calcular a Intencidade:\n";
	cout << "Digite 4 para calcular a Potencia: \n";
	cin >> num;
	
	
	system("CLS");
	
	switch (num){
		case 1:{
			cout << "CACULANDO A TENSAO: \n";
			cout << "digite o valor de resistencia, caso nao saiba digete 0: \n";
			cin >> r;
			if(r == 0){
				cout<< "digite o valor da potencia: ";
				cin >> p;
				cout << "digite o valor da intensidade";
				cin >> i;
				t = p/i;
				cout << "o valor da tensao eh: " << t;
		}else{
			cout << "digite o valor da intensidade, caso não saiba, digite 0: ";
			cin >> i;
			if(i == 0){
			
			cout << "Digite o valor de Potencia: ";
			cin >> p;
			t = sqrt(p * r);
			cout << "o valor da tensao eh: " << t;
		}else{
			cout << "o valor da tensao eh: ";
			t = r * i;
			cout << t;
		}
		}
		break;
			}
			
		
	
		case 2:{
			cout << "CACULANDO A RESISTENCIA: \n";
			cout << "digite o valor de tensao, caso nao saiba digete 0: \n";
			cin >> t;
			if(t == 0){
				cout<< "digite o valor da potencia: ";
				cin >> p;
				cout << "digite o valor da intensidade";
				cin >> i;
				r = p/(i*i);
				cout << "o valor da tensao eh: " << r;
		}else{
			cout << "digite o valor da intensidade, caso não saiba, digite 0: ";
			cin >> i;
			if(i == 0){
			cout << "Digite o valor da potencia: ";
			cin >> p;
			r = (t * t)/p;
			cout << "o valor da resistencia eh: " << r;
		}else{
			cout << "o valor da resistencia eh: ";
			r = t/i;
			cout << r;
		}
		}
			break;
		}
		
		case 3:{
			cout << "CACULANDO A INTENSIDADE: \n";
			cout << "digite o valor de tensao, caso nao saiba digete 0: \n";
			cin >> t;
			if(t == 0){
				cout<< "digite o valor da potencia: ";
				cin >> p;
				cout << "digite o valor da resistencia";
				cin >> r;
				i = sqrt (p/r);
				cout << "o valor da tensao eh: " << i;
		}else{
			cout << "digite o valor da potencia, caso não saiba, digite 0: ";
			cin >> p;
			if(p == 0){
			cout << "Digite o valor de resistencia: ";
			cin >> r;
			i = t/r;
			cout << "o valor da tensao eh: " << i;
		}else{
			cout << "o valor da tensao eh: ";
			i = t/p;
			cout << i;
		}
		}
		break;
	}
	case 4:{
			cout << "CACULANDO A POTENCIA: \n";
			cout << "digite o valor de tensao, caso nao saiba digete 0: \n";
			cin >> t;
			if(t == 0){
				cout<< "digite o valor da resistencia: ";
				cin >> r;
				cout << "digite o valor da intensidade";
				cin >> i;
				p = r/(i*i);
				cout << "o valor da tensao eh: " << p;
		}else{
			cout << "digite o valor da intensidade, caso não saiba, digite 0: ";
			cin >> p;
			if(p == 0){
			cout << "Digite o valor de resistencia: ";
			cin >> r;
			p = (t*t)/r;
			cout << "o valor da tensao eh: " << p;
		}else{
			cout << "o valor da tensao eh: ";
			p = t*i;
			cout << p;
		}
		}
		break;
}
}

}
