//first exercise ---------------------------------------------------------------------------------------------------
#include <iostream>
#include <cmath>

using namespace std;

double firstCalculation(double z){
	double resultFirst = 0.0; 
	return resultFirst = (6 * (z * z) - 5) / 3;
}
double secondCalculation(double z) {
	double resultSecond = 0.0; 
	return resultSecond = (5 * (z * z) - 4) / 12; 
}
int main() {
	int z;

	cout << "Enter an integer: ";
	cin >> z;

	if (z <= 1) {
		cout << "Result:" << firstCalculation(z);
	}
	else {
		cout << "Result:" << secondCalculation(z);
	}
	return 0;
}

//second exercise --------------------------------------------------------------------------------------------------- ヾ(- _ - )ゞ
#include <iostream>
#include <cmath>
using namespace std;

// A utility function to calculate area of triangle formed by(x1, y1),(x2, y2) and (x3, y3)
float area(int x1, int y1, int x2, int y2, int x3, int y3){
	return abs((x1 * (y2 - y3) + x2 * (y3 - y1) + x3 * (y1 - y2)) / 2.0);
}

// A function to check whether point P(x, y) lies inside the triangle formed by A(x1, y1), B(x2, y2) and C(x3, y3)
bool isInsideFirst(int x1, int y1, int x2, int y2, int x3, int y3, int x, int y) {
	// Calculate area of triangle ABC 
	float A = area(x1, y1, x2, y2, x3, y3);
	//Calculate area of triangle PBC
	float A1 = area(x, y, x2, y2, x3, y3);
	//Calculate area of triangle PAC 
	float A2 = area(x1, y1, x, y, x3, y3);
	//Calculate area of triangle PAB 
	float A3 = area(x1, y1, x2, y2, x, y);
	return (A == A1 + A2 + A3);
}
bool isInsideSecond(int radius, int angle, int startAngle, int x, int y){
	// calculate endAngle 
	float endAngle = angle + startAngle;
	// Calculate polar co-ordinates
	float polarradius = sqrt(x * x + y * y);
	float newAngle = atan(y / x);
	return (newAngle >= startAngle && newAngle <= endAngle && polarradius < radius);
}
int main(){
	int x, y; cout << "Enter Coordinates:"; cin >> x; cin >> y;
	//check whether the point P(x, y) lies inside the triangle formed by A(0, 0), B(1, 0) and C(0, 1) and sector formed by r = 1, which starts on the(-1; 0) 
	if (isInsideFirst(0, 0, 1, 0, 0, 1, x, y) || isInsideSecond(1, 90, 180, x, y)) 
		cout << "Inside"; 
	else 
		cout << "Not Inside";

	return 0;
}
