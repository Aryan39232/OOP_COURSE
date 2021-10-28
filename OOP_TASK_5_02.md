class car:
  def _init_(self,carnumber):
    self.carnumber=carnumber
c1=car(1998)
c2=car(2002)
print('the model number of c1 is',c1.carnumber)
print('the model number of c2 is',c2.carnumber)
print('--------------------------------')
def carnumswap():
  c1.carnumber,c2.carnumber=c2.carnumber,c1.carnumber
  print("the model number of c1 is ",c1.carnumber)
  print("the model number of c2 is ",c2.carnumber)
carnumswap()
