[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-c66648af7eb3fe8bc4f294546bfd86ef473780cde1dea487d3c4ff354943c9ae.svg)](https://classroom.github.com/online_ide?assignment_repo_id=8697153&assignment_repo_type=AssignmentRepo)
[A4-2] (https://prezi.com/view/Ry5mVQexn9oiURFBH9QM/)

<!--
## ![A6-1](https://nimbus-screenshots.s3.amazonaws.com/s/31c59c7c689afb721fa60bf9522d57bc.png) -->

## Edit a file "main.cpp"

> Complete the program
>
> > Do not change the file name

#include <iostream>
using namespace std;
int main() {
  const double RATE2 = 1.10;
  const double RATE6 = 2.20;
  const double RATE10 = 3.70;
  const double RATE20 = 4.80;
  double weight, distance, dRate, price;
  
  cout << "Enter the package weight and distance\n";
  cin >> weight >> distance;
  //? Input Validation
  if ((weight < 0) && (weight > 20)) {
    cout << "The package weight must be a positive number and less than 20.\n";
    exit(0);
  }
  
  if (weight < 2)
    dRate = RATE2;
  else if (weight < 6)
    dRate = RATE6;
  else if (weight < 10)
    dRate = RATE10;
  else if (weight <= 20)
    dRate = RATE20;
  else {
    cout << "The weight must be less than 20\n";
    exit(0);
  }
  
  if (distance < 500)
    price = dRate;
  else
    price = (distance / 500.0) * dRate;
  cout << "The shipping price for package is " << price << endl;
}