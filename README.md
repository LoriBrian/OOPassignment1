# OOPassignment1

**Design Your Own Class**
--Superhero Class with Inheritance & Encapsulation

# Base class
class Superhero:
    def __init__(self, name, power, level):
        self.name = name
        self.power = power
        self.__level = level  # Encapsulated/private attribute

    def display_info(self):
        print(f"{self.name} has the power of {self.power}!")

    def get_level(self):  # Encapsulation - accessing private attribute
        return self.__level

    def level_up(self):
        self.__level += 1
        print(f"{self.name} is now level {self.__level}!")

# Subclass
class FlyingHero(Superhero):
    def __init__(self, name, power, level, flight_speed):
        super().__init__(name, power, level)
        self.flight_speed = flight_speed

    def fly(self):
        print(f"{self.name} is flying at {self.flight_speed} km/h! 🕊️")

        
--Usage

hero1 = FlyingHero("SkyWing", "Wind Control", 5, 300)
hero1.display_info()
hero1.fly()
hero1.level_up()
print(f"Current Level: {hero1.get_level()}")


**Polymorphism Challenge**
--Vehicles with Different move() Methods

class Vehicle:
    def move(self):
        pass  # base method

class Car(Vehicle):
    def move(self):
        print("Driving 🚗")

class Plane(Vehicle):
    def move(self):
        print("Flying ✈️")

class Boat(Vehicle):
    def move(self):
        print("Sailing 🚢")


--Usage:

vehicles = [Car(), Plane(), Boat()]

for v in vehicles:
    v.move()
