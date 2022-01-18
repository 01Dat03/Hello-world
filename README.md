/*###Begin banned keyword - each of the following line if appear in code will raise error. regex supported
###End banned keyword*/

//###INSERT CODE HERE -
#include<iostream>
using namespace std;
#include<math.h>
#include<algorithm>

struct PhanSo{
    int numerator ;
    int denominator ; 
    
};
void check(PhanSo &x){
    if(x.numerator >0 && x.denominator >0 || x.numerator<0 && x.denominator<0){
        x.numerator = abs(x.numerator);   x.denominator = abs(x.denominator);

    }else if(x.numerator<0 || x.denominator<0){
         x.numerator = abs(x.numerator);   x.denominator = abs(x.denominator);
         x.numerator = -x.numerator; 
    }
}
void Nhap(PhanSo x){
    cin>>x.numerator;
    cin>>x.denominator; 
}
PhanSo Nhap(){
PhanSo x; cin>>x.numerator; cin>>x.denominator;
return x;
}
PhanSo Cong(PhanSo a,PhanSo b){
check(a); check(b) ;
PhanSo x ; 
x.numerator = a.numerator + b.numerator ;
x.denominator = a.denominator + b.denominator ;
check(x) ;
return x;
}
void Xuat(PhanSo x){
if(x.denominator==1){
 cout<<x.numerator;
 return ;
}
cout<<x.numerator<<"/"<<x.denominator; 
}
int main() {
    PhanSo a, b;
    Nhap(a);
    b = Nhap();
    Xuat(Cong(a, b));
    return 0;
}

