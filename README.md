[![CodeFactor](https://www.codefactor.io/repository/github/itstep-vrn/rpgengineteamz/badge)](https://www.codefactor.io/repository/github/itstep-vrn/rpgengineteamz)

# PRGengineTeamZ
Учебный репозиторий для создания игры

#### Авторы:
+ [*© Самодуров Сергей\(SergeySamodurovS\)*](https://github.com/SergeySamodurovS) - тимлид
+ [*© Рязанцев Илья\(RID1991-IT\)*](https://github.com/RID1991-IT)
+ [*© Сафарова Рената\(RenataRobertovna\)*](https://github.com/RenataRobertovna)
+ [*© Меркулов Алексей\(mnementjr\)*](https://github.com/mnementjr)

## Классы.

**1. Equipment (экипировка)**

У игрока может быть экипировка из списка: шлем, кираса, пояс, штаны, перчатки, ничего.

У каждой вещи есть свои наименование, показатель брони и стоимость покупки.

**2. Weapon (оружие)**

У игрока может быть оружие из списка: костет, меч, посох, лук, кинжал, ничего.

У каждого оружия есть свои наименование, показатель урона и стоимость покупки. 

**3. Magic (магия)**

У игрока может быть магические заклинания из списка: стрела, молния, кулак, камнепад, файрбол, ничего.

У каждого заклинания есть свои наименование, показатель урона, стоимость покупки, затраты маны.

**4. Create (создание экземляров классов)**

Создаются экземпляры классов всех видов экипировки, оружия и заклинаний. 

**5. Hero (герой)**

У героя есть свойства: имя, урон, количество монет, оружие (только одно), магическое заклинание (только одно), список экипировки (может иметь по одной вещи каждого типа), уровень здоровья, маны.

Создаётся конструктор с параметром "Имя героя". После этого вызывается метод NewHero, который задаёт остальные параметры в значение по-умолчанию. 

Метод BuyingEquipment позволяет покупать экипировку, если достаточно средств, и у игрока ещё нет такого типа экипировки.

Метод BuyingWeapons позволяет покупать оружие, если достаточно средств.

Метод BuyingMagic позволяет покупать магическое заклинание, если достаточно средств.

Метод DealDamage вычисляет количество урона, который может нанести герой.

Метод GetInnerDamage получает в параметрах количество входящего урона, вычисляет количество блокируемого экипировкой урона, а затем изменяет уровень текущего здоровья героя.

Метод IsAlive проверяет жив ли герой и возвращает истину если жив, ложь если мёртв (уровень здоровья <= 0).

Метод GetMoney получает в качестве параметра количество золотых, которое получает герой, и прибавляет их к текущему балансу.

Метод RestoreHealth получает в качестве параметра значение восстанавливаемого здоровья и прибавляет его к текущему показателю здоровья. Если в результате этого текущее здоровье становится больше максимального, то текущее здоровье устанавливается равным максимальному;

Метод RestoreMana получает в качестве параметра значение восстанавливаемой маны и прибавляет его к текущему показателю маны. Если в результате этого текущий уровень маны становится больше максимального, то текущее значение маны устанавливается равным максимальному;

**6. Другие классы**

Классы Experience, Health, Items, Mana являются заделами под более поздние расширенные версии игры.
