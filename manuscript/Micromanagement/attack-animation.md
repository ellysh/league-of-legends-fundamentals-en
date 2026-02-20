## 3.1 Basic attack animation

>>>R1

Every champion in League of Legends has a unique **combo**. This is a sequence of actions that increases their effect. For example, an attacking combo increases a champion's damage per second (DPS).

To perform any combo, you need to understand how to work with animation. When a player issues an action command, the champion performs specific movements to execute it. These movements are called **action animation**. Typically, each action has its unique animation.

Working with animation is a complex but important topic. Mastering it requires time and regular practice. If a player does not know how to work with animation, he cannot perform the following tasks effectively:

1. Farm jungle monsters.
2. Farm minions in the lane.
3. Participate in teamfights.
4. Win trades in lane.
5. Win duels in lane or jungle.

I> A **trade** is an exchange of damage between opponents in a lane. Each side aims to inflict more damage on the opponent than it receives in return. Such a trade is considered successful and gives the winner an advantage in dynamic resources.

In other words, working with animation enables you to acquire and utilize resources effectively. Neither is possible without this skill.

Let us start with the simplest animation — a champion's basic attack.

### 3.1.1 Attack speed

>>>R1

A [**basic attack**](https://wiki.leagueoflegends.com/en-us/Basic_attack), also known as an auto-attack or AA, is the standard way to deal damage to an enemy. Every champion can perform a basic attack. If you want to give such a command, you need to simply right-click an enemy.

The basic attack animation depends on a champion's stat called **total attack speed** (or total AS). It is made up of the following components:

1. The champion's **base attack speed** (or base AS).

2. **Bonus attack speed** (or bonus AS) per champion level.

3. Bonus AS from items.

4. Bonus AS from runes.

5. Bonus AS from abilities.

6. Bonus AS from buffs.

7. **Attack speed penalty** from debuffs.

We will calculate total attack speed (AS) using an example. Let us take the champion Ashe, with a base AS of 0.66. The champion's total AS equals the base AS at level 1 when she does not have any items, skills, attack speed runes, or buffs. This means that Ashe's total AS is currently 0.66.

Let us assume that Ashe purchases the item [Berserker's Greaves](https://wiki.leagueoflegends.com/en-us/Berserker's_Greaves). It provides a 35% bonus to AS. Then, the total AS is calculated using the following formula:
{line-numbers: false, format: text}
```
total_AS = base_AS * (1 + bonus_AS / 100)
```

When we substitute the numbers here, we get the following:
{line-numbers: false, format: text}
```
total_AS = 0.66 * (1 + 35 / 100) = 0.89
```

I> Each champion has an **attack speed ratio** (or AS ratio). This is a multiplier for bonus AS. Most champions have an AS ratio of 1. The Berserker's Greaves item gives them 35% AS. Some champions have an AS ratio less than 1 (for example, Senna and Twisted Fate). The Berserker's Greaves item gives them less than 35% AS.

We have calculated the total attack speed (total AS). It determines how long a champion will play the animation for a single basic attack. This parameter is called the **attack cooldown**. Here is the formula to calculate it:
{line-numbers: false, format: text}
```
attack_cooldown = 1 / total_AS
```

We can substitute here the numbers that we got for Ashe with the Berserker's Greaves item:
{line-numbers: false, format: text}
```
attack_cooldown = 1 / 0.89 = 1.12
```

This means that a minimum of 1.12 seconds must pass between a champion's two basic attacks. In other words, the champion would not perform the second basic attack until the cooldown has passed.

### 3.1.2 Phases of basic attack

>>>R1

We have learned how to calculate the cooldown of a basic attack. Since the basic attack is running, the champion plays a full cycle of his attack animation. This cycle consists of three phases:

1. **Windup** — the swing.

2. **Firing** — the strike or shot.

3. **Recovery** — the return to the starting position.

Let us consider how Ashe at level 1, without items, plays through these three phases. Her basic attack cooldown is 1.52 seconds:
{line-numbers: false, format: text}
```
attack_cooldown = 1 / 0.66 = 1.52
```

Figure 3-1 shows the timeline diagram for a single Ashe's basic attacks.

{caption: "Figure 3-1. The timeline diagram for Ashe's basic attacks", width: "100%"}
![Basic Attack Timeline](images/Micromanagement/ashe-attack-animation.png)

The Figure shows the time axis labeled s (seconds). There are three segments on the s-axis. Each segment corresponds to one of the three animation phases. There is a screenshot above each segment. It shows some frame from the corresponding champion animation.

Let us look at what is happening in the timeline diagram step by step:

1. At point A, the player right-clicks the target. From this moment, the champion plays the windup animation phase: drawing the bow. This phase lasts 21.93% of the basic attack total cooldown. This equals 0.33 seconds, according to the following calculation:
{line-numbers: false, format: text}
```
windup = 1.52 * 21.93 / 100 = 0.33
```

2. At point B, the champion begins the firing phase: fires an arrow at the target. This phase lasts only 3.37% of the basic attack cooldown. This equals 0.05 seconds:
{line-numbers: false, format: text}
```
firing = 1.52 * 3.37 / 100 = 0.05
```

3. At point C, the champion begins the recovery phase: draws the next arrow from the quiver. This phase lasts 74.22% of the basic attack cooldown. This equals 1.13 seconds:
{line-numbers: false, format: text}
```
windup = 1.52 * 74.22 / 100 = 1.13
```

4. At point D, the champion completes a full animation cycle. In total, 1.52 seconds have passed since the player issued the command at point A. If the champion does not receive a new command, he begins the next attack animation cycle at point D on the same target.

At any point during the A-D segment, a player can issue a movement command to the champion. The outcome of this command depends on the animation phase the champion is currently playing. There are [three possible cases](https://wiki.leagueoflegends.com/en-us/Stutter-stepping):

1. Segment A-B — the command was issued during the windup phase:

* The champion will cancel his basic attack.

* The attack target will not take damage.

* The basic attack cooldown timer will reset to zero.

* The player can launch his next auto-attack at any time. Its animation will begin with the windup phase (point A).

2. Segment B-C — the command was issued during the firing phase:

* The move command will be queued.

* The champion will perform an auto-attack.

* The attack target will take damage if the attack is melee. If the attack is ranged, the target will take damage when the projectile hits it.

* The auto-attack cooldown timer will continue to run.

* After the firing animation (point C) ends, the move command is removed from the queue. The champion will perform it instead of the recovery animation. He moves to the designated point.

* The player cannot launch his next auto-attack until its cooldown timer finishes at point D.

3. Segment C-D — the command was issued during the recovery phase:

* The champion has already performed an auto-attack.

* The attack target has already taken damage.

* The basic attack cooldown timer continues to run.

* The champion ends the recovery animation early and moves to the target location.

* The player cannot launch his next auto-attack until its cooldown timer finishes at point D.

We can draw the following conclusion from the rules for combining the two commands:

1. Canceling the windup phase is almost always a mistake. It reduces the champion's damage per second (DPS). The only time canceling is justified is when the player has detected danger and needs to retreat immediately.

2. The recovery phase always takes up the majority of the basic attack cooldown. Allowing the champion to play it is a waste of time. Instead, he should move or use an ability.

3. The most effective way to cancel the recovery phase is to issue a command while in the firing phase. Then, the champion will execute a new command immediately after firing is done.

### 3.1.3 Basic attack and move

Отмена фазы автоатаки recovery часто применяется на практике. Приём **attack move** (атака и движение) — это отмена анимации с помощью команды на движение.

I> Следующее [видео на канале Skill Capped](https://www.youtube.com/watch?app=desktop&v=-oyxOgtT33U) подробно объясняет приём attack move.

Рассмотрим временную диаграмму приёма attack move. Её демонстрирует иллюстрация 3-2.

{caption: "Иллюстрация 3-2. Временная диаграмма attack move", width: "100%"}
![Временная диаграмма attack move](images/Micromanagement/ashe-attack-move.png)

Шаги этого приёма следующие:

1. В точке A игрок даёт команду на атаку. Чемпион проигрывает фазу анимации windup.

2. В точке B чемпион начинает фазу firing.

3. На отрезке B-C или в точке C игрок даёт команду на движение. Чемпион начинает двигаться сразу после завершения анимации firing. Это происходит на отрезке C-D, который длится 1.13 секунды.

4. В точке D заканчивается таймер перезарядки автоатаки. Начиная с этого момента игрок может дать команду на следующую атаку.

Технику attack move применяют в двух случаях:

1. Чтобы преследовать противника и наносить ему урон.

2. Чтобы отступать и наносить противнику урон.

В **первом случае** приём увеличивает урон по отступающему противнику. Рассмотрим разницу между командой на атаку и приёмом attack move:

* Если дать чемпиону команду на атаку, он будет стоять на месте и проигрывать все три фазы анимации. Когда противник выйдет из радиуса атаки Ashe, она отреагирует на это только в точке D. Другими словами, она начнёт двигаться только после окончания фазы recovery.

* Если применить **attack move**, чемпион будет двигаться к противнику вместо проигрывания анимации фазы firing. Это означает, что Ashe будет реагировать на его перемещение намного быстрее.

Во **втором случае** приём уменьшает урон по отступающему чемпиону. Рассмотрим разницу между attack move и отдельными командами:

* Если игрок даёт команду на атаку, чемпион стоит на месте и проигрывает все три фазы анимации. В этом случае он просто разменивается с противником уроном. Такой размен называется [**stat check**](https://www.reddit.com/r/leagueoflegends/comments/10q7lmk/comment/j6ob8tk/). Его выигрывает тот чемпион, у которого характеристики больше.

* Игрок может дать команду на движение и только отступать. В этом случае он будет получать урон до тех пор, пока не выйдет из радиуса атаки противника. Противник при это не получит никакого урона.

* Если применить **attack move**, чемпион будет размениваться уроном с противником и при этом сохранять с ним дистанцию. Это открывает две возможности. Игрок может либо перейти только к отступлению, если проиграл трейд, либо перейти в all-in, если выиграл трейд. Ни одно из отдельных действий таких возможностей не даёт.

I> **All-in** (аллын) — активный бой до победы, в котором используются все доступные умения и средства атаки. Обычно all-in заканчивается смертью одного из участников, если это дуэль.

Когда attack move применяет чемпион дальнего боя против оппонента ближнего боя, это называется **kiting** (кайтинг). Если скорость движения чемпиона больше, противник не сможет его атаковать.

### 3.1.4 Execution of the attack move

Рассмотрим, как исполнять приём attack move. Для этого надо изменить две настройки игры и  настройку мыши.

**Первая настройка** находится во вкладке "HOTKEYS". Она называется "Player Attack Move Click". Её демонстрирует иллюстрация 3-3.

{caption: "Иллюстрация 3-3. Настройка 'Player Attack Move Click'", height: "50%"}
![Настройка Player Attack Move Click](images/Micromanagement/options-player-attack-move-click.png)

Эта горячая клавиша даёт команду на движение в указанную точку. Как только в радиусе атаки окажется противник, чемпион начнёт его атаковать. Назначьте для этого действия клавишу A. Тогда при её нажатии чемпион будет атаковать ближайшую к нему цель, если она находится в радиусе атаки.

**Вторая настройка** находится во вкладке "GAME" и называется "Attack move on cursor". Её демонстрирует иллюстрация 3-4.

{caption: "Иллюстрация 3-4. Настройка 'Attack move on cursor'", width: "100%"}
![Настройка Attack move on cursor](images/Micromanagement/options-attack-move-on-cursor.png)

Эта настройка делает следующее:

* Включить — команда attack move (клавиша A) выбирает цель, ближайшую к курсору мыши.

* Выключить — команда attack move (клавиша A) выбирает цель, ближайшую к чемпиону.

Включите эту настройку. Тогда вы сможете выбирать цель для атаки с помощью положения курсора мыши.

**Третья настройка** — выключить ускорение мыши в настройках ОС. Для пользователей Windows 11 шаги выглядят так:

1. Нажмите "Пуск" (Start) -> "Параметры" (Settings). Откроется окно "Параметры" (Settings).

2. В левом меню выберите пункт "Bluetooth и устройства" (Bluetooth & devices).

3. В правой части окна выберите пункт "Мышь" (Mouse). Откроется меню настройки мыши.

4. Выключите опцию "Включить повышенную точность установки указателя" (Enhance pointer precision).

Иллюстрация 3-5 демонстрирует выключение ускорения мыши.

{caption: "Иллюстрация 3-5. Настройка 'Включить повышенную точность установки указателя'", width: "100%"}
![Настройка Enhance pointer precision](images/Micromanagement/mouse-acceleration-disable.png)

Эта настройка управляет ускорением мыши. Если оно включено, то положение указателя зависит от двух факторов:

1. Расстояние на которое вы переместили мышь.

2. Скорость с которой вы двигали мышь.

Это удобно при работе на больших мониторах. Но ускорение сильно мешает развивать мышечную память во всех компьютерных играх. Поэтому опцию надо выключить. Тогда положение указателя будет зависеть только от расстояния на которое вы переместили мышь.

Теперь рассмотрим, как исполнить приём attack move с новыми настройками. Для этого выполните следующие шаги:

1. Приблизьте курсор мыши к цели. Его необязательно наводить точно на цель.

2. Нажмите горячую клавишу A. Чемпион начнёт выполнять фазу windup анимации атаки.

3. Переместите курсор мыши в точку, куда должен двигаться чемпион. Это должно быть направление на противника или от него.

4. Когда чемпион начнёт фазу firing или recovery, нажмите правую кнопку мыши. Чемпион будет двигаться в указанную точку.

5. Считайте в уме таймер перезарядки автоатаки. Когда он закончится, начните следующую атаку с шага 1.

При исполнении attack move игроки совершают следующие типичные ошибки:

* Дают команду на движение слишком рано. Если она попадёт на фазу windup, то отменит атаку чемпиона. Это сильно уменьшает его DPS.

* Дают чемпиону двигаться дольше, чем идёт таймер перезарядки атаки. Это мешает реализовать высокую скорость атаки чемпиона.

Тренируйте приём attack move в режиме "Practice tool". Почувствуйте ритм атаки своего чемпиона на разных уровнях и с разными предметами. Тогда вы научитесь атаковать точно в момент окончания таймера перезарядки.

Обратите внимание на связь между скоростью атаки и характером передвижения чемпиона. При низкой скорости атаки, чемпион двигается длинными отрезками. При высокой скорости атаки эти отрезки укорачиваются.

### 3.1.5 Basic attack and using an ability

Мы рассмотрели отмену анимации атаки командой на движение. Это только один из четырёх способов. Вот полный список действий, которые отменяют анимацию атаки:

1. Движение
2. Умение чемпиона
3. Заклинание призывателя
4. Активный эффект предмета.

Рассмотрим второй вариант: отмена анимации атаки умением чемпиона. Назовём этот приём аналогично первому варианту — **attack ability** (атака и умение). Третий и четвёртый варианты работают аналогично ему.

Иллюстрация 3-6 показывает временную диаграмму, когда умение чемпиона отменяет анимацию атаки.

{caption: "Иллюстрация 3-6. Временная диаграмма отмены анимации атаки умением", width: "100%"}
![Временная диаграмма отмены анимации атаки умением](images/Micromanagement/ashe-attack-ability.png)

Шаги этого приёма следующие:

1. В точке A игрок даёт команду на атаку. Чемпион проигрывает фазу анимации AA windup.

2. В точке B чемпион начинает фазу AA firing.

3. На отрезке B-C или в точке C игрок даёт команду применить умение W. Чемпион начинает выполнять его анимацию сразу после завершения фазы AA firing. Это происходит на отрезке C-D и далее.

4. В точке D заканчивается таймер перезарядки автоатаки. Начиная с этого момента игрок может дать команду на следующую атаку.

Приём attack ability применяют, когда нужно выдать максимальный урон в единицу времени (DPS). При этом цель находится в радиусе атаки и умений. Это особенно хорошо работает по обездвиженной цели. Если цель двигается и разрывает дистанцию, игроку придётся чередовать приёмы attack move и attack ability.

### 3.1.6 Execution of the attack ability

Чтобы эффективно исполнять приём attack ability, надо переключить все умения чемпиона на "Quick Cast". Эта настройка находится на вкладке "HOTKEYS". Её демонстрирует иллюстрация 3-7.

{caption: "Иллюстрация 3-7. Настройка 'Quick Cast All'", width: "100%"}
![Настройка Quick Cast All](images/Micromanagement/quick-cast.png)

На вкладке "HOTKEYS" нажмите кнопку "Quick Cast All". Тогда чемпион применит умение, как только вы отпустите соответствующую кнопку (например, W). Вам больше не нужно нажимать её дважды. Это значительно ускоряет действия в игре, но к этой настройке надо привыкнуть.

Обратите внимание, что некоторые умения с [**зарядкой**](https://leagueoflegends.fandom.com/ru/wiki/Подготовка) (charging) не стоит настраивать на Quick Cast. Если чемпион может двигаться во время зарядки, его позицию можно сменить заклинанием призывателя [скачок](https://leagueoflegends.fandom.com/ru/wiki/Скачок_(заклинание_призывателя)) (flash). Зажимать клавишу Quick Cast умения и одновременно использовать скачок неудобно. Легче когда умение настроено на Normal Cast (по-умолчанию). Вот примеры умений, которым не нужен Quick Cast: Vi Q, Viego W.

Теперь рассмотрим, как исполнить приём attack ability с настройкой умений на Quick Cast. Для этого выполните следующие шаги:

1. Приблизьте курсор мыши к цели. Его необязательно наводить точно на цель.

2. Нажмите горячую клавишу A. Чемпион начнёт выполнять фазу windup анимации атаки.

3. Наведите курсор мыши так, чтобы умение попало в цель.

4. Когда чемпион начнёт фазу firing или recovery, нажмите кнопку умения. Чемпион применит его вместо того, чтобы проигрывать анимацию recovery.

Типичная ошибка при исполнении этого приёма: применить умение на фазе windup анимации атаки. Тогда чемпион отменит атаку и использует умение. Это сильно уменьшает его DPS и может сломать комбо.

Тренируйте приём attack ability в "Practice tool". Постарайтесь запомнить две вещи на вашем основном чемпионе:

1. Как выглядит анимация firing вашего чемпиона, а также её примерное время на разных уровнях и предметах. Тогда вы не будете отменять её умением.

2. Область действия всех умений. Тогда вам не придётся зажимать кнопки, чтобы проверить радиус умений. Это может сэкономить секунды, которые решат исход сражения.

{pagebreak}
