# <p align=center> ***🏹Choose Your Weapon⚔️***

<p align=center> <img src=Images/Weapons_Banner.png alt="Weapons Banner">

### An Object-Oriented Program using `Weapons⚔️` as a Class
🧑‍❤️‍💋‍👨by: ***CS-1204 Team 9😎*** <br />
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;**Bernal, Brandon**<br />
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;**Lunar, Von Andrei G.**<br />
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;**Mendoza, James Gabriel** <br />
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;**Oliver, Jmar**

<br />

### **👩‍🏫Context:**

&nbsp; Our class in CS 121 was tasked to do our laboratory activity 3 and 4 about our topic--Object-Oriented Programming that focuses on classes. Our team was assigned to create a program that uses classes and was given `Weapons` to use as our topic. This Python software develops a weapon management system based on object-oriented programming concepts. It consists of an abstract base class AbstractWeapon, which has common properties such as name, level, damage, and durability, and an abstract method special_attack. The Weapon class inherits from AbstractWeapon and implements the special_attack method, which activates unique special powers for some weapons. The WeaponManager class keeps many weapon types, including swords, marksman, casters, and rangers. Each weapon category provides a variety of weapons with unique qualities. The application allows users to select a weapon class, select a weapon from the available options, check its stats, use the weapon, and activate its special attack (if the weapon does have one).


<br />

## **Weapon Class: The Heart of the Weapon Management System🧙‍♂️**

&nbsp; The Weapon class serves as the cornerstone of our weapon management system. Building upon the foundation provided by the AbstractWeapon parent class, this implementation brings weapons to life with practical functionality and unique special abilities.
Each weapon is characterized by essential attributes including its name, level, damage potential, damage type, effective range, durability status, historical origin, and age. Beyond these standard properties, certain exceptional weapons possess special attack capabilities that set them apart on the battlefield.
When a user selects a weapon, they can examine its complete statistical profile through the display function, revealing all the vital information needed to make tactical decisions. The practical use_weapon method simulates combat usage, tracking durability degradation with each deployment and preventing further use when a weapon reaches its breaking point.
Perhaps most intriguing is the special_attack feature, which activates unique abilities for select weapons. The enchanting Doughdil charms enemies to lower their defenses, while the mystical Wand unleashes devastating lightning bolts. The Pope's Staff demonstrates ultimate power by disintegrating all enemies in its path, and the magical Tome creates healing circles to restore allies across a wide area.

### *💻Code Snippet:*
```python
class Weapon(AbstractWeapon):
    def __init__(self, name, level, damage, damage_type, range, durability, origin, age, has_special_attack=False):
        super().__init__(name, level, damage, damage_type, range, durability, origin, age)
        self.has_special_attack = has_special_attack

    def display_stats(self):
        print(f"\n{self.name} Stats:")
        print(f"Level: {self.level}")
        print(f"Damage: {self.damage}")
        print(f"Damage Type: {self.damage_type}")
        print(f"Range: {self.range}")
        print(f"Durability: {self.durability}/100")

    def use_weapon(self):
        if self.durability <= 0:
            print(f"{self.name} is broken and cannot be used!")
            return False

        self.durability -= 10
        print(f"{self.name} was used, dealing {self.damage} damage! Remaining durability: {self.durability}/100")
        return True

    def special_attack(self):
        if not self.has_special_attack:
            print(f"{self.name} has no special attack.")
        else:
            if self.name == "Doughdil":
                print(f"{self.name} charms the enemy, lowering their defenses!")
            elif self.name == "Wand":
                print(f"{self.name} fires a bolt of blue lightning!")
            elif self.name == "Pope's Staff":
                print(f"{self.name} unleashes divine power, disintegrating every enemy target!")
            elif self.name == "Tome":
                print(f"{self.name} creates a magic circle, healing all allies in a wide-range area!")
```


<br />

### **🙇Acknowledgement:**

<br />
