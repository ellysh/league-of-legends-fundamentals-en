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

>>>R1

In the second example, the blue team's jungler takes the [Infernal Drake](https://wiki.leagueoflegends.com/en-us/Infernal_Drake). First, he clears all his jungle camps for the second time. Then, he goes to the dragon pit. This way, the player uses his time as efficiently as possible.

Let us say Xin Zhao is the blue team's jungler. He is level 5 when he approaches the dragon pit. His damage per second (DPS) is around 100 physical damage (AD). At this point, the dragon has 5730 health. This means the jungler will take the monster solo in about one minute.

For killing the dragon, the jungler will receive 125 gold and 150 experience. The jungler item will provide an additional 80 experience. The team will receive a permanent buff for the rest of the game: 3% attack damage (AD) and ability power (AP). We can convert this buff into gold.

When a team takes an epic monster, the jungler should always finish it off. The jungler's item will grant him an additional 80 experience, increasing the team's total reward for the monster.

[The following table](https://wiki.leagueoflegends.com/en-us/Gold_efficiency#Basic_reference_items) gives the cost of a champion's stats in gold. According to the table, we get the following values:

* 1 AD = 35 gold
* 1 AP = 20 gold

Xin Zhao has 100 AD so that the dragon buff will give him `100 * 0.03 = 3` AD. This increase is equal to `3 * 35 = 105` gold. We can take this number as the average AD value for all champions on the team.

At this point, an AP champion will have a maximum of two [Amplifying Tomes](https://wiki.leagueoflegends.com/en-us/Amplifying_Tome). Therefore, his total AP will be `20 + 20 = 40`. Taking the dragon will give the AP champion `40 * 0.03 = 1.2` AP. This equals `1.2 * 20 = 24` gold.

Let us calculate the average gain in gold for all AP and AD champions on the team:
{line-numbers: false, format: text}
```
5 * (105 + 24) / 2 = 322.5
```

This means that taking the red dragon will give the entire team approximately 300 gold at the beginning of the game. Therefore, when the jungler soloed the infernal dragon, the team earned 425 gold and 230 experience. Part of this reward went to the jungler, and the rest went to his allies. 

Let us compare the jungler's reward with his typical monster farming per minute: 300 gold and 600 experience. These numbers are bigger. Thus, the jungler personally paid `300 - 125 - 105 = 70` gold and `600 - 150 - 80 = 370` experience for taking the dragon. His team received a total of 240 gold.

We can conclude that the jungler lost approximately half a level for taking the dragon. The team's overall gain was modest. This suggests that taking the dragon is a long-term investment for the jungler and his team. It does not provide immediate benefits. However, the dragon's buff will become a significant advantage in the late game when converted into gold.

Let us consider the worst-case scenario for taking the dragon. In this case, the blue mid laner and ADC help their jungler to take the object. They take the dragon in about 20 seconds. Then, the mid laner and ADC will spend another 10 seconds returning to their lanes. Their total gold payment for participating in the team action will be:
{line-numbers: false, format: text}
```
150 + 150 + 150 = 450
```

The experience payment will be:
{line-numbers: false, format: text}
```
300 + 300 + 300 = 900
```

At the early stages of the game, this is a significant investment. We calculated that the team will receive 425 gold and 230 experience for the dragon. This means the reward will compensate for the gold, but not the experience.

Now, let us say the red jungler waits in ambush while the blue champions take the dragon. When the monster has low health, the red jungler finishes him off with the smite spell and survives. In this case, the blue champions receive nothing for their participation fee in the team action.

The red team gets a significant advantage. It consists of the following:

1. The blue champions' team action participation fee.

2. The dragon reward: gold plus the buff.

Here is the gold advantage for the red team:
{line-numbers: false, format: text}
```
450 + 425 = 875
```

Here is the experience advantage for the red team:
{line-numbers: false, format: text}
```
900 + 230 = 1130
```

This means that stealing a dragon gives the enemy team a significant advantage. It is challenging to compensate for this advantage at the beginning of the game.

Our example leads to several conclusions:

1. The more champions involved in a team action and the longer it lasts, the more expensive it is for the team.

2. Taking epic monsters should be done as quickly as possible. This reduces the chance of the enemy team interfering.

3. A failed team action gives the enemy a significant advantage. The higher the cost of participating in the play, the higher the cost of a mistake.

#### 2.2.2.3 Destruction of the tower

>>>R1

The team destroys an enemy tower in the third example. The tower gives only a gold reward, not experience. First, let us look at how this reward works.

Figure 2-1 shows the different tower types: T1, T2, T3, and T4. The tower type determines the reward for destroying it. Table 2-6 provides the specific numbers.

{caption: "Table 2-6. Tower rewards", width: "100%"}
| Tower designation | Tower name | Global gold | Local gold |
|  | | | |
| :---: | --- | :---: | --- |
|  | | | |
| T1 | Outer turret | 50 | 250 |
|  | | | |
| T2 | Inner turret | 25 | • 425 on mid lane |
|  | | | • 675 on top and bot lanes |
|  | | | |
| T3 | Inhibitor turret | 25 | 375 |
|  | | | |
| T4 | Nexus turret | 50 | 0 |

Destroying a tower rewards a team with two types of gold: global and local gold. **Global gold** is awarded to all champions, including those currently killed. **Local gold** is split equally among champions within a 1200 radius of the destroyed tower. If a champion deals damage to the tower within 10 seconds before its destruction, he also receives local gold. In this case, the reward does not depend on the distance to the tower.

The outer turrets have a plating mechanic [**turret plating**](https://wiki.leagueoflegends.com/en-us/Turret#General). It works like this. The tower's total health is divided into five parts. Each part represents 1000 health, for a total of 5000 health. The champion receives 125 local gold for each plate destroyed. After this, the tower gains bonus armor and magic resistance for 20 seconds. At 14 minutes, the plates disappear, and players can no longer obtain the reward for them.

Tower and plate rewards should be taken into account when calculating resources. They are an important source of income and can give a team a significant advantage.

Let us return to our example. The blue team takes Baron Nashor. The red team tries to prevent this. This leads to a five-on-five teamfight. Three red champions and two blue champions are killed. The red team then retreats, and the blue team finishes off Baron Nashor.

The three surviving blue team players choose an action before recalling. For simplicity, we assume that they have only two options:

1. Pursue the two surviving red champions.

2. Destroy the enemy T2 tower on the top lane.

Let us calculate the blue team's reward for pursuing. For each red champion killed, players will receive 300 gold plus 150 gold for the assist. This gives a total of 450 gold. The experience reward is 300.

The maximum gold reward for two champions will be as follows:
{line-numbers: false, format: text}
```
450 + 450 = 900
```

The gold reward without assists reduces to the following:
{line-numbers: false, format: text}
```
300 + 300 = 600
```

The experience reward does not depend on assists and will be as follows:
{line-numbers: false, format: text}
```
300 + 300 = 600
```

Now, let us calculate the blue team's reward for destroying the T2 top lane tower. Each blue champion will receive 25 global gold. Those who destroyed the tower will split 675 local gold. In total, this will give the entire team:
{line-numbers: false, format: text}
```
25 * 5 + 675 = 800
```

Which of the two options is more beneficial for the blue team? If the pursuit ends with two kills and assists, it will yield more. However, this comes with a risk: both red champions might escape. Then the blue team will lose time and gain nothing. Most likely, the pursuit will end with only one kill. One red champion will stay behind to buy time for their ally to escape. In this case, the blue team will only receive 450 gold and 150 experience.

The reward for destroying the tower is more reliable. Two red champions with depleted resources will be unable to defend it. Therefore, the blue team is guaranteed to receive 800 gold for the tower. This reward is higher than the likely outcome of pursuing enemies for 450 gold and 150 experience. Therefore, the blue team should choose to attack the tower.

One might wonder: why can not the blue team first pursue the enemy and then destroy the tower? The problem is that pursuing causes the blue team to lose tempo. The three red champions killed on the Baron will respawn. They will quickly return to the map because the enemy is near their base. Then the three blue champions will find themselves outnumbered and depleted of resources. They could become surrounded near the red T2 tower and die.

When a team has tempo, it must decide how to capitalize on it. Typically, this involves choosing one action from several options. Once the team does the chosen play, the turn passes to the enemy.

I> Experienced players recommend making only one team play at a time. Multiple parallel plays spread the team's resources and often fail as a result.

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
