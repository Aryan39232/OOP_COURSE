class rectangle:
  def _init_(self,length,width):
    self.length = length
    self.width = width

  def rectangle_area(self):
    return self.length*self.width

r = rectangle(12,20)
print(r.rectangle_area())
