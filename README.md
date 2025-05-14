# <p align=center> 🏹***Choose Your Weapon***⚔️

<p align=center> <img src=Images/Weapons_Banner.png alt="Weapons Banner">

## <p align=center>An Object-Oriented Program using `Weapons⚔️` as a Class
### ***CS-1204 Team 9***🧑‍❤️‍💋‍👨 <br />
| Members                       | Github Profile                                              |
|-------------------------------|-------------------------------------------------------------|
| **Bernal, Brandon Josef Y.**  | [Brandon-JYB](https://github.com/Brandon-JYB)               |
| **Lunar, Von Andrei G.**      | [Dreilunar](https://github.com/DreiLunar)                   |
| **Mendoza, James Gabriel S.** | [JamesMendozaRiniya](https://github.com/JamesMendozaRiniya) |
| **Oliver, Jmar C.**           | [yeloooooooooooooo](https://github.com/yeloooooooooooooo)   |
<br />

## **Weapon Class: The Heart of the Weapon Management System🧙‍♂️**

&ensp; The Weapon class serves as the cornerstone of our weapon management system. Building upon the foundation provided by the `AbstractWeapon` parent class, this implementation brings weapons to life with practical functionality and unique special abilities.
Each weapon is characterized by essential attributes including its `name`, `level`, `damage`, `damage type`, `range`, `durability status`, `historical origin`, and `age`. Beyond these standard properties, certain exceptional weapons possess special attack capabilities that set them apart on the battlefield.
When a user selects a weapon, they can examine its complete statistical profile through the display function, revealing all the vital information needed to make tactical decisions. The practical `use_weapon` method simulates combat usage, tracking durability degradation with each deployment and preventing further use when a weapon reaches its breaking point.
Perhaps most intriguing is the `special_attack` feature, which activates unique abilities for select fictional weapons.

### 💻*Code Snippet:*
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
To our beloved teacher, **Ms. Fatima Marie Agdon**.

<br />

&ensp; We would like to express our sincere gratitude for your dedication, patience, and passion in teaching us computer programming. Your ability to explain complex topics clearly and guide us through each challenge has made a big difference in our learning experience.

&ensp; Thank you for sharing your knowledge, for believing in our potential, and for inspiring us to think critically and code with confidence. Your support and encouragement have been truly meaningful, and we are incredibly grateful for all the time and effort you've given us.

<br />

*Sincerely,* <br />
**Team 9**