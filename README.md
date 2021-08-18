# C++-file-
In this file there are lot of programming of c++ language with there output. In which also attached with output. 
PRACTICAL 1:- WAP to print the sum and product of digits of an integer.
SOLUTION:-
#include <iostream>
using namespace std; 
int main()
{ 
int num,sum=0,product=1,i;
 cout<<"enter the number\n";
 cin>>num;
 while(num>0)
 {
  sum=sum+num%10;
  product=product*(num%10);
   num=num/10;
 }
 cout<<"sum of integer="<<sum<<" and product="<<product;
}





 
PRACTICAL 2:- Write a program to reverse a number.
SOLUTION:- 
#include <iostream> 
using namespace std; 
int main() 
{ 
  int n, reversedNumber = 0,remainder;
  cout << "Enter an integer: "; 
  cin >> n;
  while(n != 0)
   {
    remainder = n%10;
    reversedNumber = reversedNumber*10 + remainder;
    n = n/10; 
   } 
   cout << "Reversed Number : " << reversedNumber; 
   return 0; 
}





 
PRACTICAL 3:- WAP to compute the sum of the first n terms of the following series S = 1+1/2+1/3+1/4+…… 

SOLUTION:- 

#include <iostream>
using namespace std;
 
int main()
{
  int n;
  float sum=0.0,i;
  cout<<"enter the value of n\n";
  cin>>n;
  
  for(i = 1; i <= n; i++)
  {
   sum= sum +(1/i);
  }
  cout<<"The sum of series till "<<n<<" is "<<sum;
  return 0;
}











PRACTICAL 4:- WAP to compute the sum of the first n terms of the following series S =1-2+3-4+5…………….
SOLUTION:-
#include <iostream> 
using namespace std; 
int sum(int n) 
{ 
    if (n % 2 == 1) 
    return (n + 1) / 2; 
    else
    return -n / 2; 
} 
int main() 
{ 
    int n; 
    cout<<"Enter the number : ";
	cin>>n;  
    cout <<sum(n);   
    return 0; 
}






 
PRACTICAL 5:-Write a function that checks whether a given string is Palindrome or not.
Use this function to find whether the string entered by the user is Palindrome or not.

SOLUTION:-

#include<iostream>
#include"cstring"
using namespace std;
void palindrome()
{
	char s[30];
	int i,n,c=0;
	cout<<"enter the string\n";
	gets(s);
	n=strlen(s);
	for(i=0;i<=n/2;i++)
	{
		if(s[i]==s[n-i-1])
		c++;
    }
		if(c==i)
		cout<<"string is palindrome"<<endl;
		else
		cout<<"string is not palindrome"<<endl;
}
int main()
{
  palindrome();	
}







 
PRACTICAL 6:- Write a function to find whether a given no. is prime or not.
Use the same to generate the prime numbers less than 100.

SOLUTION:-

#include <iostream>
using namespace std;
int main()
{
	int num,count=0;
	cout<<"enter the number to find out it is prime or not\n";
	cin>>num;
	for(int i=2;i<num;i++)
	{
    	if(num%i==0)
    	count++;
	}
	if(count==0)
	cout<<num<<" is prime number";
	else
	cout<<num<<" is non-prime number";
	cout<<"\nprime numbers less than 100 are\n";
    
	for(int i=2;i<=100;i++)
	{
    	count=0;
	for(int j=2;j<i;j++)
	{
    	if(i%j==0)
    	count++;
	}
	if(count==0)
	cout<<i<<"\n";
	}
}



 










PRACTICAL 7:- WAP to compute the factors of a given number.
SOLUTION:- 
#include <iostream>
using namespace std; 
int main()
{
	int n, i;
	cout << "Enter a integer: ";
	cin >> n;
	cout << "Factors of " << n << " are: " << endl;  
	for(i = 1; i <= n; i++)
	{
    	if(n % i == 0)
        	cout << i << endl;
	}
	return 0;
}







 
PRACTICAL 8:- Write a macro that swaps two numbers. WAP to use it.
SOLUTION:- 

#include <iostream>
#define SWAP(x,y){int temp; temp=x; x=y; y=temp;}
using namespace std;
int main()
{
  int a,b;
 cout<<"Enter the two numbers : "<<endl;
  cin>>a>>b;
  SWAP(a,b);
  cout<<"After swapping the value of a="<<a<<" and b="<<b<<endl;
  return 0;
}







 








PRACTICAL 9:- WAP to perform following actions on an array entered by the user: i) Print the even-valued elements ii) Print the odd-valued elements iii) Calculate and print the sum and average of the elements of array iv) Print the maximum and minimum element of array v) Remove the duplicates from the array vi) Print the array in reverse order The program should present a menu to the user and ask for one of the options. The menu should also include options to re-enter the array and to quit the program.

SOLUTION:- 
#include <iostream>
using namespace std;
 
int main()
{
	int arr[6],n;
	char ch;
    
    
do
{
	cout<<"enter the array elements\n";
	for(int i=0;i<6;i++)
	cin>>arr[i];
 
cout<<"select from the following menu options\n1) Print the even-valued elements\n2) Print the odd-valued elements\n3) Calculate and print the sum and average of the elements of array\n4) Print the maximum and minimum element of array\n5) Remove the duplicates from the array\n6) Print the array in reverse order\n";
cin>>n;
switch(n)
{
case 1:
{
cout<<"the even valued elements are\n";
for(int i=0;i<6;i++)
{
if(arr[i]%2==0)
cout<<arr[i]<<"\n";
}
break;
}
case 2:
{
	cout<<"the odd valued elements are\n";
for(int i=0;i<6;i++)
{
if(arr[i]%2!=0)
cout<<arr[i]<<"\n";
}
break;
}
case 3:
{
	int sum=0;
	for(int i=0;i<6;i++)
 	sum=sum+arr[i];
 	float avg=(float)sum/6;
	cout<<"\nSum="<<sum;
	cout<<"\tAvg="<<avg;
break;
}
case 4:
{
int max=arr[0],min=arr[0];
 for(int i=0;i<6;i++)
 {
 	if(max<arr[i])
 	max=arr[i];
 	if(min>arr[i])
 	min=arr[i];
 }
 cout<<"The maximum element is="<<max;
 cout<<"\nThe minimum element is="<<min;
 
break;
}
case 5:
{
   int n=6,i;
   cout<<"Removing duplicates";
	for( i=0;i<n;++i)
   	 for(int j=i+1;j<n;)
   	 {
   		 if(arr[i]==arr[j])
   		 {
   			 for(int k=j;k<n-1;++k)
   				 arr[k]=arr[k+1];
   				 
   			 --n;
   		 }
   		 else
   			 ++j;
   	 }
    
    for(i=0;i<n;++i)
    cout<<endl<<arr[i];
break;
}
case 6:
{
	cout<<"\narray in reverse order\n";
	for(int i=5;i>=0;i--)
	cout<<arr[i]<<endl;
break;
}
default:
cout<<"Invalid option";
break;
 
 
}
cout<<"Do you want to continue(y/n)\n";
 cin>>ch;
 
}while(ch=='y');
return 0;
}






 
 
PRACTICAL 10:- WAP that prints a table indicating the number of occurrences of each alphabet in the text entered as command line argument.
SOLUTION:- 
#include<iostream>
#include <string.h>
#include <ctype.h>
using namespace std;
struct detail
{
	char c;
	int freq;
};

int main()
{
	struct detail s[26];
	char string[100], c;
	int i = 0, index;

	for (i = 0; i< 26; i++)
	{
	s[i].c = i + 'a';
	s[i].freq = 0;
	}
	cout<<"Enter string: ";
	i = 0;
	do
	{
	//fflush(stdin);
	c = getchar();
	string[i++] = c;
	if (c == '\n')
	{
	break;
	}
	   c = tolower(c);
	index = c - 'a';
	s[index].freq++;
	} while (1);
	string[i - 1] = '\0';
cout<<"The string entered is:\n"<<string;

	cout<<"*************************\nCharacter\tFrequency\n*************************\n";
	for (i = 0; i< 26; i++)
	{
	if (s[i].freq)
	{
	cout<<s[i].c<<"\t\t"<<s[i].freq<<endl;
	}
	}

	return 0;
}




 















PRACTICAL 11:- Write a program that swaps two numbers using pointers.
SOLUTION:- 
#include <iostream> 
using namespace std; 
void swap(int *a, int *b) {
  int temp; 
  temp = *a;
  *a = *b;
  *b = temp;
}
 
int main() {
 
  int a=5,b=6;
 
  cout << "Before swapping\t  a="<<a<<"\tb="<<b;
 
  swap(&a, &b);
 
 cout << "\nAfter Swapping    a="<<a<<"\tb="<<b;
 
  return 0;
 
}









 
PRACTICAL 12:- Write a program in which a function is passed an address of two variables and then alter its contents.

SOLUTION:-

#include<iostream>
 
 using namespace std;
 
 void call_by_address(int *x,int *y)
 
 {
 
 int z=*x;
 
 *x=*y;
 
 *y=z;
 
 }
 
 int main()
 
 {
 
 int a=15, b=16;
 
 cout<<"before swapping\n"<<"a: "<<a<<"\nb: "<<b;
 
 call_by_address(&a, &b);
 
 cout<<"\nafter swapping\n"<<"a: "<<a<<"\nb: "<<b;
 
}







 
PRACTICAL 13:- Write a program which takes the radius of a circle as input from the user, passes it to another function that computes the area and the circumference of the circle and displays the value of area and circumference from the main () function.

SOLUTION:-

#include<iostream>
 
 using namespace std;
 
 #define pi 3.14
 
 class area
 
 {
 
 int r;
 
 float area1,cir;
 
 public:
 
 void getdata()
 
 {
 
 cout<<"enter the radius\n";
 
 cin>>r;
calculate_area(r);
calculate_circumference(r);
 }
 
 void calculate_area(int r)
 
 {
 
 area1=pi*r*r;
 
 cout<<"The area of circle="<<area1<<endl;
 }
void calculate_circumference(int r)
{
 cir=2*pi*r;
 
 cout<<"The circumference of circle="<<cir<<endl;
 
}
 
 
 };
 
 int main()
 
 {
 
 area a1;
 
 a1.getdata();
 
 
 }
  




 


PRACTICAL 14:- Write a program to find sum of n elements entered by the user. To write this program, allocate memory dynamically using new or delete operator.

SOLUTION:- 

#include<iostream> 
using namespace std; 
int main()
{ 
int n,*p;
cout<<"Enter array size:";
cin>>n;
p=new int[n];
cout<<"Enter list of integers"<<endl;
for(int i=0;i<n;i++)
cin>>p[i];
int s=0; 
for( int i=0;i<n;i++) 
s=s+p[i]; 
cout<<"Sum of array elements is\n"; 
cout<<s;
delete [ ]p;
return 0;
}





 
PRACTICAL 15:- .  Write a menu driven program to perform following operations on strings: a) Show address of each character in string b) Concatenate two strings without using strcat function. c) Concatenate two strings using strcat function. d) Compare two strings e) Calculate length of the string (use pointers) f) Convert all lowercase characters to uppercase g) Convert all uppercase characters to lowercase h) calculate no. of vowels in the string i) reverse the string

SOLUTION:-

#include<iostream>
using namespace std;
#include<string.h>
int main()
{
   int c;
   char ch;
 do
 {
   cout<<"\n";
   cout<<"select what do you want : "<<endl;
   cout<<"1.show address of each character in string\n";
   cout<<"2.concatenate two strings without using strcat function\n";
   cout<<"3.concatenate two strings with using strcat function\n";
   cout<<"4.compare two strings\n";
   cout<<"5.calculate lenght of string(use pointers)\n";
   cout<<"6.convert all lowercse character in uppercase\n";
   cout<<"7.convert all uppercase character in lowercase\n";
   cout<<"8.calculate no. of vowels in the string\n";
   cout<<"9.reverse the string\n";
   cin>>c;
   switch(c)
   {
   	case 1:
   	{
   	int i;
   	char name[10],*p;
   	cout<<"enter the string\n";
   	cin>>ws;
   	gets(name);
   	p=name;
   	while(*p!='\0')
   	{
   	cout<<"The address of "<<name[i]<<" is "<<&p<<endl;
   	i++;
   	p++;
    }  			
	}
	break;	
   	case 2:
   	{
	string name,name2,result;
	cout<<"enter the string"<<endl;
	cin>>ws;
	getline(cin,name);	
	cout<<"enter the string 2"<<endl;
	cin>>ws;
    getline(cin,name2);
	result=name+name2;
	cout<<"string after concatenating :"<<result;
	break;
    }
	case 3:
	{
    char string1[40],string2[40];
	cout<<"enter the string1:"<<endl;
	cin>>ws;
	gets(string1);
	cout<<"enter the string2:"<<endl;
	cin>>ws;
	gets(string2);
	strcat(string1,string2);
	cout<<"value of string1 after concatenation:"<<string1;
    break; 
    }
    case 4:
    {
    char string1[50], string2[50];
	cout<<"enter the string1:"<<endl;
	cin>>ws;
	gets(string1);
	cout<<"enter the string2:"<<endl;
	cin>>ws;
	gets(string2);
	if(strcmp(string1,string2)==0)
	{
		cout<<"both are same";
	}
	else
	{
		cout<<"both are different";
	}
    break;
    }
    case 5:
    {
    int co=0;
	char str[40],*p;
	cout<<"enter the string"<<endl;
	cin>>ws;
	gets(str);
	p=str;
	while(*p!='\0')
	{
		co++;
		p++;
	}
	cout<<"length of string is: "<<co;
	break;
    }
    case 6:
    {
    char str[100],upp[100];
    int i=0,j=0;
	cout<<"enter the string in lowercase"<<endl;
	cin>>ws;
    gets(str);
	while(str[i]!='\0')
	{
		if(str[i]>='a'&&str[i]<='z')
		upp[j]=str[i]-32;
		else
		upp[j]=str[i];
		i++;
		j++;
	}
	upp[j]='\0';
	cout<<"The string converted to uppercase:";
	puts(upp);
    break;  
    }
    case 7:
    {
    char str[30],lower[30];
    int i=0,j=0;
    cout<<"enter the string in uppercase"<<endl;
    cin>>ws;
    gets(str);
    while(str[i]!=0)
    {
   	 if(str[i]>='A'&&str[i]<='Z')
   	 lower[j]=str[i]+32;
   	 else
   	 lower[i]=str[j];
   	 i++;
   	 j++;
    }
    lower[i]='\0';
    cout<<"the string in lowercase: ";
    puts(lower);
    break;
    }
    case 8:
   	{
    int vowels=0,consonants=0,i;
	char ch[50];
	cout<<"enter the string1"<<endl;
	cin>>ws;
	gets(ch);
	for(i=0;ch[i]!='\0';i++)
	{
	    if(ch[i]=='a' ||ch[i]=='e' ||ch[i]=='i' ||
		   ch[i]=='o' ||ch[i]=='u' ||ch[i]=='A' ||
		   ch[i]=='E' ||ch[i]=='I' ||ch[i]=='O' ||
		   ch[i]=='U')
	      vowels++;	
     	else if((ch[i]>='a'&& ch[i]<='z') || (ch[i]>='A'&& ch[i]<='Z'))
     	  consonants++;
    }
     	cout<<"total no. of vowels="<<vowels;
    break;
    }
    case 9:
  	{
    char str[40];
	cout<<"enter the string"<<endl;
	cin>>ws;
	gets(str);
	strrev(str);
	cout<<"reversed string: "<<str;
    break; 
	}
    default:
    cout<<"invalid number"<<endl;
    break;
    }
    cout<<"\n\ndo you want to continue(y/n)\n";
    cin>>ch;
  }while(ch=='y');
}
 

OUTPUT:-
 

 
PRACTICAL 16:- Given two ordered arrays of integers ,write a program to merge the two-arrays to get an ordered array.

SOLUTION:-

#include<iostream>
using namespace std;
int main ()
{
  int a[5], b[5], c[10];
  cout << "Enter the array A\n";
  for (int i = 0; i < 5; i++)
   cin>>a[i]; 
cout<<"Enter the array B\n";
    for(int i=0;i<5;i++)
    cin>>b[i];
    for(int i=0,j=5;i<5,j<10;i++,j++)
    {
    c[i]=a[i];
    c[j]=b[i];
    }
    cout<<"The sorted individual array is\n";
    for(int i=0;i<10;i++)
for(int j=i+1;j<10;j++)
{
    int temp;
    if(c[i]>c[j])
    {
     temp=c[i];
     c[i]=c[j];
     c[j]=temp;
    }
}
for(int i=0;i<10;i++)
cout<<c[i]<<endl;
return 0;
}


 











PRACTICAL 17:- WAP to calculate Factorial of a number (i)using recursion, (ii) using iteration.

SOLUTION:- 

#include<iostream>
using namespace std;
void factorial_using_iteration();
int fact(int);
int main()
{
	int number,factorial;
	cout<<"************FACTORIAL USING RECURSION*****************************\n";
	cout<<"\nenter the number whose factorial do you want\n";
	cin>>number;
	factorial=fact(number);
	cout<<"The factorial of "<<number <<" is: "<<factorial<<endl;
	cout<<"\n*******FACTORIAL USING ITERATION*******************************\n\n";
    factorial_using_iteration();	
}
void factorial_using_iteration()
{
	int number,factorial=1;
	cout<<"enter the number whose factorial do you want\n";
	cin>>number;
	for(int i=1;i<=number;i++)
	{
		factorial=factorial*i;
	}
	cout<<"The factorial of "<<number<<" is: "<<factorial;
}
int fact(int number)
{
	if(number==1)
	return 1;
	else
	return (number*fact(number-1));
}






 















PRACTICAL 18:- WAP to calculate GCD of two numbers (i) with recursion (ii) without recursion.

SOLUTION:-
#include <iostream>
using namespace std;
 
int GCDfunc(int a, int b){
   while(a != b){
       if(a>b){
           return GCDfunc(a-b, b);
       }
       else{
           return GCDfunc(a, b-a);
       }
   }
   return a;
}
 
int main()
{
   int num1, num2, x,y,i, gcd;
   cout<<"Enter number1 and number2 : "<<endl;
   cin>>num1>>num2;
   cout<<"RECURSION METHOD :"<<endl;
   gcd = GCDfunc(num1, num2);
   cout<<"The GCD of "<<num1<<" and "<<num2<<" is "<<gcd<<endl;
   cout<<"ITERATION METHOD"<<endl;
   for(i=1; i<=num1 && i<=num2; i++){
       if(num1%i==0 && num2%i==0){
           gcd = i;
       }
   }
 
   cout<<"GCD of "<<num1<<" and "<<num2<<" is "<<gcd;
   return 0;
}




 









PRACTICAL 19:- Write a menu driven program to perform following operations on matrix.(a )sum, (b) difference, (c) product, (d)transpose.
SOLUTION:- 
#include<iostream>
using namespace std;
void addition(int a[2][2],int ar[2][2]);
void subtraction(int a[2][2],int ar[2][2]);
void multiplication(int a[2][2],int ar[2][2]);
void transpose(int a[2][2]);
int main()
{
	int a[2][2],ar[2][2];
	cout<<"enter the elements of the first matrix"<<endl;
	for(int i=0;i<2;i++)
	{
	for(int j=0;j<2;j++)
	{
		cin>>a[i][j];
	}
		cout<<"\n";	
	}
	cout<<"enter the elements of the second matrix"<<endl;
	for(int i=0;i<2;i++)
	{
	for(int j=0;j<2;j++)
	{
		cin>>ar[i][j];
	}
		cout<<"\n";	
	}
    cout<<"The addition of  two matrices is :"<<endl;
    addition(a,ar);
    cout<<"The subtraction of  two matrices is :"<<endl;
    subtraction(a,ar);
    cout<<"The multiplication of  two matrices is :"<<endl;
    multiplication(a,ar);
    cout<<"The transpose of  FIRST matrix is :"<<endl;
    transpose(a);
}
void addition(int a[2][2],int ar[2][2])
{
	int c[2][2];
	for(int i=0;i<2;i++)
	{
		for(int j=0;j<2;j++)
		{
			c[i][j]=a[i][j]+ar[i][j];
		}
		cout<<"\n";
	}
	for(int i=0;i<2;i++)
	{
		for(int j=0;j<2;j++)
		{
			cout<<" "<<c[i][j];
		}
		cout<<"\n";
	}
}
void subtraction(int a[2][2],int ar[2][2])
{
	int c[2][2];
	for(int i=0;i<2;i++)
	{
		for(int j=0;j<2;j++)
		{
			c[i][j]=a[i][j]-ar[i][j];
		}
		cout<<"\n";
	}
	for(int i=0;i<2;i++)
	{
		for(int j=0;j<2;j++)
		{
			cout<<" "<<c[i][j];
		}
		cout<<"\n";
	}
}
void multiplication(int a[2][2],int ar[2][2])
{
	int c[2][2],k;
	for(int i=0;i<2;i++)
	{
		for(int j=0;j<2;j++)
		{
			c[i][j]=0;
			for(k=0;k<2;k++)
			c[i][j]=c[i][j]+a[i][k]*ar[k][j];
	    }
	    cout<<"\n";
	    }
	    for(int i=0;i<2;i++)
	    {
	    	for(int j=0;j<2;j++)
	    	{
	    		cout<<" "<<c[i][j];
			}
			cout<<"\n";
		}
}
void transpose(int a[2][2])
{
	int tr[2][2];
	for(int i=0;i<2;i++)
	{
		for(int j=0;j<2;j++){
			tr[i][j]=a[j][i];
		}
	}
	for(int i=0;i<2;i++)
	{
		cout<<"\n";
		for(int j=0;j<2;j++){
			cout<<" "<<tr[i][j];
		}
	}
}


 







PRACTICAL 20:- create a person class create some objects of this class. Inherit the class person to create two class teacher and student. Maintain the respective information in classes and create , display and delete objects of these two objects (use runtime polymorphism)
SOLUTION:-
#include<iostream>
using namespace std;
class person
{
	protected:
	char name[30];
	int id;
};
class teacher:public person
{
	public:
	virtual void getinfo()
	{
		cout<<"enter the name of the teacher\n";
		cin.get(name,30);
		cout<<"enter the id of the teacher\n";
		cin>>id;
	}
	virtual void display()
	{
		cout<<"The name of teacher is "<<name<<endl;
		cout<<"The ID of the teacher is"<<id<<endl;
	}
};
class student:public person
{
	public:
	void getinfo()
	{
		cout<<"enter the name of the student\n";
		cin>>ws;
		cin.get(name,30);
		cout<<"enter the id of the student\n";
		cin>>id;
	}
	void display()
	{
		cout<<"The name of student is "<<name<<endl;
		cout<<"The ID of the student is"<<id<<endl;
	}
};
int main()
{
	teacher*ptr;
	teacher t;
	student*pt;
	student s;
	ptr=&t;
	ptr->getinfo();
	pt=&s;
	pt->getinfo();
	cout<<"\nDISPLAYING INFORMATION\n\n";
	cout<<"\nTEACHER INFORMATION\n\n";
	ptr->display();
	cout<<"\nSTUDENT INFORMATION\n\n";
	pt->display();
	delete[]ptr;
	delete[]pt;
}





 





PRACTICAL 21:- Create a class triangle. Include overloaded functions to calculating area. overload assignment operator and equality operators.
SOLUTION:-
#include <iostream>
#include <cmath>
using namespace std;
class Triangle
{
private:
float a,b,c,h;
public:
Triangle(){}
Triangle(float a,float b,float c){
this->a=a;
this->b=b;
this->c=c;
}
Triangle(float b,float h){
this->b=b;
this->h=h;
}
float area(){
cout<<a;
return area(this->a,this->b,this->c); 
}
float area(float a,float b,float c){
float p=(a+b+c)/2;
return sqrt(p*(p-a)*(p-b)*(p-c)); 
}
// overloaded functions for calculating are
float area(float b,float h){

return (b+h)/2;
}
//Overload assignment operator
Triangle &operator=(const Triangle & triangle)
{;
this->a = triangle.a;
this->b = triangle.b;
this->c = triangle.c;
return *this;
}
//equality operator.
friend bool operator== (const Triangle &t1, const Triangle &t2){
return (t1.a == t2.a && t1.b == t2.b && t1.c == t2.c);
}
};
int main(){
Triangle triangleABC(18,30,24);
cout<<"Area of the tringle ABC with sides 18,30,24: "<<triangleABC.area(18,30,24)<<"\n";
Triangle triangleBH;
cout<<"\nArea of the tringle with base 24 and height 18: "<<triangleBH.area(24,18)<<"\n";
Triangle triangleCopy=triangleABC;
cout<<"\nArea of the copy tringle with base 24 and height 18: "<<triangleCopy.area()<<"\n";
if(triangleABC==triangleCopy){
cout<<"The triangles are equal.\n";
}else{
cout<<"The triangles are not equal.\n";
}
return 0;
}




 









PRACTICAL 22:- Create a class box containing length , breadth and height. Include following operators in it. (A) calculate surface area of cube (B) calculate volume (C) overload ++ operator (D) overload – operator (E)overload == operator as a friend function (F) overload assignment operator (G) check if it is cube or a cuboid. Write a program which takes input from the user for length, breadth and height to test the above class.
SOLUTION:- 
#include<iostream>
using namespace std;
class Box
{
int length,breadth,height;
public:
double surfacearea();
void print();
double volume();
Box operator++(int n);
Box operator++();
Box operator--(int n);
Box operator--();
Box operator=(Box b1);
friend Box operator==(Box b1,Box b2);
int check();
Box();
};
Box::Box()
{
cout<<"enter the length , breadth and height respectively"<<endl;
cin>>length>>breadth>>height;
}
int Box::check()
{
if(length==breadth==height)
return 1;
else
return 0;
}

double Box::surfacearea()
{
if(check()==0)
return(2*((length*breadth)+(breadth*height)+(height*length)));
else
return(6*length*length);
}
double Box::volume()
{
return(length*breadth*height);
}
Box Box::operator++()
{
length++;
breadth++;
height++;
return(*this);
}
Box Box::operator--(int n)
{
length--;
breadth--;
height--;
return(*this);
}
Box Box::operator++(int n)
{
length++;
breadth++;
height++;
return(*this);
}
Box Box:: operator--()
{
--length;
--breadth;
--height;
return(*this);
}

Box Box::operator=(Box b1)
{
length=b1.length;
breadth=b1.breadth;
height=b1.height;
return(*this);
}
Box operator==(Box b1, Box b2)
{
if((b1.length==b2.length) && (b1.breadth==b2.breadth) && (b1.height==b2.height))
cout<<"The two boxes have equal dimensions";
else
cout<<"The two boxes are unequal";

}
void Box::print()
{
cout<<endl;
cout<<"the  length is "<<length<<endl;
cout<<"the breadth is "<<breadth<<endl;
cout<<"the height is "<<height<<endl;
}


int main()
{
int d=1;
do
{

Box obj;
cout<<"enter 1 to show volume" <<endl<<" 2 for surface area"<<endl<<"3 to increment using postfix"<<endl<<" 4 to increment using prefix"<<endl;
cout<<"5 to decrement using postfix"<<endl<<"6 to decrement using prefix"<<"7 to check equality of two boxes"<<endl;
cout<<"8 to assign values to a box"<<endl<<"9 to check if it is a cube or cu                      boid"<<endl<<"enter 10 to print current box status"<<endl;
cout<<"enter 0 to quit"<<endl;
cin>>d;
switch(d)
{
case 1:
{
cout<<"the volume is "<<obj.volume()<<endl;
break;
}
case 2:
{
cout<<"the surface area is "<<obj.surfacearea()<<endl;
break;
}
case 3:
{
cout<<"increment using postfix";
obj++;
obj.print();
break;
}
case 4:
{
cout<<"increment using prefix";
++obj;
obj.print();
break;
}
case 5:
{
cout<<"decrement using postfix";
obj--;
obj.print();
break;
}
case 6:
{
cout<<"decrement using prefix";
--obj;
obj.print();
break;
}
case 7:
{
cout<<"enter the dimensions of other box";
Box obj2;
obj2==obj;
obj2.print();
break;
}
case 8:
{
cout<<"to assign values to a box object"<<endl;
Box b2=obj;
b2.print();
break;
}
case 9:
{
if(obj.check()==1)
cout<<"it is a cube "<<endl;
else
cout<<"it is a cuboid."<<endl;

break;
}
case 10:
obj.print();
}
cout<<"Enter 0 to quit"<<endl;
cin>>d;
}
while(d!=0);
return 1;
}






 



PRACTICAL 23:- Create a structure student containing fields for roll number, name , class , year, total marks. Create 10 students and store them into file.
SOLUTION:-
#include<iostream>
#include<fstream>
using namespace std;
struct student 
{
	int roll_no;
	char name[30];
	char batch[20];
	int year;
	int marks;
}s[10];
int main()
{

	int i=0;
  cout<<"DETAILS OF THE STUDENT"<<endl;
  for(i=0;i<10;i++)
  {
  	cout<<"Enter the details of student "<<i+1<<endl;
  	cout<<"Enter the roll number"<<endl;
  	cin>>s[i].roll_no;
  	cout<<"Enter the name"<<endl;
  	cin>>s[i].name;
  	cout<<"Enter the class"<<endl;
  	cin>>s[i].batch;
  	cout<<"Enter the year"<<endl;
  	cin>>s[i].year;
  	cout<<"Enter the total marks"<<endl;
    cin>>s[i].marks;
  }
  fstream student;
  student.open("student",ios::out);
  if(!student)
  {
   cout<<"file creation failed";
  }	
  else
  {
  	student<<"DISPLAYING DETAILS OF STUDENTS";
  	for(i=0;i<10;i++)
  	{
  	cout<<"STUDENT "<<i+1<<endl;
    student<<"Roll No.    : "<<s[i].roll_no<<endl;
  	student<<"Name        : "<<s[i].name<<endl;
  	student<<"Class       : "<<s[i].batch<<endl;
  	student<<"Year        : "<<s[i].year<<endl;
  	student<<"Total marks : "<<s[i].marks<<endl<<endl;
    }
    student.close();
  }
}






 


 

 



PRACTICAL 24:- Write a program to retrieve the information from the file created in previous question and print in the following pattern roll no , name, marks.
SOLUTION:-
#include<iostream>
#include<fstream>
using namespace std;
struct student 
{
	int roll_no;
	char name[30];
	int marks;
}s[2];
int main()
{

	int i=0;
  cout<<"DETAILS OF THE STUDENT"<<endl;
  for(i=0;i<2;i++)
  {
  	cout<<"Enter the details of student "<<i+1<<endl;
  	cout<<"Enter the roll number"<<endl;
  	cin>>s[i].roll_no;
  	cout<<"Enter the name"<<endl;
  	cin>>s[i].name;
  	cout<<"Enter the total marks"<<endl;
    cin>>s[i].marks;
  }
  	cout<<"DISPLAYING DETAILS OF STUDENTS";
  	for(i=0;i<2;i++)
  {
  	cout<<"STUDENT "<<i+1<<endl;
    cout<<"Roll No.    : "<<s[i].roll_no<<endl;
  	cout<<"Name        : "<<s[i].name<<endl;
  	cout<<"Total marks : "<<s[i].marks<<endl<<endl;
  }
}





 


PRACTICAL 25:- Copy the contents of the one file to another text file, after removing all the whitespaces.
SOLUTION:-
#include<iostream>
#include<fstream>
using namespace std;
int main()
{
	fstream filename;
	filename.open("t.txt",ios::out);
	if(!filename){
		cout<<"error while creating file";
	}
	else
	{
		cout<<"Data written into file";
		filename<<"hello\nbsc.it-2\nstudents\n";
		filename.close();
	}
	ifstream obj;
	obj.open("t.txt",ios::in);
	ofstream file;
	file.open("copy.txt",ios::out);
	if(!obj)
	cout<<"error while opening the file";
	else
	{
		char buff[1000];
		cout<<"\nThe contents in the file are\n";
		while(obj)
		{
			obj.getline(buff,1000);
			cout<<buff<<endl;
			file<<buff<<endl;
		}
	}
}





 




PRACTICAL 26:- Write a function that reverses the elements of array in place. The function must accept only one pointer value and return void.
SOLUTION:-
#include<iostream>
using namespace std;
int main()
{
	int arr[10],n,i=1;
	int*parr=arr;
	cout<<"enter the size of array"<<endl;
	cin>>n;
	cout<<"enter the elements of array"<<endl;
	for(i=0;i<n;i++)
	{
		cin>>*(parr+i);
	}
	cout<<"\nThe elements of array are"<<endl;
	for(i=0;i<n;i++)
	{
		cout<<*(parr+i)<<endl;
	}
	cout<<"\nThe reversed form of array are"<<endl;
	for(i=n-1;i>=0;i--)
	{
		cout<<*(parr+i)<<endl;
	}
	return 0;
}











PRACTICAL 27:- write a program that reads 10 integers from user and store them in array. Implement array using pointers. The program will print the array in ascending and descending order.

SOLUTION :- 

#include <iostream>
#include <math.h>
#define N 10
using namespace std;
int main(int argc, char **argv)
{
int *arr=new int[N];
int i;
for(i=0;i<N;i++)
{
cout<<"Input element "<<i<<": ";
cin>>arr[i];
}
int min,j;
for(i=0;i<N;i++)
{
min=i;
for(j=i+1;j<N;j++)
if(arr[j]<arr[min])
min=j;
j=arr[min];
arr[min]=arr[i];
arr[i]=j;
}
cout<<"In ascending order: ";
for(i=0;i<N;i++)
cout<<arr[i]<<" ";
cout<<endl<<"In descending order: ";
for(i=0;i<N;i++)
cout<<arr[N-i-1]<<" ";
return 0;
}







 















PRACTICAL 28:- Write a program to show function overloading and operator overloading.
SOLUTION:-
#include<iostream>
using namespace std;
class abc
{
	int a,b;
	public:
		void display(int a,double b)
		{
			cout<<"int a="<<a<<" double b="<<b<<endl;
		}
		void display(int a,int b)
		{
			cout<<"int a="<<a<<" int b="<<b<<endl;
		}
		void display(char c)
		{
			cout<<"char c="<<c<<endl;
		}
};
int main()
{
	abc obj;
	obj.display(2,3.4);
	obj.display(5,6);
	obj.display('r');
}






 

PRACTICAL 29:- WAP to create a class and access member function of a class.
SOLUTION:- 
#include<iostream>
using namespace std;
class student
{
  int id;
  string name;
  public:
   void getdata()
   {
    cout<<"Enter the name of the student"<<endl;
    getline(cin,name);
    cout<<"Enter the id of the student"<<endl;
    cin>>id;
   }
   void display()
   {
   	cout<<"\nDISPLAYING INFORMATION\n";
    cout<<"The Id of the student is = "<<id<<"\n";
    cout<<"The name of the student is = "<<name<<"\n";
   }
};
int main()
{
  student s1;
  s1.getdata();
  s1.display();
}


 










PRACTICAL 30:- . Write a program to show Constructor and Destructor in a class.

SOLUTION:- 

#include<iostream>
using namespace std;
class Marks
{
public:
int maths;
int science;
Marks() {
cout << "Inside Constructor"<<endl;
cout << "C++ Object created"<<endl;
}
~Marks() {
cout << "\nInside Destructor"<<endl;
cout << "C++ Object destructed"<<endl;
}
};
int main( )
{
Marks m;
return 0;
}






 













PRACTICAL 31:- Write a program to show the concept of inheritance in classes.
SOLUTION:- 
#include<iostream>
using namespace std;
class dimension
{
 protected:
 int side;
 public:
    void getinfo()
	{
    cout<<"enter the side of square"<<endl;
	cin>>side;
	}
};
class square:public dimension
{
	public:
	float area;
	void display()
	{
		area=side*side;
		cout<<"The area of square is : "<<area;
	}
};
int main()
{
	square s;
	s.getinfo();
	s.display();
}












PRACTICAL 32:- Write a program to implement the file handling concepts.
SOLUTION:-
#include<iostream>
#include<fstream>
using namespace std;
int main()
{
  fstream new_file;
  new_file.open("new_file",ios::out);
  if(!new_file)
  {
   cout<<"file creation failed";
  }	
  else
  {
  	cout<<"new file created";
  	new_file.close();
  }
}






 

PRACTICAL 33:- Write a program to implement the exception handling.
SOLUTION:-
#include<iostream>
using namespace std;
int main()
{
int a,b;
cout<<"Enter any two integer values"<<endl;
cin>>a>>b;
int x=a-b;
try
{
if(x!=0)
{
cout<<"Result(a/x)="<<a/x<<endl;
}
else
{
throw x;
}
}
catch(int x)
{
cout<<"Exception caught:Divide By Zero \n";
}
}






 












