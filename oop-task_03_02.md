class fl:
  def __init__(self, crt, des, size):
    self.crt = crt
    self.des = des
    self.size = size

  def disp(self):
    print("Creator:", self.crt)
    print("Description:", self.des)
    print("Size:", self.size)

  def chksize(self):
    if self.size >= 1000:
      print("File is very Large")
    else:
      print("File is not Large")
  
class picture(fl):
  def __init__(self, crt, des, size, dim1, dim2):
    fl.__init__(self, crt, des, size)
    self.dim1 = dim1
    self.dim2 = dim2

  def disp(self):
    fl.disp(self)
    print("Dimensions:", self.dim1, 'X', self.dim2)

  def chkdims(self):
    if (self.dim1 > 1920  or self.dim2 > 1080):
      print("Dimensions of the picture are very large")
    else:
      print("Dimensions of the picture are not very large")

f1 = fl("Jaynt", "PDF of Coreman", 980)
f2 = picture("Jaynt", "Picture of Sun", 2040 ,1280, 720)

f2.disp()
f2.chkdims()
f2.chksize()
