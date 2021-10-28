from abc import abc, abstractmethod
import math
class shape(abc):
    def _init_(self, shape):
        self.shape = shape

    @abstractmethod
    def area(self):
        pass

class rectangle(shape):
    def _init_(self, length, breadth):
        shape._init_(self, 'rectangle')
        self.length = length
        self.breadth = breadth

    def area(self):
        return self.length*self.breadth

class circle(shape):
    def _init_(self, radius):
        shape._init_(self, 'circle')
        self.radius = radius

    def area(self):
        return round((math.pi)(self.radius*2),2)

class square(shape):
    def _init_(self, side):
        shape._init_(self, 'square')
        self.side = side

    def area(self):
        return self.side*self.side

sq = square(9)
print("area of square   :", sq.area())
rect = rectangle(6,7)
print("area of rectangle:", rect.area())
c = circle(8)
print("area of circle   :", c.area())
