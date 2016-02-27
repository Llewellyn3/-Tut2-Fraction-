# -Tut2-Fraction-
#include <iostream>
using namespace std;

struct fraction
{
    int numerator;
    int denominator;
}

frac1,frac2,frac3,frac4,frac5,frac6;

int inline gcd(int x, int y)
{
    int temp;

    while(y != 0)
    {
        temp = y;
        y = y % x;
        x = temp;
    }
    return x;
}

void Add()
{
    int n = (frac1.numerator * frac2.denominator) + (frac2.numerator * frac1.denominator);

    int d = (frac1.denominator * frac2.denominator);

    frac3.numerator = n / gcd(n, d);
    frac3.denominator = d / gcd(n, d);
}

void Subtract()
{
	int n= (frac1.numerator*frac2.denominator)-(frac2.numerator*frac1.denominator);
	
	int d=( frac1.denominator*frac2.denominator);
	
	frac4.numerator = n/gcd( n, d);
	frac4.denominator = d/gcd(n,d);
}

void Multiply() 
{   
	      
	int n = (frac1.numerator * frac2.numerator);     
	
	int d = (frac1.denominator * frac2.denominator); 
	
	frac5.numerator = n/gcd(n,d);
	frac5.denominator = d/gcd(n,d);
	
}

void Divide()
{
	int n = (frac1.numerator*frac2.denominator);

	int d = (frac1.denominator*frac2.numerator);
	
	frac6.numerator = n/gcd(n,d);
	frac6.denominator = d/gcd(n,d);
}

void Print()
{

	cout<<"The addition of fractions: "<<frac3.numerator<<"/"<<frac3.denominator;
  cout<<"The subtraction of fractions: "<<frac4.numerator<<"/"<<frac4.denominator;
	cout<<"The multiplication of fractions: "<<frac5.numerator<<"/"<<frac5.denominator;
	cout<<"The division of fractions: "<<frac6.numerator<<"/"<<frac6.denominator<<endl;
}


int main()
{
  cout<<"Please input the first numerator: ";
	cin>>frac1.numerator;

	cout<<"Please input the first denominator: ";
	cin>> frac1.denominator;


  cout<<"Please input the second numerator: ";
	cin>>frac2.numerator;

	cout<<"Please input the second denominator: ";
	cin>> frac2.denominator;
    
  Add();
	Subtract();
	Multiply();
	Divide();

	Print();

    
}
