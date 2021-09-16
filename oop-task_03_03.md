class vechicle:
    def __init__(self):
        self.name =  input("Enter the vechcile : ")
        self.mileage = (int)(input("Enter the mileage : "))
        self.capacity = (int)(input("Enter the capacity : "))
  
    def display1(self):
        print("Name : {}\nMileage = {}\nCapacity = {}\nTOTAL_FARE = {}\n".format(self.name,self.mileage,self.capacity,self.fare))   
class bus(vechicle):
    def __init__(self):
        vechicle.__init__(self)
    def fare(self):
        self.fare = self.capacity * 100
        if self.capacity > 50 :
            self.fare = self.capacity * 100 + ((self.capacity * 100)*0.1)
        else:
            self.fare = self.capacity * 100
   
v1 = bus()
v1.fare()
v1.display1()
