## 2.2 Economy

>>>R1

C> The general that hearkens to my counsel and acts upon it, will conquer: let such a one be retained in command! The general that hearkens not to my counsel nor acts upon it, will suffer defeat — let such a one be dismissed! While heading the profit of my counsel, avail yourself also of any helpful circumstances over and beyond the ordinary rules.
C>
C> -- Sun Tzu "Art of War"

In this section, we will explore the economic component of League of Legends. It is simpler than in real-time strategy games. Despite this, the economy is important and often decides the outcome of a game.

A player must calculate the resources that each possible action will bring him. This allows him to distinguish between profitable and unprofitable actions. This way, a player will be more efficient in investing his time in resources. The team that converts time into resources better gains an advantage.

Let us look at how to calculate resources when planning actions correctly.

### 2.2.1 Gold and experience income

>>>R1

Resource calculations help make decisions. The more accurate they are, the more complete the information a player has. This information can help make better decisions, but it does not guarantee error-free play.

Let us calculate the resources that champions receive during the laning phase.

#### 2.2.1.1 Income on lane

>>>R1

Let us first look at champions who farm minions on some lane. The first wave of minions for each lane spawns near the Nexus at 1:05 game time. Subsequent waves then spawn every 30 seconds: at 1:35, 2:05, and so on.

If a champion finishes off all enemy minions in a single wave, he receives the maximum possible gold. This amount increases as the game progresses.

Table 2-2 shows the average cost of one minion wave depending on game time.

{caption: "Table 2-2. Minion wave gold reward", width: "70%"}
| Game time | Average wave cost | Average gold per 1 cs |
|  | | |
| --- | --- | --- |
|  | | |
| 0:00 | 125 | 19.8 |
|  | | |
| 15:00 | 147 | 22.6 |
|  | | |
| 17:15 | 150 | 23 |
|  | | |
| 25:00 | 190 | 27.6 |

I> **Creep score** (cs) is the number of enemy minions or jungle monsters that a champion has last hit.

According to the table, one minion wave yields an average of 150 gold. Waves spawn at the Nexus every 30 seconds. Therefore, a lane champion farms two minion waves in one minute. This means his income is approximately 300 gold per minute.

Killing a minion grants not only gold but also experience (EXP or XP). If the champion is within 1500 range when the minion dies, he receives experience. This does not even require attacking the minion.

Table 2-3 shows the experience reward for each minion type.

{caption: "Table 2-3. Minion experience rewards", width: "80%"}
| Minion type | Experience reward | Reward increases every 3 minutes |
|  | | |
| --- | --- | --- |
|  | | |
| Melee minion | 60 | +5 |
|  | | |
| Caster minion | 30 | +3 |
|  | | |
| Siege minion | 93 | +7 |

Each wave contains three warrior minions and three mage minions. The first siege minion appears in the fourth wave. After that, until the 15th minute, it appears in every third wave: 7, 10, 13, and so on. Then, from the 15th to the 25th minute, it appears in every second wave. After the 25th minute, each wave includes a siege minion.

Let us calculate the experience income per minute in a lane. In one wave, a champion receives, on average, `60 * 3 + 30 * 3 ~ 300` experience until the 15th minute. This means he will receive 600 experience in two waves. In other words, his income is 600 experience per minute. We could evaluate whether this is a big or a small number. To do this, let us refer to Table 2-4. It shows the amount of experience and minion waves a champion needs to reach each level.

{caption: "Table 2-4. Experience to reach certain champion levels", width: "80%"}
| Level | Experience | Minion waves | Shared minion waves |
|  | | | |
| :---: | :---: | :---: | :---: |
|  | | | |
| 2 | +280 | 2 | 2 |
| 3 | +380 | 3 | 4 |
| 4 | +480 | 4 | 6 |
| 5 | +580 | 6 | 9 |
| 6 | +680 | 9 | 12 |
| 7 | +780 | 11 | 16 |
| 8 | +880 | 14 | 21 |
| 9 | +980 | 18 | 26 |
| 10 | +1080 | 21 | 31 |
| 11 | +1180 | 25 | 37 |
| 12 | +1280 | 30 | 43 |
| 13 | +1380 | 34 | 49 |
| 14 | +1480 | 39 | 55 |
| 15 | +1580 | 45 | 62 |
| 16 | +1680 | 49 | 69 |
| 17 | +1780 | 54 | 76 |
| 18 | +1880 | 60 | 84 |

Shared minion waves mean that two champions are in a lane. In this case, killing each minion grants 130% of the experience gained. This experience is split evenly, with each champion receiving 65%. Because of this, they will be at a lower level than champions in solo lanes.

Note that the 30th minion wave spawns at 16 minutes, which is roughly when the laning phase ends.

#### 2.2.1.2 Income in jungle

>>>R1

Now, let us talk about champions who farm jungle monsters. Each jungle camp grants 4 creep score, which is an average of 100 gold. A jungler can take three camps per minute. Therefore, his income is approximately 300 gold per minute. Note that this is roughly equal to the income of a champion who farms on a lane.

Killing a monster not only grants gold, but also experience. On average, a jungler receives between 165 and 240 experience for one camp. This value increases as the game progresses. For three camps, a jungler receives an average of 600 experience. In other words, his income is approximately 600 experience per minute. This is roughly equal to what a champion in a solo lane receives.

Table 2-5 shows how many monster camps a jungler needs to take to reach the first 7 levels.

{caption: "Table 2-5. Experience for gaining levels for a jungler", width: "85%"}
| Level | Experience | Camps | Creep score |
|  | | | |
| :---: | :---: | :---: | :---: |
|  | | | |
| 2 | +280 | 1 | 4 |
| 3 | +380 | 3 | 12 |
| 4 | +480 | 6 | 24 |
| 5 | +580 | 10 | 40 |
| 6 | +680 | 13 | 52 |
| 7 | +780 | 17 | 68 |

For killing the first camp, the champion receives an additional 150 experience thanks to a jungle item. This same item also provides an additional 80 experience for killing large monsters. Thus, the jungler always gains level 2 at 4 CS.

We examined the income of champions in the lane and jungle. We can draw the following conclusions from this:

1. The first four minion waves are extremely important. For the jungler, the first jungle clear is crucial. This is six monster camps in total.

2. Depriving a champion of income in the first minutes of the game gives an advantage of two or more levels later.

3. When a champion is not farming his lane, he loses resources. For every minute the champion is away, he loses an average of 300 gold and 600 experience that he could have gained.

4. Sharing minion waves between two champions in a lane is only beneficial at the beginning of the game. The longer the game goes on, the less beneficial this becomes. The level gap between champions and solo laners will widen.

Experienced players pay special attention to the first two waves of minions in the lane. At the very beginning of the game, every minion killed counts. It can determine who in lane gains an early advantage. A good player can convert this advantage into the first kill and the tower plate. Thus, correct decisions in the first minutes of the game can determine the outcome of the laning stage.

### 2.2.2 Action planning

>>>R1

Beginner players rarely connect the dots between some action and its long-term results. Therefore, they underestimate the consequences of their mistakes and miscalculations.

Here is an example. Suppose a jungler performs a poor gank. As a result, the enemy top laner survives without even losing health. The player believes there is nothing wrong with this play, and the equilibrium between the teams remains unchanged. In fact, this is not the case: the enemy team gained an advantage. The reason is that the player wasted his time and did not farm the jungle while the enemy jungler did.

I> A **gank** is an ambush of an enemy champion in the lane. This is a typical jungler tactic.

Let us look at several examples of gameplay situations from an economic perspective. They will demonstrate how resource calculations predict the outcome of a given play.

#### 2.2.2.1 Gank

>>>R1

In the first example, the blue team's jungler is planning his actions. He has just returned to base after the first jungle clear. For simplicity, let us assume he is only considering two options:

1. Continue farming his jungle.
2. Gank the enemy mid laner.

We have already calculated that farming the jungle earns a champion about 300 gold and 600 experience per minute. If the enemy jungler does the same, then resource equilibrium remains unchanged between the teams.

Let us calculate the outcome of ganking the mid laner. First, we need to estimate the time it will take. The champion will spend about 30 seconds reaching the mid lane and positioning themselves to attack. This time may be shorter, depending on mobility items and runes.

Let us assume the blue jungler has reached the position to attack the enemy mid laner. He may not be able to attack right away. The jungler will spend some time in ambush, waiting for the right moment. For example, when the enemy moves far away from his tower. After this, the player attacks and pursues the target for a while. The entire gank, from the moment the decision is made at the base until its completion, takes about 40 seconds.

We found that the jungler spent about 40 seconds on the gank. If the player had returned to the jungle and started farming, he would have taken one monster camp. Converted to resources, this comes to approximately 100 gold and 200 experience. This is the jungler's fee for participating in the gank.

Now, let us calculate the teams' gain from the possible gank outcomes. There are three participants in the gank: the red team's mid laner, the blue team's jungler, and the blue team's mid laner. The possible outcomes for each of them are:

1. Killed
2. Survived with minimal health
3. Survived with medium or high health.

**The first scenario** is when an enemy kills the champion. He is then absent from the map for a period of time. This time is made up of two parts:

1. The resurrection time, which depends on the champion's level. During the laning stage, this is on average 20 seconds.

2. The time to reach the middle of his lane or a jungle camp. This time depends on the champion's items and abilities. On average, this is around 30 seconds.

In total, a killed champion is absent from his lane or jungle for almost one minute. During this time, he loses two minion waves or three jungle camps. In other words, he loses 300 gold and 600 experience.

**The second scenario** is when the champion survives on minimal health. In this state, it is dangerous for him to remain in his lane or farm the jungle. The enemy jungler can easily finish him off.

The champion returns to base. Then, he spends 8 seconds casting the [**recall**](https://leagueoflegends.fandom.com/ru/wiki/Воставение_(Закаление)) spell. Afterward, he restores health and mana at the fountain for over 10 seconds. The champion then returns to the lane for about 30 seconds. In total, he is off the map for about 50 seconds. This means he will miss almost two minion waves. In other words, he loses 300 gold and 600 experience. The jungler will have the same effect.

**Third case**: the champion survives on medium or high health. In this state, he can continue farming lane minions or jungle monsters. If he has enough gold, he can return to base to buy an item. Recall will cost him about 40 seconds off the map. That is at least one missed wave, or 150 gold and 300 experience.

Let us summarize the results for each of the three champions to estimate the team's income. For simplicity, we will consider only three gank outcomes:

1. **Best** - the red team's mid laner is killed, and the blue team's champions remain at full health.

2. **Mediocre** - the red team's mid laner survives at minimum health, and the blue team's champions remain at full health.

3. **Worst** - the red team's mid laner remains at full health, and both blue team champions are killed.

In the **best case**, the blue team's income would be as follows:

1. The blue jungler and mid laner receive gold and experience for the kill. The player who did a kill receives 300 gold, and the player who did assist receives 150 gold. It totals 450 gold. They both share approximately 300 experience.

2. The blue mid laner can stay in lane and farm. Then he will receive 300 gold and 600 experience in one minute. His opponent will be absent from the lane for the entire time.

I> **Assist** is helping to kill an enemy champion in any form.

The total advantage in favor of the blue team will be the kill reward and the mid laner's farm. Then we need to subtract the jungler's fee for participating in the gank.

Here is the gold advantage for the blue team:
{line-numbers: false, format: text}
```
450 + 300 - 100 = 650
```

Here is the experience advantage for the blue team:
{line-numbers: false, format: text}
```
300 + 600 - 200 = 700
```

A team advantage of 650 gold and 700 experience is significant in the first minutes of the game. Therefore, an early successful gank can significantly impact the laning phase.

In a **mediocre** gank, the blue team's income is calculated similarly. However, we must exclude the bounty for killing the red team's mid laner from the formula.

The red mid laner will return to base to regenerate health. This will cost him one minute of missed farm.

Here is the gold advantage for the blue team:
{line-numbers: false, format: text}
```
300 - 100 = 200
```

Here is the experience advantage for the blue team:
{line-numbers: false, format: text}
```
600 - 200 = 400
```

We got a decent result. But it is unlikely that this advantage decides the outcome of the laning phase.

In the **worst case**, the red team gets the advantage. It comes from the following:

1. The red mid laner will receive the bounty for the double kill. That is 300 gold and 300 experience for each blue champion.

2. The red mid laner can stay in lane and farm. Then he will receive 300 gold and 600 experience. The blue mid laner would not receive these resources.

3. The blue team's losses will be twice 300 gold and 600 experience. This is the farm per one minute of the blue mid laner and jungler, which they would not receive.

The red team's overall advantage will come from the mid laner's gain and both blue champions' losses. We will also take into account the jungler's fee for participating in the gank.

Here is the gold advantage for the red team:
{line-numbers: false, format: text}
```
300 + 300 + 300 + 300 + 100 = 1300
```

Here is the experience advantage for the red team:
{line-numbers: false, format: text}
```
300 + 300 + 600 + 600 + 200 = 2000
```

This means that a failed gank gives the enemy team a huge advantage. After this play, the blue mid laner lost his laning phase for sure. It is tough for him to come back from such a significant gap.

Here is the summary from our calculations. The gank is beneficial for the blue jungler. But only if it leads to at least a mediocre result. To reduce the cost of participating in a gank, the blue jungler should come to the mid lane after clearing his camps. This will increase the income in case of success and slightly reduce the losses in case of failure.

Our example showed the cost of a single serious mistake in League of Legends. Either a poor plan or poor execution can cause the mistake. In other words, even a good plan does not guarantee an advantage if a player can not execute it well.

#### 2.2.2.2 Taking the dragon

Во втором примере лесник синей команды забирает [огненного дракона](https://leagueoflegends.fandom.com/ru/wiki/Огненный_дракон). Сначала он чистит свой нижний лес во второй раз. После этого выходит на эпического монстра. Так игрок использует своё время максимально эффективно.

Пусть лесником синей команды будет Xin Zhao. Он имеет 5-й уровень, когда подходит к логову дракона. Его **урон в секунду** (damage per second или DPS) составляет около 100 физического урона (AD). В этот момент у дракона 5730 здоровья. Это означает, что лесник в одиночку заберёт монстра примерно за одну минуту.

За убийство дракона лесник получит 125 золота и 150 опыта. Ещё 80 опыта даст предмет лесника. Команда получит постоянное усиление до конца партии: 3% силы атаки (attack damage или AD) и силы умений (ability power или AP). Оценим это усиление в золоте.

I> Когда команда забирает эпического монстра, его всегда должен добивать лесник. Предмет лесника даст ему дополнительные 80 опыта. Это увеличит суммарную награду за монстра для команды.

[Следующая таблица](https://wiki.leagueoflegends.com/en-us/Gold_efficiency#Basic_reference_items) даёт оценку параметров чемпиона в золоте. Согласно ей, мы получаем:

* 1 AD = 35 золота
* 1 AP = 20 золота

Xin Zhao имеет 100 AD, следовательно усиление дракона даст ему `100 * 0.03 = 3` AD. Эта прибавка равна `3 * 35 = 105` золота. Её можно взять за среднее значение для всех AD чемпионов в команде.

AP чемпион к этому моменту будет иметь максимум два предмета [Amplifying Tome](https://wiki.leagueoflegends.com/en-us/Amplifying_Tome). Поэтому его суммарное AP составит `20 + 20 = 40`. Усиление дракона даст чемпиону `40 * 0.03 = 1.2` AP. Это равно `1.2 * 20 = 24` золота.

Посчитаем среднее усиление для всех AP и AD чемпионов в команде:
{line-numbers: false, format: text}
```
5 * (105 + 24) / 2 = 322.5
```

То есть усиление красного дракона даст всей команде около 300 золота в начале партии. Таким образом, когда лесник в одиночку убил красного дракона, команда заработала 425 золота и 230 опыта. Часть награды получил сам лесник, а часть — его союзники.

Соотнесём награду лесника с его обычным фармом монстров в течение минуты: 300 золота и 600 опыта. Получается, что за взятие дракона лично он заплатил `300 - 125 - 105 = 70` золота и `600 - 150 - 80 = 370` опыта. Его команда получила в сумме 240 золота.

Можно сделать вывод, что лесник потерял примерно половину уровня за взятие дракона. Суммарный доход команды получился скромным. Из этого следует, что взятие дракона — это долгосрочное вложение лесника в свою команду. Оно не даёт немедленной выгоды. Но на поздней стадии игры усиление дракона станет значительным преимуществом при пересчёте на золото.

Рассмотрим худший сценарий взятия дракона. Допустим, что леснику синей команды помогает его мидлейнер и ADC. В этом случае они забирают дракона примерно за 20 секунд. Ещё 10 секунд они потратят, чтобы вернуться на свои линии. Их суммарная плата по золоту за участие в командном действии составит:
{line-numbers: false, format: text}
```
150 + 150 + 150 = 450
```

Плата по опыту будет такой:
{line-numbers: false, format: text}
```
300 + 300 + 300 = 900
```

На начальной стадии игры это серьёзное вложение. Как мы посчитали, команда получит за дракона 425 золота и 230 опыта. То есть награда скомпенсирует золото, но не опыт.

Теперь допустим, что лесник красной команды ждёт в засаде, пока синие чемпионы бьют дракона. Когда у него остаётся мало здоровья, красный лесник добивает монстра [заклинанием кара](https://leagueoflegends.fandom.com/ru/wiki/Кара_(Заклинание)) (smite) и выживает после этого. В этом случае синие чемпионы не компенсируют свою плату за участие в командном действии.

Посчитаем, какое преимущество получила красная команда. Оно складывается из следующего:

1. Плата синих чемпионов за участие в командном действии.

2. Награда за дракона: золото плюс усиление.

Перевес по золоту получится такой:
{line-numbers: false, format: text}
```
450 + 425 = 875
```

Перевес по опыту получится следующий:
{line-numbers: false, format: text}
```
900 + 230 = 1130
```

Это означает, что кража дракона даёт противнику большое преимущество. В начале партии оно особенно значительно.

Из нашего примера можно сделать несколько выводов:

1. Чем больше чемпионов участвует в командном действии и чем дольше оно длится, тем дороже это обходится для команды.

2. Брать эпических монстров надо максимально быстро. Это уменьшает шанс вмешательства вражеской команды, если она не готова действовать с самого начала.

3. Неудачное командное действие даёт противнику большое преимущество. Чем выше плата за участие в нём, тем выше цена ошибки.

#### 2.2.2.3 Destruction of the tower

В третьем примере команда разрушает вражескую башню. За это она получает награду золотом, но не опытом. Сначала рассмотрим, как работает эта награда.

На иллюстрации 2-1 отмечены разные типы башен: T1, T2, T3 и T4. Тип башни определяет награду за её разрушение. Таблица 2-6 приводит конкретные цифры.

{caption: "Таблица 2-6. Награда за разрушение башен", width: "100%"}
| Обозначение башни | Название башни | Глобальное золото | Локальное золото | 
|  | | | |
| :---: | --- | :---: | --- |
|  | | | |
| T1 | Внешняя башня | 50 | 250 |
|  | (Outer turret) | | |
|  | | | |
| T2 | Внутренняя башня | 25 | • 425 на средней линии |
|  | (Inner turret) | | • 675 на верхней и нижней линии |
|  | | | |
| T3 | Башня ингибитора | 25 | 375 |
|  | (Inhibitor turret) | | |
|  | | | |
| T4 | Башня Нексуса | 50 | 0 |
|  | (Nexus turret) | | |

За уничтожение башни команда получает два типа награды: глобальное и локальное золото. **Глобальное золото** получают все чемпионы, включая убитых в данный момент. **Локальное золото** делится поровну между чемпионами, которые находятся в радиусе 1200 от разрушенной башни. Если чемпион нанёс ей урон в течение 10 секунд перед разрушением, он тоже получает локальное золото. В этом случае награда не зависит от расстояния до башни.

Внешние башни имеют механику пластин [**turret plating**](https://wiki.leagueoflegends.com/en-us/Turret#General). Она работает так. Весь уровень здоровья башни делится на пять частей. Каждая часть соответствует 1000 единиц здоровья. В сумме это 5000 здоровья. За уничтожение каждой пластины чемпион получает награду 125 локального золота. После этого башня получает дополнительную броню и сопротивление магии на 20 секунд. На 14-й минуте пластины пропадают и награду за них больше нельзя получить.

Награду за башни и пластины следует учитывать при расчёте ресурсов. Это важный источник дохода. Он может дать команде значительное преимущество.

Вернёмся к нашему примеру. Допустим, что синяя команда забирает барона Нашора. Красная команда пытается этому помешать. В результате происходит сражение. В нём погибают три красных чемпиона и два синих. Тогда красные отступают, а синие добивают барона Нашора.

Три выживших игрока синей команды выбирают действие перед recall. Для простоты предположим, что у них есть только два варианта:

1. Преследовать двух выживших красных чемпионов.

2. Разрушить вражескую T2 башню на верхней линии.

Посчитаем награду синей команды за преследование. За каждого убитого красного чемпиона она получит 300 золота плюс 150 золота за ассист. В сумме это даст 450 золота. Награда по опыту составит 300.

Максимальная награда по золоту за двух чемпионов составит:
{line-numbers: false, format: text}
```
450 + 450 = 900
```

Без ассистов награда по золоту будет меньше:
{line-numbers: false, format: text}
```
300 + 300 = 600
```

Награда по опыту не зависит от ассистов и будет следующей:
{line-numbers: false, format: text}
```
300 + 300 = 600
```

Теперь посчитаем награду синей команды за разрушение T2 башни на верхней линии. Каждый синий чемпион получит 25 глобального золота. Те кто разрушил башню, разделят 675 локального золота. В сумме для всей команды это даст:
{line-numbers: false, format: text}
```
25 * 5 + 675 = 800
```

Какой из двух вариантов выгоднее для синей команды? Если преследование закончится двумя убийствами с ассистами, оно даст больше. Но с этим связан риск: оба красных чемпиона могут уйти. Тогда синяя команда потеряет время и ничего не получит. Вероятнее всего, погоня закончится только одним убийством. Красный чемпион останется, чтобы выиграть время для союзника и дать ему уйти. В этом случае синяя команда получит только 450 золота и 150 опыта.

Награда за разрушение башни надёжнее. Два красных чемпиона с истощенными ресурсами не смогут её защитить. Поэтому синяя команда гарантированно получит 800 золота за башню. Эта награда выше, чем вероятный результат преследования в 450 золота и 150 опыта. Поэтому синей команде выгодно атаковать башню, а не преследовать противников.

Может возникнуть вопрос: почему синяя команда не может сначала преследовать противника, а потом разрушить башню? Проблема в том, что на преследовании синие потеряют темп. Трое красных чемпионов, убитых на бароне,  возродятся. Они быстро вернутся на карту, потому что противник находится около их базы. Тогда трое синих чемпионов окажутся в меньшинстве и с истощёнными ресурсами. Они могут попасть в окружение под башней и погибнуть.

Когда команда имеет темп, она должна решить, как именно его реализовать. Обычно это выбор одного действия из нескольких вариантов. Когда оно исполнено, очередь хода переходит к противнику.

I> Опытные игроки рекомендуют делать только один командный ход за раз. Несколько параллельных плэев распыляют ресурсы команды и часто заканчиваются неудачно.

### 2.2.3 Practice of resource calculation

Мы рассмотрели три примера расчёта ресурсов. Может показаться, что этот навык нужен только леснику. Обычно именно он начинает командные действия вокруг объектов на стадии лейнинга. Поэтому леснику важно просчитывать, к чему они могут привести.

На самом деле, навык расчёта ресурсов нужен каждой роли. Вот примеры нескольких ситуаций:

1. Топлейнер собирается помочь леснику взять герольда. Он должен посчитать, сколько ресурсов за это заплатит.

2. Мидлейнер собирается ганкать нижнюю линию. Он должен оценить выигрыш команды по ресурсам от удачного ганка и потери от неудачного.

3. ADC собирается помочь леснику взять дракона. Он должен посчитать, сколько ресурсов за это заплатит.

4. Саппорт собирается ганкать среднюю линию. Он должен оценить выигрыш по ресурсам за успех и потери за неудачу.

В каждом из этих случаев предварительный расчёт покажет, насколько выгодно планируемое действие. Если риск велик, а выгода — нет, игроку стоит отказаться от участия в командном действии.

Чтобы научиться считать ресурсы, игроку придётся концентрировать на этом своё внимание. Во время игры внимание в дефиците. Поэтому лучше начать тренироваться при просмотре реплеев или стримов.

Для качественного самокоучинга новичкам не хватает знаний. Расчёт ресурсов — это универсальный метод для оценки качества решений. Рассмотрим на примере, как его применять.

I> [**Outplayed**](https://www.overwolf.com/app/overwolf-outplayed) — одно из лучших приложений для записи реплеев. Они сохраняются на диске в формате MP4 и не требуют клиента игры для просмотра. Поэтому вы можете смотреть реплеи, пока стоите в очереди на следующую игру.

Допустим, что вы смотрите свой реплей и проводите сессию самокоучинга. Во время партии есть явные моменты, когда вы принимаете решения. Обычно они касаются участия в предстоящем командном действии. Например, ваш лесник пингует помощь на драконе. Остановите реплей в этот момент. Посчитайте, сколько ресурсов ваша команда получит за успешное взятие дракона. Вычтите из этого свою плату за участие. Посчитайте также, сколько команда потеряет, если противник будет контестить дракона и заберёт его.

Когда у вас есть оценки результатов, спросите себя — оправдано ли ваше участие в командном действии? Стоит ли риск возможной выгоды? Сравните свои расчёты с дальнейшими событиями в реплее. Это даст мгновенную обратную связь. Если ваши расчёты разошлись с фактическими результатами, найдите в них ошибку.

Привычка рассчитывать ресурсы заставит вас внимательнее относиться ко времени. Игроки платят недополученными ресурсами за участие в любом командном действии. Поэтому его длительность определяет выгоду для команды. Например, взятие дракона за 30 секунд даст команде преимущество. Но то же самое действие, выполненное за минуту, даст преимущество противнику. Учитывайте это в своих играх.

Во время просмотра реплеев обращайте внимание, сколько времени вы тратите на принятие решений. Это может быть выбор предмета в магазине или планирование следующего действия на карте. Подсчитайте, сколько всего времени за партию вы стояли на месте и думали. Переведите это время в недополученные ресурсы. Если получилось много, вам стоит поработать над этой проблемой.

Чтобы научиться принимать решение быстрее, вам нужно накопить больше шаблонов типичных игровых ситуаций. Расчёт ресурсов поможет находить правильные действия в них. Таким образом вы сможете запомнить, как признаки ситуации, так и подходящую реакцию на неё. В следующий раз, когда вам встретится аналогичная ситуация, вы сразу примете правильное решение.

Чтобы эффективнее запоминать шаблоны ситуаций, их лучше документировать. Текстовые заметки для этого не подходят. Например, вы можете записать: "не забирать дракона, когда у команды нет темпа". Это хороший совет, но для него нужны признаки конкретной игровой ситуации.

Шаблоны типичных ситуаций в League of Legends визуальные. Поэтому лучшая документация для них тоже визуальная. Делайте скриншоты из реплеев, которые демонстрируют конкретные шаблоны. Например, это может быть ошибка, которую вы хотите запомнить и больше не повторять. Шаблоном также может быть ваше или чужое хорошее действие.

I> [**Greenshot**](https://getgreenshot.org/) — удобная программа для сохранения скриншотов. Она имеет встроенный графический редактор, чтобы добавлять обозначения и текст.

Давайте файлам со скриншотами говорящие названия, например "не-брать-дракона-без-темпа.png". Регулярно просматривайте свои скриншоты, чтобы освежить в памяти знакомые шаблоны. Таким образом вы будете постепенно накапливать знания об игре. Вы заметите, что перестанете допускать прежние ошибки и ваш уровень начнёт расти.

Скриншоты также полезно делать при просмотре гайдов, стримов, соревнований и коучинг сессий (своих и чужих). Сохраняйте и просматривайте все важные шаблоны, которые вам удалось распознать в контенте любого типа.

I> Подробнее тему экономики разбирает профессиональный игрок Bwipo в [следующем видео](https://www.youtube.com/watch?v=fJ-C4PEk-9Y).

{pagebreak}
