# horas-trabajadas
#include <iostream>
using namespace std;
int segundos(int h,int m,int s);
void trabajo(int seg);
int main()
{
int entradah,entradam,salidah,salidam,entradas,salidas,s1,s2,r;
cout<<"hora de entrada:(24hrs.)";
cin>>entradah;
cout<<"minutos de entrada:(24hrs.)";
cin>>entradam;
cout<<"segundos de entrada:(24hrs.)";
cin>>entradas;
cout<<"hora de salida:(h,m,s)";
cin>>salidah;
cout<<"minuto de salida:(h,m,s)";
cin>>salidam;
cout<<"segundo de salida:(h,m,s)";
cin>>salidas;
s1=segundos(entradah,entradam,entradas);
s2=segundos(salidah,salidam,salidas);
r=s2-s1;
if(r<0)
{
	r+=86400;
	trabajo(r);
}
else
trabajo(r);
return 0;
}
int segundos(int h,int m,int s)
{
    int z;
    h*=3600;
    m*=60;
    s+=(h+m);
    return s;
}
void trabajo(int seg)
{
    int h,m;
    h=seg/3600;
    seg%=3600;
    m=seg/60;
    seg%=60;
    cout<<h<<":"<<m<<":"<<seg;
}
