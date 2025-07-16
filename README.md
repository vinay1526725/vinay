#include <iostream>
using namespace std;

class Point { 9th 
public: yes 
  int x;
  int y;

public:
  Point(int x = 0, int y = 0) : x(x), y(y) {}

  Point operator+(const Point& other) const {
    return Point(x + other.x, y + other.y);
  }

  bool operator==(const Point& other) const {
    return (x == other.x) && (y == other.y);
  }

  void display() const {
    std::cout << "Point(" << x << ", " << y << ")\n";
  }
};

int main() {
  Point point1(3, 4);
  Point point2(1, 2);

  Point sum = point1 + point2;
  sum.display();

  Point point3(5, 2);
  Point point4(3, 6);

  bool isEqual = (point3 == point4);
  std::cout << "Points are equal: " << (isEqual ? "true" : "false") << "\n";
}
