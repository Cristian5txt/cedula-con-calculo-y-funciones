#include <iostream>
using namespace std;

void ingresar(string& apellido1, string& apellido2, string& nombre1, string& nombre2,
                           string& nacionalidad, string& dia, string& sexo,
                           string& lugar_nacimiento1, string& lugar_nacimiento2,
                           string& NUM, string& fecha_vencimiento, string& NUI,int& anio,int& mes);
void imprimir(const string& apellido1, const string& apellido2, const string& nombre1, const string& nombre2,
                   const string& nacionalidad, const string& dia, const string& sexo,
                   const string& lugar_nacimiento1, const string& lugar_nacimiento2,
                   const string& NUM, const string& fecha_vencimiento, const string& NUI,int& anio, int& resultado_resta,int& mes);

int restar(int a, int b);
int main() {

    string nombre1, nombre2, apellido1, apellido2, nacionalidad, dia,lugar_nacimiento1, lugar_nacimiento2, NUM, sexo, NUI, fecha_vencimiento;
    int x,y,resultado_resta,anio,mes;
    cout<< "INGRESE EL ANIO ACUTAL"<<endl;
    cin>>x;
    cout<< "INGRESE SU EDAD"<<endl;
    cin>>y;

    resultado_resta= restar(x,y);

    ingresar(apellido1, apellido2, nombre1, nombre2, nacionalidad, dia,sexo, lugar_nacimiento1, lugar_nacimiento2, NUM, fecha_vencimiento, NUI,anio,mes);

    imprimir(apellido1, apellido2, nombre1, nombre2, nacionalidad, dia,sexo, lugar_nacimiento1, lugar_nacimiento2, NUM, fecha_vencimiento, NUI,anio,resultado_resta,mes);

    return 0;
}
int restar(int a, int b){
int resta = a-b;
return resta;
}

void ingresar(string& apellido1, string& apellido2, string& nombre1, string& nombre2,
                           string& nacionalidad, string& dia, string& sexo,
                           string& lugar_nacimiento1, string& lugar_nacimiento2,
                           string& NUM, string& fecha_vencimiento, string& NUI,int& anio,int& mes) {
    cout << "Apellidos" << endl;
    cin >> apellido1;
    cin>> apellido2;

    cout << "Nombres" << endl;
    cin >> nombre1;
    cin>> nombre2;

    cout << "Nacionalidad" << endl;
    cin >> nacionalidad;

    cout << "Fecha de nacimiento" << endl;
    cin >> dia;
    cin>> mes;

    cout << "Sexo" << endl;
    cin >> sexo;

    cout << "Lugar de nacimiento" << endl;
    cin >> lugar_nacimiento1;
    cin>> lugar_nacimiento2;

    cout << "No Documento" << endl;
    cin >> NUM;

    cout << "Fecha de vencimiento" << endl;
    cin >> fecha_vencimiento;

    cout << "NUI" << endl;
    cin >> NUI;
}

void imprimir(const string& apellido1, const string& apellido2, const string& nombre1, const string& nombre2,
                   const string& nacionalidad, const string& dia, const string& sexo,
                   const string& lugar_nacimiento1, const string& lugar_nacimiento2,
                   const string& NUM, const string& fecha_vencimiento, const string& NUI,int& anio,int& resultado_resta,int& mes) {
    cout << "    " << endl;

    cout << "CEDULA DE" << " ***** " << "REPUBLICA DEL ECUADOR" << endl;
    cout << "IDENTIDAD" << " ***** " << "DIRECCION GENERAL DE REGISTRO CIVIL, IDENTIFICACION Y CEDULACION" << endl;

    cout << "APELLIDOS" << "        " << "CONDICON CIUDADANIA*NNA" << endl;
    cout << apellido1 << endl;
    cout << apellido2 << endl;

    cout << "NOMBRES" << endl;
    cout << nombre1 << endl;
    cout << nombre2 << endl;

    cout << "NACIONALIDAD" << endl;
    cout << nacionalidad << endl;

    cout << "FECHA DE NACIMIENTO" << "                        " << "SEXO" << endl;
    cout << dia <<"-"<<mes<<"-"<<resultado_resta <<"                                 " << sexo << endl;

    cout << "LUGAR DE NACIMIENTO" << "                        " << "No.DOCUMENTACION" << endl;
    cout << lugar_nacimiento1 << "                                  " << NUM << endl;
    cout << lugar_nacimiento2 << "                                 " << "FECHA DE VENCIMIENTO" << endl;

    cout << "                  FIRMA DEL TITULAR" << "        " << fecha_vencimiento << endl;
    cout << "NUI." << NUI << "    *******       " << endl;
}
