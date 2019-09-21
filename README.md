# INHERITENCE-1

#INHERITANCE METHOD

class Mobile:
    def __init__(self,brand,model,price):
        self.brand = brand
        self.model = model
        self.price = price


    def display_all(self):
        return f'MOBILE: {self.brand}, MODEL: {self.model} and PRICE: {self.price}'

class Smartphone(Mobile):

    #two ways we use the inheritance:
    
    def __init__(self,brand,model,price,ram,internal_memory,rear_camera):
        # 1st method:
        # Mobile.__init__(self,brand,model,price)
        #2nd Method:
        super().__init__(brand,model,price)
        self.ram = ram
        self.internal_memory = internal_memory
        self.rear_camera = rear_camera


mob1 = Mobile('nokia',1108,3000)
mob2 = Smartphone('samsung','qeqwq',40000,'16GB','30GB','25megaPIxcel')
print(mob1.display_all())
print(mob2.price)
print(mob2.display_all())
