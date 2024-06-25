# python-
# PYTHON-PROGRAM-8
program for finding distance and converting km to meters
class distance:
    def __init__(self):
        self.km = 0
        self.m = 0
    def set(self,km,m):
        self.km = km
        self.m = m
    def __isub__(self,distance):
        self.m = self.m-distance.m
        if self.m<0:
            self.m += 1000
            self.km += 1
        self.km = self.km-distance.km
        return self
    def convert_to_meters(self):
        return self.km*1000+self.m
    def display(self):
        print(self.km,"killometers",self.m,"meters")
d1 = distance()
d2 = distance()
d1.set(21,70)
d2.set(18,120)
d1 -= d2
print("d1-d2:")
d1.display()
print("that is :",d1.convert_to_meters(),"meters")
