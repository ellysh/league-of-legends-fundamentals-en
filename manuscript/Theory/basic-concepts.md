## 2.1 Basic concepts

>>>R1

In this section, we will review the basic concepts of the game. It would be better to systematize them. For this purpose, the following list of questions would help us:

1. What is the initial state of objects on the map?

2. What throws objects off equilibrium?

3. What actions are beneficial?

4. How do you discover an advantage?

5. How do you gain an advantage?

6. How do you leverage an advantage to victory?

Each of these question is related to a specific game concept.

The order of the questions is important: each follows logically from the previous one. The game concepts are similarly interconnected: complex ones are based on simpler ones.

The basics always seem trivial. However, many new players have a poor understanding of them. This prevents them from mastering specific practical techniques (for example, wave management). Until a player understands the general patterns of League of Legends mechanics, information from guides will seem disjointed and chaotic. It is almost impossible to absorb information in this form.

We will examine each concept in detail to eliminate any misunderstandings.

### 2.1.1 Equilibrium

>>>R1

The first question on our list is the following:

> What is the initial state of objects on the map?

Initially, all objects on the map are in equilibrium. **Equilibrium** means balance and a stable state of the game's elements. All subsequent concepts are built on this concept.

You can easily find the equilibrium of game objects if you look on the Summoner's Rift map. Figure 2-1 demonstrates it.

I> The general structure of the map remained unchanged between Seasons 14 and 15. Some diagrams in the book are for the Season 13 map. All of them remain relevant for the new versions.

{caption: "Figure 2-1. Summoner's Rift map for Season 13", height: "50%"}
![Summoner's Rift ma](images/Theory/map-season-13-no-champions.png)

Letters and geometric shapes mark interactive objects on the map. Note that player champions are not among them. Now we exclude them for simplicity.

Map symbols are as follows:

* T1, T2, T3, T4 — [**turrets**](https://wiki.leagueoflegends.com/en-us/Turret) of each team.

* I — [**inhibitors**](https://wiki.leagueoflegends.com/en-us/Inhibitor) of each team.

* N — [**Nexus**](https://wiki.leagueoflegends.com/en-us/Nexus) of each team.

* Green circle — the neutral [**monster**](https://wiki.leagueoflegends.com/en-us/Monster) camp.

* Blue rectangle — the [**minion**](https://wiki.leagueoflegends.com/en-us/Minion) (creep) wave of blue team.

* Red rectangle the minion wave of red team.

You can see three forms of equilibrium on the map:

1. Landscape equilibrium.

2. Resource equilibrium.

3. Teams power equilibrium.

**Landscape equilibrium** refers to the geometry of the map and all static objects on it: walls, bushes, buildings, and roads (lanes). Figure 2-1 shows that these objects are symmetrical about the center of the map.

Here are some examples of landscape equilibrium:

* The blue team's base is in the lower left corner. The red team's base is symmetrical about the center of the map and is in the upper right corner.

* The blue team's jungle with [Red Brambleback](https://wiki.leagueoflegends.com/en-us/Red_Brambleback) (red buff) is at the bottom. The same jungle of the red team is at the top, symmetrical to the map center. The same is true for both jungles with [Blue Sentinel](https://wiki.leagueoflegends.com/en-us/Blue_Sentinel) (blue buff).

* The [baron pit](https://wiki.leagueoflegends.com/en-us/Baron_pit) is located on the upper river. The [dragon pit](https://wiki.leagueoflegends.com/en-us/Dragon_pit) is on the lower river, symmetrical to the map center.

* Each blue team structure has a red team structure that is symmetrical about the center.

**Resource equilibrium** means the resources available to both teams. This refers to what they already possess and what they can potentially acquire on the map.

There are a number of objects on the map that grant rewards when destroyed. The first example is neutral monsters. They are marked by green circles on Figure 2-1. Note that each green circle has a symmetrical counterpart relative to the center of the map. This means that teams can potentially earn equal amounts of resources in the jungle.

Enemy minions are another source of income. Every 30 seconds, each Nexus spawns the same number of minions. This means both teams have the potential to kill the same number of minions.

We can consider all buildings like resources too. Destroying an enemy building grants a reward. Thanks to the landscape equilibrium, these resources are also equal for both teams.

**Teams power equilibrium** applies to all of their units: towers, inhibitors, the Nexus, minions, and champions. Towers, inhibitors, and the Nexus are immobile structures. They are subject to landscape equilibrium and are symmetrical about the map's center. This means teams have an equal number of each type of structure.

Minions are mobile units. They represent both team power and enemy resources. Minions move in groups called **waves**. Waves spawn near Nexuses at regular intervals. The first wave occurs at 1:05 game time and repeats every 30 seconds.

Three waves of minions spawn simultaneously on each side. They move along three lanes: top, middle, and bottom. These lanes connect the teams' bases. On each lane, the blue and red waves of minions meet exactly in the middle. Then they fight each other.

Minion waves are in equilibrium. If their clash front is in the middle of the line, it would not move. Its position will remain constant, as Figure 2-1 shows. This happens because each successive wave arrives just as the last minions of the previous wave die.

Champions are also mobile units. They are the primary units of each team. If a champion becomes too weak relative to opponents, he can no longer contribute to the game. Then the champion becomes a resource for the enemy team, like a minion.

We have considered three forms of equilibrium for game objects. Each of these forms is dynamic. It means that if something disturbs the equilibrium of objects, they will recover to its original state over time. Let us look at some examples.

Some champions' abilities can disrupt the **landscape equilibrium**. They create new walls (Anivia W) or passages (Bard E). This disrupts the balance of static objects. However, the effect of such abilities is limited in time. The landscape returns to its original state after a few seconds.

When a player destroys some object, he disrupts the **resource equilibrium**. First, the player receives a reward that the enemy does not have. Second, the destroyed object disappears from the map. For example, after killing a jungle monster, its camp will empty. However, after a certain amount of time, the monster will reappear at its camp. The respawn time depends on the monster type and lasts from 2 to 6 minutes.

The dynamic balance of power between teams is more complex. First, only some structures can regenerate after being destroyed. Second, the minion collision front can move along the line. If it deviates from the line's center, it eventually returns. We'll discuss this mechanic in more detail in section "4.1 Minion Wave Management."

The dynamic **equilibrium of power** between teams is more complex. First, only some structures can recover after being destroyed. Second, the minion collision front can move along the line. If it deviates from the line's center, it eventually returns. We will discuss this mechanic in more detail in section "4.1 Minion wave management."

### 2.1.2 Action

>>>R1

Here is the second question on our list:

> What throws objects off equilibrium?

Player champions are the only thing that can disrupt any form of equilibrium of game objects. Even their presence on map changes teams balance. This happens because players cannot select the same champion.

When a champion performs some action, it affects a game object and changes its state. This disrupts one of the three forms of equilibrium.

We can divide all possible champion's actions into two categories: micro and macro. The most basic actions fall into the **micro-level** and pursue short-term goals. Here are a few examples:

* Move a few steps back to avoid an incoming projectile.

* Use a crowd control (CC) skill on an enemy to stop him.

A sequence of micro-level actions compiles into a single **macro-level** action. It is aimed at achieving a longer-term goal. For example, a champion uses auto-attacks and abilities to quickly kill enemy minions. This is one macro action, called pushing a lane.

Here is a list of basic macro-level actions that disrupt the balance of game objects:

1. Attacking enemy minions.
2. Attacking an enemy champion.
3. Attacking an enemy tower.
4. Attacking an enemy inhibitor, if possible.
5. Attacking the enemy Nexus, if possible.
6. Attacking jungle monsters.

A sequence of basic macro actions combines into a single complex macro action. It is aimed at executing a plan with several steps. Here are examples of such actions:

* Split push to create a threat on the side lane and gain map control.

* Siege the enemy base from two directions to destroy one of the inhibitors.

Each player has a task to select and execute the most advantageous macro action at the given moment. This action should disrupt any type of equilibrium in favor of the player's team. This way, he increases his team's chances of winning.

### 2.1.3 Game scenario

>>>R1

We have considered actions of player champions. It is important to emphasize that players act within strict boundaries. They are dictated by the game's design and balance. The developers want each game to follow a specific scenario. Therefore, they adjust the parameters of game objects to ensure that players benefit from following that scenario.

Let us look on how a typical rating game scenario looks like. We can divide it into three phases:

1. Laning – the beginning.

2. Mid game – the middle.

3. Late game – the end.

The **laning** phase begins at the first second and lasts until approximately the 14th minute. It ends when players destroy the first tower on any lane. The teams' goals during this phase are to gather resources and prevent the enemy from doing the same.

During the laning phase, players are distributed across the map to maximize their income. The resources are enemy minions and jungle monsters. Therefore, at least one champion should occupy each lane and jungle.

The standard champion distribution across the map in the laning phase looks like this:

1. One player goes to the top lane.

2. One player goes to the mid lane.

3. Two players (the ADC and the support) go to the bottom lane.

4. One player goes to the jungle.

Typically two players occupy bot lane. One of them is a support. He does not kill minions. Instead, he has a special item that provides him gold in a different way.

The **mid game** phase typically begins at the 14th minute and lasts until the 25th minute. It ends around the time when players collect their third item. Teams' goals during this stage are following:

1. Map control.

2. Capturing objectives.

I> An **objective** is an epic jungle monster or enemy structure. Destroying one increases the team's strength or provides a significant reward. Objectives include dragons, Herald, Baron Nashor, Voidgrubs, enemy towers, and inhibitors.

When the mid game phase begins, players swap their lanes. The standard swap looks like this:

1. The ADC moves from the bot lane to the mid lane.

2. The top laner moves from the top lane to the bot lane.

3. The mid laner moves from the mid lane to the top lane.

These swaps allows the team to better control the map. The champions' abilities for each role dictate which lane they should occupy during the mid game. We will cover this topic in more detail in section "4.2 Map Control."

During the mid game, champions often leave their lanes and group together. This helps them to contest objectives more effectively.

I> **Contest** is a battle between teams for a specific object on the map: a building or an epic monster.

The late game phase begins around the 25th minute. By this time, players usually have destroyed all T1, T2, and T3 towers on one or more lanes

The teams' goals in the late game are following:

1. Win decisive team fights.

2. Capture epic monsters.

3. Destroy structures on enemy base (T3 and T4 towers, inhibitors, Nexus).

Teams frequently clash in five-on-five fights during the late game. The outcome of these fights determines who will take the next epic monster. Victory in the decisive teamfight allows to destroy the enemy T4 towers and Nexus.

### 2.1.4 Advantage

Мы переходим к третьему вопросу, который звучит так:

> Какие действия являются выгодными?

Чтобы ответить на него, обратимся к примеру. Допустим, что начинается стадия лейнинга. Оба мидлейнера находятся на средней линии. Каждую секунду игроки выбирают и исполняют какое-то действие. Ограничим выбор только средней линей. Тогда варианты будут следующими:

1. Атаковать вражеского чемпиона
2. Атаковать вражескую башню
3. Фармить вражеских миньонов
4. Отойти в безопасную зону под свою башню.

Пусть на средней линии будет равновесие сил. Это означает, что фронт столкновения миньонов находится посередине линии. Их количество одинаково с каждой стороны. Также здоровье, мана, уровни и предметы обоих чемпионов равны.

Рассмотрим варианты действий с точки зрения мидлейнера синей команды. **Во-первых**, атака вражеского чемпиона ведёт к риску из-за равенства сил. Примерно в 50% случаев игрок сможет его убить. Тогда он получит опыт и золото. В других 50% случаев игрок погибнет. Таким образом он отдаст противнику опыт и золото. Это означает, что действие "атаковать вражеского чемпиона" невыгодное. Оно не увеличивает шансы команды на победу.

**Во-вторых**, мидлейнер не может атаковать башню без поддержки миньонов. Они должны принимать на себя атаки башни, пока чемпион её атакует. В противном случае башня быстро убьёт чемпиона. Поэтому нападение на башню в текущей ситуации будет невыгодным.

**В-третьих**, фарм вражеских миньонов — это стандартное действие на фазе лейнинга. Оно сохраняет равновесие по ресурсам между игроками на линии. Если синий мидлейнер лучше добивает миньонов, он получит преимущество с минимальным риском. В данной ситуации это будет наилучшим действием.

**В-четвертых**, отход в безопасную зону означает отказ от фарма. В результате противник будет фармить и получить преимущество по ресурсам. Это невыгодное действие, которое увеличит шансы вражеской команды на победу.

Теперь допустим, что ситуация меняется. К мидлейнеру синей команды подходит его лесник. Тогда шансы атаковать и убить красного чемпиона возрастают. Это становится выгодным действием.

Что произошло в нашем примере, когда пришел синий лесник? Синяя команда получила численное преимущество на средней линии. Преимущество — это вторая фундаментальная концепция. Она следует из понятия равновесия.

Команда получает **преимущество** (advantage), когда любая из форм равновесия смещается в её пользу. Преимущество может получить не только команда, но и отдельный игрок. Когда равновесие на линии смещается в его пользу, он получает преимущество.

Преимущество бывает разного типа. Он зависит от того, какая из форм равновесия была нарушена. Опытные игроки различают следующие типы преимущества:

1. **Численное** — в сражении со стороны одной команды участвует больше чемпионов, чем с другой.

2. **По предметам** — у одного или нескольких чемпионов команды предметов больше или они дороже, чем у оппонентов.

3. **По уровню** — у одного или нескольких чемпионов команды уровень выше, чем у оппонентов.

4. **По ресурсам** — у одного или нескольких чемпионов команды есть что-то из следующего, когда у оппонентов этого нет:

   * здоровье

   * мана

   * готовые [**заклинания призывателя**](https://leagueoflegends.fandom.com/ru/wiki/Заклинание_призывателя) (summoner spell)

   * готовые умения, особенно [**абсолютное умение**](https://leagueoflegends.fandom.com/ru/wiki/Умение_чемпиона) (ultimate)

   * индивидуальные или командные [**усиления**](https://leagueoflegends.fandom.com/ru/wiki/Усиление), полученные за убийство лесного монстра.

5. **Контроль карты** означает иметь обзор и влияние в её ключевых областях. Обзор дают специальные предметы — [**варды**](https://leagueoflegends.fandom.com/ru/wiki/Тотем) (ward). Влияние появляется, когда чемпионы находятся в зоне доступности от ключевых точек карты. Эту концепцию мы рассмотрим в разделе "4.2 Контроль карты".

6. **Позиционное преимущество** означает более выгодное расположение чемпиона на линии или команды перед сражением. Примеры: обход с фланга, контроль узких мест карты, вытеснение (zoning) противника из какой-то области.

7. **По составу команды** — чемпионы одной стороны лучше взаимодействуют и усиливают друг друга, чему у противников.

8. **По темпу**. Мы рассмотрим концепцию темпа далее.

Обратите внимание, что команда может иметь сразу несколько типов преимущества. При этом у оппонентов тоже может быть преимущество, но в других аспектах.

Рассмотрим пример. Пусть у синей команды сильнее состав чемпионов и лучший контроль карты. У красной команды есть усиление [**старшего дракона**](https://leagueoflegends.fandom.com/ru/wiki/Старший_дракон). В этом случае усиление дракона станет решающим преимуществом. **Решающее преимущество** (decisive advantage) — нарушает равновесие сил команд или чемпионов на линии больше, чем другие типы преимущества.

Обратите внимание, что важность каждого типа преимущества зависит от текущего состояния партии. Например, на стадии лейнинга преимущество по уровню важнее, чем по предметам. Это правило справедливо до тех пор, пока чемпионы не получат 6-й уровень. Поэтому в таких условиях преимущество по уровню будет решающим. После 6-го уровня предметы дают больше и становятся решающим преимуществом.

Вернёмся к начальному вопросу о выгодных действиях. По убыванию выгоды они будут следующими:

1. Реализация имеющегося преимущества.

2. Действие которое, даст какой-то тип преимущества.

3. Стандартное действие.

**Реализация преимущества** — это самое выгодное действие в общем случае. Команда или отдельный чемпион уже сильнее противника. Они должны как-то это реализовать и получить что-то в награду. Пример: атака противников на объекте, когда у команды есть численное преимущество.

**Действие, которое потенциально даст преимущество** будет вторым по выгоде. Если удастся нарушить какую-либо форму равновесия в свою пользу, этим можно будет воспользоваться. Пример: атака дракона, чтобы получить его усиление.

**Стандартное действие** будет самым невыгодным в нашем списке. Обычно оно направлено на то, чтобы сохранить текущее равновесие сил. Игрок сможет получить преимущество из такого действия только тогда, когда исполняет его значительно лучше оппонента. Пример: фарминг миньонов на линии.

### 2.1.5 Macrocycle

Четвёртый вопрос звучит так:

> Как обнаружить преимущество?

Для этого игроку нужно две вещи:

1. Заучить шаблоны для распознавания типичных игровых ситуаций.

2. Эффективно управлять вниманием во время партии.

Шаблоны для разных игровых аспектов и правильные действия мы будем рассматривать дальше в каждой главе этой книги. Сейчас мы поговорим об управлении вниманием.

В **стратегиях реального времени** (real-time strategy или RTS) есть понятие макроцикла. **Макроцикл** (macro cycle) — это подход к эффективному управлению игровой экономикой. Его идея в том, чтобы составить список задач и регулярно его исполнять.

Вот пример макроцикла для типичной стратегии:

1. Производство рабочих.
2. Распределение рабочих для добычи ресурсов.
3. Производство военных юнитов.
4. Строительство новых зданий.
5. Выполнение технических улучшений.

Когда игрок следует макроциклу, он по порядку выполняет действия из списка. Достигнув последнего, игрок начинает список сначала.

Преимущество макроцикла в том, что игрок не забудет ничего важного. После многократного повторения макроцикл формирует устойчивую привычку. Если в списке есть какое-то действие, игрок обязательно его выполнит. Ему не надо тратить лишние когнитивные ресурсы на запоминание. Макроцикл позволяет в равных долях распределять внимание между всеми аспектами игры.

В любой стратегии происходят случайные события. Некоторые из них требуют полного внимания игрока. После решения возникшей проблемы, игрок должен начать макроцикл по новой. Это его режим работы по умолчанию.

В League of Legends нет такой экономической составляющий, как в типичной стратегии. Игроки не строят базу и не производят новые юниты. Тем не менее, сама идея макроцикла остаётся актуальна. Потому что в игре есть много аспектов и игроку нужно распределять внимание между ними.

Среди новичков типична ошибка, когда игрок фокусирует внимание только на одном аспекте игры. Например, начинающий топлейнер смотрит только на волну вражеских миньонов. Таким образом он старается не пропустить возможность для их добивания (ластхит). При этом игрок не видит состояние своего чемпиона и противника. Он не замечает моменты, когда получает преимущество по здоровью, мане или уровню. Поэтому игрок не может реализовать такое преимущество. Макроцикл позволяет избежать подобных ошибок.

Макроцикл для каждой из пяти ролей будет отличаться. Для примера мы рассмотрим возможные макроциклы мидлейнера и лесника.

Иллюстрация 2-2 демонстрирует объекты на карте, между которыми должен переключать своё внимание мидлейнер.

{caption: "Иллюстрация 2-2. Макроцикл мидлейнера", height: "50%"}
![Макроцикл для мидлейнера](images/Theory/map-season-13-midlaner-macrocycle.png)

Это дополненная версия иллюстрации 2-1. На ней синие и красные круги отмечают чемпионов.

Рассмотрим макроцикл мидлейнера синей команды. На иллюстрации его чемпион отмечен розовым кругом. Розовый текст указывает объекты, проверка которых входит в макроцикл игрока.

Согласно иллюстрации, макроцикл мидлейнера выглядит так:

1. Состояние своего чемпиона:

   * количество здоровья
   * количество маны
   * уровень
   * готовые умения
   * предметы и готовность их эффектов.

2. Состояние оппонента на линии:

   * количество здоровья
   * количество маны
   * уровень
   * готовые умения (надо запоминать время перезарядки)
   * предметы.

3. Вражеская волна миньонов:

   * есть ли миньон для ластхита?
   * общее количество миньонов в волне
   * место нахождения следующей волны (симметрично следующей союзной).

4. Союзная волна миньонов:

   * есть ли миньон для ластхита?
   * общее количество миньонов в волне
   * место нахождения следующей волны.

5. Союзная или вражеская башня, если она находится поблизости:

   * количество здоровья и пластин
   * дальность её атаки.

6. Миникарта:

   * место расположения союзного лесника
   * место расположения вражеского лесника (нужен навык его трекинга)
   * состояние соседних линий (положение волн миньонов, наличие чемпионов на линиях)
   * состояние ближайших лагерей монстров (особенно эпических: Герольд, барон, дракон).

7. Статистика команд (scores) по клавише Tab:

   * уровни всех чемпионов
   * предметы всех чемпионов.

I> [**Перезарядка**](https://leagueoflegends.fandom.com/ru/wiki/Перезарядка) (cooldown или CD) наступает сразу после использования умения. Это время, в течение которого оно недоступно. Перезарядка есть не только у умений чемпиона, но и у рун, заклинаний призывателя и эффектов предметов.

Список приводит все аспекты партии, на которые игрок должен регулярно обращать внимание. В одном из них может возникнуть шаблон типичной ситуации. Он укажет на временное преимущество и возможность его реализовать. Шаблон невозможно заметить без переключения внимания на соответствующий аспект игры.

> Чтобы обнаружить закономерность в чём-либо, на это что-то надо посмотреть.

Рассмотрим макроцикл лесника синей команды. Эта роль отличается от остальных тем, что почти всю стадию лейнинга игрок проводит в лесу. Поэтому его макроцикл кардинально отличается от остальных.

Иллюстрация 2-3 демонстрирует объекты на карте, которые входят в макроцикл лесника.

{caption: "Иллюстрация 2-3. Макроцикл лесника", height: "50%"}
![Макроцикл для лесника](images/Theory/map-season-13-jungler-macrocycle.png)

Лесник синей команды отмечен розовым кругом. Согласно иллюстрации, его макроцикл выглядит так:

1. Состояние своего чемпиона:

   * количество здоровья
   * количество маны
   * уровень
   * готовые умения
   * предметы и готовность их эффектов.

2. Место расположения и состояние вражеского лесника (нужен навык его трекинга):

   * миникарта
   * окно статистики команд.

3. Ближайшие лагеря лесных монстров:

   * текущая цель для фарминга
   * следующая цель для фарминга.

4. Состояние линий, начиная с ближайшей:

   * положение волн миньонов
   * наличие чемпионов на линии
   * состояние чемпионов (здоровье, мана, уровень, предметы).

5. Следующий эпический монстр для взятия:

   * таймер его возрождения
   * союзные чемпионы в зоне доступности
   * вражеские чемпионы в зоне доступности.

6. Статистика команд (scores) по клавише Tab:

   * уровни всех чемпионов
   * предметы всех чемпионов.

Обратите внимание, что леснику недостаточно смотреть только на миникарту. Игрок должен переключать камеру на каждую линию и проверять, что именно там происходит. Для этого лучше использовать горячие клавиши (hotkey) F1, F2, F3, F4. [Следующее видео](https://www.youtube.com/watch?v=pizMcCWv8y8) объясняет, как их настроить.

Попробуйте постепенно ввести макроцикл в свои игры. Для этого выполните следующие шаги:

1. Составьте макроцикл из минимально необходимых действий. Для начала это может быть следующий список:

   * проверить игровые объекты на основном экране
   * проверить миникарту
   * проверить статистику команд по клавише Tab.

2. Поставьте [приложение метроном](https://play.google.com/store/apps/details?id=com.andymstone.metronome&hl=en) на 15 секунд, чтобы получать регулярный звуковой сигал.

3. При срабатывании сигнала выполняйте макроцикл. Последовательно переключайте внимание между пунктами, указанными в списке.

4. Если вас отвлекло какое-то игровое событие, сначала обработайте его. Затем вернитесь к макроциклу и начните его сначала.

Начните тренировать макроцикл в режиме "Co-op vs. AI" (против ботов). Так вам будет проще следить за переключением внимания. Постепенно минимальный макроцикл войдёт у вас в привычку. Добавьте в него действия, которые считаете важными. Постепенно сокращайте задержку между звуковыми сигналами.

Равномерно распределять внимание между аспектами игры важно для каждой роли. Для лесника это просто необходимо. Если лес — ваша основная роль, постарайтесь освоить минимальный макроцикл перед следующей рейтинговой игрой.

### 2.1.6 Tempo

Пятый вопрос был таким:

> Как получить преимущество?

Опытные игроки накапливают преимущество **от малого к большему**. Это самый надёжный способ выиграть у равного по силам противника.

Накопление преимущества начинается, когда одна из форм равновесия нарушается в пользу игрока. Он должен это заметить и воспользоваться возможностью. Часто это означает действовать по плану, в котором каждое действие даёт небольшую выгоду. Постепенно план приводит к крупному преимуществу.

Темп — это то, с чего начинают накапливать преимущество опытные игроки. Разберёмся, что означает этот термин.

В **пошаговых стратегиях** (turn-based strategy или TBS) есть понятие хода. **Ход** — это определённый момент времени, когда игроку разрешено действовать. Ходы следуют друг за другом последовательно. Каждый игрок действует в свой ход.

League of Legends — это игра в реальном времени. Её механика не ограничивает моменты, когда игроки могут действовать. Тем не менее, в игре есть понятия хода. Он называется плэй.

I> **Плэй** (play) — так называют ход команды или чемпиона опытные игроки в League of Legends.

Команда и каждый её чемпион эффективно действуют только при определённых условиях. Они складываются из имеющихся ресурсов и позиций игроков на карте. Если ресурсы есть и позиции выгодные — можно делать плэй. В противном случае команда или чемпион действовать не могут.

Условия при которых команда или чемпион могут действовать эффективно называются [**темпом**](https://wiki.leagueoflegends.com/en-us/Snowball#Qualities). Coach Kairos подробно объясняет эту концепцию в [следующем видео](https://www.youtube.com/watch?v=vHVeltI0IkE). Он даёт следующую **формулу расчёта темпа** для конкретного чемпиона:
{line-numbers: false, format: text}
```
tempo = champion power / distance from objective
```

Обозначения в формуле следующие:

* tempo — темп
* champion power — сила чемпиона
* distance from objective — расстояние до объекта.

**Первая часть формулы** — champion power (сила чемпиона). Она складывается из его ресурсов. Для удобства разделим их на два типа:

1. Статические
2. Динамические.

**Статические ресурсы** — это то, что чемпион уже получил и больше не может потерять. Примеры: уровень, предметы, золото, постоянные стаки каких-то умений.

**Динамические ресурсы** — это то, что чемпион может потратить или потерять. Примеры: запас здоровья и маны, временные усиления, готовность умений, заклинаний призывателя и эффектов предметов.

Мы говорили о равновесии игровых объектов. Одна из его форм — равновесие ресурсов, которое восстанавливается с течением времени. Очевидно, что динамические ресурсы восстанавливаются с течением времени. Например, каждый чемпион пассивно пополняет здоровье и ману, даже не возвращаясь на фонтан. Также его умения и эффекты предметов снова готовы после времени перезарядки.

Менее очевидно то, что равновесие статических ресурсов тоже восстанавливается с течением времени. Рассмотрим пример. Допустим, что мидлейнер синей команды первым получил 18-й уровень и собрал все предметы. Для его команды это большое преимущество, которое можно довести до победы. Но если партия затягивается, красная команда вернётся в игру. Спустя какое-то время её чемпионы получат 18-е уровни и соберут все предметы. Таким образом игрок, который лидировал по статическим ресурсам, потеряет преимущество через какое-то время. Тогда вместе с равновесием статических ресурсов восстановится и равновесие сил команд.

Для простоты coach Kairos предлагает учитывать статические и динамические ресурсы чемпиона из таблицы 2-1.

{caption: "Таблица 2-1. Ресурсы чемпиона для расчёта темпа", width: "100%"}
| Обозначение | Описание | Шкала |
|  | | |
| --- | --- | --- |
|  | | |
| resources | Здоровье и мана | от 1 до 3, где 2 — это половина |
|  | | |
| stats | Базовые характеристики за уровень | от 1 до 5, где 3 — равенство уровней |
|  | | |
| items | Предметы и их характеристики | от 1 до 5, где 3 — равенство предметов |
|  | | |
| cooldowns | Готовность умений, заклинаний призывателя и эффектов предметов | от 1 до 5, где 3 — означает, что некоторые CD готовы |

Формула для расчёта силы чемпиона выглядит так:
{line-numbers: false, format: text}
```
champion power = resources * (stats + items + cooldowns)
```

Обратите внимание, что resources — это множитель. Другими словами, здоровье и мана являются определяющим фактором. На низком уровне здоровья у чемпиона нет темпа, независимо от остальных его характеристик.

**Вторая часть формулы** для расчёта темпа — расстояние до объекта. Объектом может быть не только эпический монстр или вражеское строение. В контексте темпа им может быть линия для ганка, командное сражение, лагерь лесных монстров и даже волна миньонов на лини.

Обратите внимание, что темп считается для конкретного объекта на карте. Пример: пусть чемпион находится на нижней линии. Тогда его темп относительно дракона будет высоким, а относительно барона — низким.

Расстояние до объекта измеряется в секундах, чтобы его достичь. Например, если игрок на базе, но у него готово заклинание телепорта, то его расстояние до объекта будет маленьким.

Чтобы оценить расстояние, coach Kairos предлагает шкалу от 1 до 10:

* 1 — чемпион уже на объекте.
* 5 — чемпион на полпути к объекту.
* 10 — чемпион на базе или мёртв.

Рассмотрим, как использовать формулу для расчёта темпа на примере. Вычислим темп синего лесника Viego относительно дракона. Для простоты будем учитывать только лесников обеих команд и проигнорируем остальных чемпионов.

Допустим, что Viego имеет полное здоровье и ману. Тогда его resources равны 3. У него восьмой уровень, а у красного лесника — шестой. Тогда stats Viego равны 5. Пусть он собрал первый предмет, а противнику не хватает одного компонента. Тогда его items равно 4. Все умения и заклинания у Viego готовы. Поэтому cooldowns чемпиона равны 5. Он выходит на нижнюю реку из своего леса — его расстояние до объекта равно 2.

Расчёт темпа для Viego относительно дракона выглядит так: 
{line-numbers: false, format: text}
```
tempo = 3 * (5 + 4 + 5) / 2 = 21
```

Это очень высокое значение. Сравним его с темпом красного лесника Ekko, который находится в своём верхнем лесу. Расстояние до объекта для него равно 7. Пусть его ресурсы будут следующими:

* Полное здоровье и мана: resources = 3.

* Шестой уровень, когда у противника восьмой: 
 stats = 1.

* Нет первого предмета, когда у противника есть: items = 2.

* Готовы все умения и заклинания: cooldowns =  5.

Темп Ekko относительно дракона следующий: 
{line-numbers: false, format: text}
```
tempo = 3 * (1 + 2 + 5) / 7 = 3.4
```

Это очень низкое значение. Оно означает, что Ekko не может контестить дракона.

Формула от coach Kairos показывает, как можно увеличить темп. Для этого надо получить один или несколько следующих пунктов:

1. Преимущество по ресурсам (здоровье, мана).

2. Преимущество по уровню чемпиона.

3. Преимущество по предметам.

4. Преимущество по времени перезарядки умений, заклинаний и эффектов предметов.

5. Находиться близко к объекту.

Этот список работает и в обратную сторону. Если что-то из перечисленного есть у противника, то он получает темп. Соответственно, игрок теряет темп.

Coach Kairos предлагает рассчитывать темп команды, как сумму темпов её игроков. Эта формула выглядит так:
{line-numbers: false, format: text}
```
team tempo = top tempo + jungle tempo + mid tempo + adc tempo + support tempo
```

Применив эту формулу к обеим командам, можно сделать вывод — кто имеет темп на конкретном объекте. Имеющая темп команда с большей вероятностью выиграет сражение и заберёт объект.

Небольшой выигрыш по темпу можно легко получить, если занять более выгодную позицию ближе к объекту. Но преимущество по темпу меняется динамично. Оно даёт временное окно, когда команда или игрок могут действовать с преимуществом. Если эту возможность не заметить или не воспользоваться ей, то от темпа не будет пользы.

### 2.1.7 Victory condition

Последний вопрос в нашем списке следующий:

> Как довести преимущество до победы?

Мы выяснили, что есть разные типы преимущества. Также преимущество одного типа может отличаться количественно. Например, сравним разницу по золоту между командами в 1000 и в 14000. Во втором случае примерно каждый чемпион лидирующей команды опережает своего оппонента на линии на целый предмет. Это открывает гораздо больше возможностей, чем небольшое преимущество команды в 1000 золота.

Не всякого преимущество достаточно, чтобы одержать верх в партии. **Условие победы** (win condition) — это конкретный тип преимущества в достаточном количестве, чтобы гарантировать команде победу.

**Цель команды на партию** — достигнуть своё условие победы. Обратите внимание, что оно зависит от состава команды. Другими словами, разные комбинации чемпионов имеют разные условия для победы в партии.

Чтобы достичь условия победы, команде нужен **общий план на игру**. Он определяет решения и действия команды в течение партии. План строится исходя из следующих факторов:

1. Комбинация чемпионов в команде.

2. Комбинация чемпионов у противника.

3. План каждого игрока на стадию лейнинга.

**Комбинация чемпионов в команде** определяет, как они могут взаимодействовать и тем самым усилить свои возможности. В зависимости от чемпионов, надо выбирать подходящие приёмы для контроля карты и строить командные сражения.

**Комбинация чемпионов противников** показывает, какие средства есть у вражеской команды. Некоторые средства могут полностью нейтрализовать возможности команды игрока. Это надо учитывать при составлении плана.

**План игрока на лейнинг** определяет, как именно он собирается выходить в мидгейм с преимуществом. Некоторые чемпионы могут смещаться и помогать союзникам в течение лейнинга. Другие вынужденны постоянно оставаться на своей линии. В противном случае, они выйдут в мидгейм с отставанием. Это тоже надо учитывать в общем плане на игру.

В текущем балансе игры есть ряд устоявшихся типичных планов. Игроки выбирают один из них в подавляющем большинстве партий. Эти планы работают как в соревновательных играх, так и в рейтинговых на всех уровнях Эло.

Вот список типичных планов на игру:

1. **Ранняя агрессия** (early game aggression). Команда выбирает чемпионов, которые особенно сильны на стадии лейнинга. Примеры: Renekton, Lee Sin, Lucian. На равных ресурсах они сильнее оппонента на линии за счёт ранних power spike от умений. Эти power spike позволяют убивать противников и получать ранее преимущество по ресурсам. План на игру заключается в том, чтобы накапливать преимущество от малого к большему.

I> **Power spike** (пик силы) — момент в игре, когда конкретный чемпион становится значительно сильнее. Это происходит после достижения определённого уровня или приобретения ключевого предмета.

2. **Скейлинг в лейтгейм** (late game scaling). В команде есть минимум один гиперкерри чемпион. Примеры: Kayle, Jinx, Smolder, Aurelion Sol. Он слаб в начале партии, но становится очень сильным в лейтгейме. План заключается в замедлении игры и получении с карты равных ресурсов с противником. Те же ресурсы дают гиперкерри более сильные power spike, чем другим чемпионам. Тогда в мидгейме он начинает доминировать в командных сражениях. Игра всей команды строится вокруг гиперкерри.

I> **Scaling** (скейлинг или масштабирование) — это увеличение силы чемпиона в результате получения ресурсов и с течением времени.

I> **Carry** (кэри) — это чемпион с хорошим масштабированием умений от AD или AP. После приобретения нескольких предметов он становится основным источником урона в команде. Его участие в сражении — это решающий фактор.

3. [**Сплит-пуш**](https://leagueoflegends.fandom.com/wiki/User_blog:Fistful_of_Force/Split_push.) (split push) — это давление одного чемпиона на боковой линии. План заключается в том, чтобы создавать угрозу разрушения башни или ингибитора. Противники будут вынуждены на неё реагировать. Тем самым команда получает контроль карты и численное преимущество в сражениях за объекты.

I> **Пушинг миньонов** ([pushing](https://www.mobafire.com/league-of-legends/wiki/game-mechanics/pushing)) — это быстрое убийство вражеских миньонов на линии. Для этого обычно применяют атакующие умения чемпиона.

4. **Командное сражение** (team fight). Команда выбирает чемпионов, которые сильны в сражениях пять на пять. Умения таких чемпионов позволяют инициировать сражение (engage) или наносить урон по области (area-of-effect damage). Примеры: Malphite, Amumu, Rumble, Zyra, Brand. План заключается в ускорении игры. Команда навязывает частые сражения за объекты на карте. Подходящая комбинация чемпионов даёт в них преимущество.

5. **Осада** (siege). В команду входят чемпионы с большой дальностью умений или атаки. Примеры: Jayce, Ziggs, Caitlyn, Ezreal, Zoe. План состоит в том, чтобы наносить противнику урон с безопасного расстояния. Это истощает динамические ресурсы вражеской команды. Когда она уже не сможет действовать, надо навязывать сражение за объект на карте.

Чем больше чемпионов команды ориентированы на один план, тем лучше он работает. С другой стороны, противник может выбрать чемпионов так, чтобы полностью нейтрализовать этот план. Поэтому в соревновательных партиях и на высоком Эло игроки комбинируют несколько планов. Например, команда выбирает одного гиперкерри и нескольких чемпионов на раннюю агрессию. Таким образом их слабости компенсируются.

Общий план на игру может быть не только у команды, но и у отдельного игрока. Чаще всего на индивидуальный план полагаются в рейтинговых партиях на низком Elo. В них сложно коммуницировать с командой и договариваться. Некоторые планы строятся вокруг одного чемпиона (например, сплит-пуш или выход в лейтгейм). Именно их предпочитают опытные игроки. Так они меньше зависят от решений команды и могут достичь условия победы самостоятельно.

Вернёмся к нашему вопросу: как довести преимущество до победы? Для этого надо использовать преимущество так, чтобы реализовать общий план на игру. Например, в плане "ранняя агрессия" преимущество надо постепенно накапливать, пока оно не станет решающим. А в плане "командное сражение" преимущество надо реализовывать в контесте объектов. Поступая так, команда достигает своё условие победы.

{pagebreak}
