// matrices-calculator
//multiplication of matrices
#include<stdio.h>
#include<iostream.h>
#include<conio.h>

int main() {
   int a[10][10], b[10][10], c[10][10], i, j, k;
   int sum = 0;

   cout<<"\nEnter First Matrix : n";
   for (i = 0; i < 3; i++) {
      for (j = 0; j < 3; j++) {
	 cin>>a[i][j];
      }
   }

   cout<<"\nEnter Second Matrix:n";
   for (i = 0; i < 3; i++) {
      for (j = 0; j < 3; j++) {
	 cin>>b[i][j];
      }
   }

   cout<<"The First Matrix is: \n";
   for (i = 0; i < 3; i++) {
      for (j = 0; j < 3; j++) {
	 cout<<"\t"<<a[i][j];
      }
      cout<<"\n";
   }

   cout<<"The Second Matrix is : \n";
   for (i = 0; i < 3; i++) {
      for (j = 0; j < 3; j++) {
	 cout<<"\t"<<b[i][j];
      }
      cout<<"\n";
   }

   //Multiplication Logic
   for (i = 0; i <= 2; i++) {
      for (j = 0; j <= 2; j++) {
	 sum = 0;
	 for (k = 0; k <= 2; k++) {
	    sum = sum + a[i][k] * b[k][j];
	 }
	 c[i][j] = sum;
      }
   }

   cout<<"\nMultiplication Of Two Matrices : \n";
   for (i = 0; i < 3; i++) {
      for (j = 0; j < 3; j++) {
	 cout<<"\t"<<c[i][j];
      }
      cout<<"\n";
   }

   getch();
}
