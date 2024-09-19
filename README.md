# add_complex
a simple code practice

这是一个复数相加的代码练习
#include<iostream>
using namespace std;
class Complex {
	double real;
	double imag;
public:
	Complex():real(0),imag(0){}
	Complex(double a, double b) :real(a), imag(b) {}
	void display();
	Complex operator+(Complex &c2);

};
void Complex::display() {
	cout << "(" << real << "," << imag << "i)" << endl;
}
Complex Complex::operator+(Complex& c2) {
	Complex c1(real + c2.real, imag + c2.imag);
	return c1;
}
int main() {
	Complex c(3, 2), cc;
	cc.display(); c.display();
	cc=cc + c;
	cc.display();
	return 0;
}
