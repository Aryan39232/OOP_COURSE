class travel:

  def _init_(self, travel):
    self.travel = travel

  def number_of_passangers(self):
    pass

  def distance(self):
    pass

  def mode(self):
    pass

class train(travel):

  def _init_(self, total_passangers):
    self.total_passangers = total_passangers

  def cost_of_transport(self):
    print('cost of transport by train is',self.total_passangers*60)

class bus(travel):

  def _init_(self, total_passangers):
    self.total_passangers = total_passangers

  def cost_of_transport(self):
    print('cost of transport by bus is',self.total_passangers*100)

mode1 = train(12)
mode1.cost_of_transport()

mode2 = bus(12)
mode2.cost_of_transport()
