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

## 📜How to Use:
### Main Menu
When you start the program, you'll see the main menu displaying weapon classes:

```
Select weapon class:
1. Sword
2. Marksman
3. Caster
4. Ranger
```
Enter the number corresponding to the weapon class you'd like to explore, or type 'q' to quit the program.

### Selecting a Weapon
After choosing a class, you'll be shown available weapons within that category:

```
Select [Weapon Class] weapon:
1. [Weapon 1]
2. [Weapon 2]
3. [Weapon 3]
```
Enter the number of the weapon you want to select.

### Weapon Stats
Once a weapon is selected, its stats will be displayed:

```
[Weapon Name] Stats:
Level: [Level]
Damage: [Damage]
Damage Type: [Type]
Range: [Range]
Durability: [Durability]/100
```
### Using the Weapon
You'll be prompted to use the weapon:

```
Do you want to use this weapon? (Y/N):
```
- Enter 'Y' to use the weapon, which reduces its durability by 10 points
- Enter 'N' to return without using it

### Special Attacks
If the selected weapon has a special attack capability, you'll be prompted:
```
Do you want to use the special attack? (Y/N):
```
- Enter 'Y' to execute the special attack
- Enter 'N' to return without using it

## **🙇Acknowledgement:**
To our beloved teacher, **Ms. Fatima Marie Agdon**.

<br />

&ensp; We would like to express our sincere gratitude for your dedication, patience, and passion in teaching us computer programming. Your ability to explain complex topics clearly and guide us through each challenge has made a big difference in our learning experience.

&ensp; Thank you for sharing your knowledge, for believing in our potential, and for inspiring us to think critically and code with confidence. Your support and encouragement have been truly meaningful, and we are incredibly grateful for all the time and effort you've given us.

<br />

*Sincerely,* <br />
**Team 9**