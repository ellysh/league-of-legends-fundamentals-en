## 2.2 Economy

C> *The general that hearkens to my counsel and acts upon it, will conquer: let such a one be retained in command! The general that hearkens not to my counsel nor acts upon it, will suffer defeat — let such a one be dismissed! While heading the profit of my counsel, avail yourself also of any helpful circumstances over and beyond the ordinary rules.*
C>
C> -- Sun Tzu "Art of War"

In this section, we will examine the economic aspect of League of Legends. It is much simpler than in a typical real-time strategy game. Despite this, the economy plays a crucial role and can often determine the outcome of a match.

A player must calculate the resources that each of his possible actions would provide. This allows him to distinguish between profitable and unprofitable actions. By doing so, the player can invest his time and resources more effectively. The team that converts time into resources better typically gains a significant advantage.

Let us look at how to calculate resources correctly when planning actions.

### 2.2.1 Gold and experience income

Resource calculations assist in decision-making. The more precise these calculations are, the more comprehensive the information available to a player. This information can lead to better decisions, although it does not ensure flawless gameplay.

Now, let us calculate the resources that champions receive during the laning phase.

#### 2.2.1.1 Income on lane

Let us first examine the champions who farm minions in each lane. The first wave of minions for every lane spawns near the Nexus at 1:05 game time. Subsequent waves then spawn every 30 seconds: at 1:35, 2:05, and so on.

When a champion last hits all enemy minions in a single wave, he receives the maximum possible gold. This gold amount increases as the game progresses.

Table 2-2 shows the average gold value of one minion wave based on game time.

{caption: "Table 2-2. Minion wave gold value", width: "70%"}
| Game time | Average gold per wave | Average gold per 1 cs |
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

According to the table, one minion wave costs an average of 150 gold. Waves spawn at the Nexus every 30 seconds. Therefore, a champion in a lane can farm two minion waves in one minute. Consequently, this results in an estimated income of around 300 gold per minute.

In addition to gold, killing a minion also rewards the champion with experience (EXP or XP). If the champion is within 1500 range when the minion dies, he receives experience. Getting this reward does not even require attacking the minion.

Table 2-3 shows the experience rewards for each minion type.

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

Each wave includes three warrior minions and three mage minions. The first siege minion appears in the fourth wave. From that point until the 15th minute, it appears in every third wave: 7, 10, 13, and so on. After the 15th minute and up to the 25th minute, siege minions appear in every second wave. After the 25th minute, each wave includes a siege minion.

Let us calculate the experience income per minute in a lane. In one wave, a champion receives `60 * 3 + 30 * 3 = 300` experience on average until the 15th minute. This means he receives 600 experience in two waves. Consequently, his income is 600 experience per minute. We could evaluate whether this is a big or a small number. To do this, let us refer to Table 2-4. It shows the amount of experience and the number of minion waves a champion needs to reach each level.

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

Shared minion waves mean that two champions are present in the same lane. In this case, killing each minion grants a total of 130% of the experience normally gained. This experience is divided evenly between the two champions, with each receiving 65%. As a result, they will generally be at a lower level compared to champions in solo lanes.

It is important to note that the 30th minion wave spawns at 16 minutes, which is approximately when the laning phase ends.

#### 2.2.1.2 Income in jungle

Now, let us discuss champions who farm jungle monsters. Each jungle camp provides 4 creep score, which translates to an average of 100 gold. A jungler can take about three camps per minute during the laning phase. Therefore, his income is approximately 300 gold per minute. This is roughly equivalent to the income of a champion farming in a lane.

In addition to gold, killing a monster also grants experience. On average, a jungler receives between 165 and 240 experience for each camp. This value increases as the game progresses. For three camps, a jungler gets an average of 600 experience. Consequently, his income is approximately 600 experience per minute. This is also roughly equal to what a champion in a solo lane earns.

Table 2-5 shows how many monster camps a jungler needs to clear in order to reach the first 7 levels.

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

For killing the first camp, the champion receives an additional 150 experience thanks to a jungle item. The item also provides an extra 80 experience for killing large monsters. Thus, the jungler always gains level 2 at 4 CS.

We examined the income of champions in the lane and jungle. We can draw the following conclusions from this:

1. The first four minion waves are extremely important. For the jungler, the first jungle clear is crucial. This is six monster camps in total.

2. Preventing a champion from earning income in the first minutes of the game gives an advantage of two or more levels later on.

3. When a champion is not farming his lane, he loses resources. For every minute the champion is absent, he misses out on approximately 300 gold and 600 experience.

4. Sharing minion waves between two champions is beneficial only in the early game. As the match progresses, this shared income becomes less advantageous. This increases the level gap with solo laners.

Experienced players pay close attention to the first two waves of minions in the lane. In the early game, each minion kill is crucial. It can determine who gains an early advantage. A skilled player can convert this advantage into the first kill and tower plates. Therefore, making the right decisions in the first minutes of the game can heavily influence the outcome of the laning phase.

### 2.2.2 Action planning

Beginner players often fail to see the connection between their actions and their long-term consequences. As a result, they underestimate the impact of their mistakes and miscalculations.

For example, when a jungler executes a poor gank, the enemy top laner may survive without taking any damage. The jungler may think there is nothing wrong with this play, and the resource equilibrium between the teams remains unchanged. In fact, this is not the case: the enemy team has actually gained an advantage. The reason is that the player wasted time that could have been spent farming monster camps, while the enemy jungler kept farming.

I> A **gank** is an ambush on an enemy champion in the lane. This is a common tactic used by junglers.

Let us examine several gameplay situations from an economic perspective. They will illustrate how resource calculations can predict the outcome of a given play.

#### 2.2.2.1 Gank

In the first example, the blue team's jungler is planning his next actions. He has just returned to base after the first jungle clear. For simplicity, let us assume he is considering only two options:

1. Continue farming his jungle.
2. Gank the enemy mid laner.

We have previously established that farming the jungle allows a champion to earn approximately 300 gold and 600 experience per minute. If the enemy jungler does the same, the resource equilibrium between the teams remains unchanged.

Now, let us calculate the potential outcome of ganking the mid laner. First, we need to estimate the time it will take. The champion will spend about 30 seconds reaching the mid lane and positioning themselves to attack. This time may vary based on mobility items and runes.

Here is the next step. After reaching the mid lane, the blue jungler needs to wait in ambush for the right moment to attack. For example, when the red mid laner moves far away from his tower. At this moment, the player attacks and pursues the target for a while. The blue jungler spends about 40 seconds making this play in total.

We found that the jungler spent about 40 seconds on the gank. If the player chooses to farm instead of ganking, he would take one monster camp for this time. It provides approximately 100 gold and 200 experience. This is the jungler's fee for participating in the gank.

Next, let us calculate what every team gets from this gank. There are three participants in this play: the red team's mid laner, the blue team's jungler, and the blue team's mid laner. Each player has three possible outcomes:

1. Killed
2. Survived with minimal health
3. Survived with medium or high health.

In **the first scenario**, the champion was killed by the enemy. He is then absent from the map for a certain period. This time is made up of two parts:

1. The resurrection time, which depends on the champion's level. During the laning phase, this is on average 20 seconds.

2. The time to reach the middle of his lane or a jungle camp. This time is around 30 seconds and depends on the champion's items and abilities.

In total, a killed champion is absent from his lane or jungle for almost one minute. During this time, he loses two minion waves or three jungle camps. Consequently, he loses 300 gold and 600 experience.

**The second scenario** is when the champion survives with minimal health. In this state, it is dangerous for him to remain in his lane or farm the jungle. The enemy jungler can easily finish him off.

The champion needs to return to base and recover. For doing that, he spends 8 seconds casting the **recall** spell. Afterward, he restores health and mana at the fountain for over 10 seconds. The champion then returns to the lane for about 30 seconds. In total, he is off the map for approximately 50 seconds. This means he will miss almost two minion waves. Consequently, he loses 300 gold and 600 experience. These calculations are valid for both the mid laner and jungler.

**Third case**: the champion survives with medium or high health. In this state, he can continue farming lane minions or jungle monsters. If he has enough gold, he can return to the base and buy an item. Recall will cost him about 40 seconds off the map. That is at least one missed wave, or approximately 150 gold and 300 experience.

Let us summarize the results for all three champions and estimate the team's income. For simplicity, we will focus only on three outcomes of a gank:

1. **Best case**. The red team's mid laner is killed, while the blue team's champions remain at full health.

2. **Mediocre case**. The red team's mid laner survives with minimum health, while the blue team's champions remain at full health.

3. **Worst case**. The red team's mid laner remains at full health, while both blue team champions are killed.

In the **best case**, the blue team's income would be as follows:

1. The blue jungler and mid laner receive gold and experience for the kill. The player who secured the kill receives 300 gold, while the player who assisted receives 150 gold. It totals 450 gold. They both share approximately 300 experience.

2. The blue mid laner can stay in lane and continue farming. Then he will earn 300 gold and 600 experience in one minute. His opponent will be absent from the lane for the entire time.

I> **Assist** is any action that helps in killing an enemy champion.

We can calculate the total advantage in favor of the blue team by combining the kill reward and the mid laner's farm. Then we need to subtract the jungler's fee for participating in the gank.

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

In a **mediocre gank case**, we calculate the blue team's income in the same way. However, we must exclude the bounty for killing the red team's mid laner from the formula.

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

The blue team got a decent result. But it is unlikely that this advantage decides the outcome of the laning phase.

In the **worst gank case**, the red team gets the advantage. It comes from the following:

1. The red mid laner receives the bounty for the double kill. That is 300 gold and 300 experience for each blue champion.

2. The red mid laner can stay in lane and farm. Then he will receive 300 gold and 600 experience. The blue mid laner would not receive these resources.

3. The blue team's losses would amount to twice 300 gold and 600 experience. This is the missed farm per one minute of the blue mid laner and jungler.

The red team's overall advantage will come from the mid laner's gain and both blue champions' losses. We must also factor in the jungler's fee for making the play.

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

These numbers show that a failed gank gives the enemy team a significant advantage. After such a play, it becomes nearly impossible for the blue mid laner to recover from this substantial gap.

Here is the summary for our calculations. The gank is beneficial for the blue jungler only if it leads to at least a mediocre result. To reduce the cost of participating in the gank, the blue jungler should come to the mid lane after clearing his camps. This approach will increase the potential income in case of success and slightly reduce losses if the gank fails.

Our example illustrates the consequences of a single serious mistake in League of Legends. Either a poor plan or poor execution can cause such a mistake. In other words, even a good plan does not guarantee an advantage if a player can not execute it well.

#### 2.2.2.2 Taking the dragon

In the second example, the blue team's jungler takes the [Infernal Drake](https://wiki.leagueoflegends.com/en-us/Infernal_Drake). First, he clears all his jungle camps for the second time. Then, he goes to the dragon pit. This way, the player uses his time as efficiently as possible.

Let us say Xin Zhao is the blue team's jungler. He is level 5 when he approaches the dragon pit. His **damage per second** (DPS) is around 100 **physical damage** (AD). At this point, the dragon has 5730 health. This means the jungler will take down the monster in about one minute.

For killing the dragon, the jungler will receive 125 gold and 150 experience. His jungler item will provide an extra 80 experience. Additionally, the team will receive a permanent buff for the rest of the game, granting 3% attack damage (AD) and ability power (AP). We can convert this buff into gold.

I> When a team takes an epic monster, the jungler should always finish it off. His item grants him an extra 80 experience, increasing the team's total reward for taking the monster.

[The following table](https://wiki.leagueoflegends.com/en-us/Gold_efficiency#Basic_reference_items) gives the cost of a champion's stats in gold. According to the table, we get the following values:

* 1 AD = 35 gold
* 1 AP = 20 gold

Since Xin Zhao has 100 AD, taking the dragon will give him an additional `100 * 0.03 = 3` AD. This increase is equal to `3 * 35 = 105` gold. We can take this number as the average value for all AD champions on the team.

At this point, an AP champion will have a maximum of two [Amplifying Tomes](https://wiki.leagueoflegends.com/en-us/Amplifying_Tome). Therefore, his total AP will be `20 + 20 = 40`. Taking the dragon will grant this AP champion `40 * 0.03 = 1.2` AP. This increase is equal to `1.2 * 20 = 24` gold.

Now, we can calculate the average gold gain for all AD and AP champions on the team:
{line-numbers: false, format: text}
```
5 * (105 + 24) / 2 = 322.5
```

This means that taking the red dragon will provide the entire team with approximately 300 gold at the beginning of the game. Consequently, when the jungler soloed the Infernal Drake, the team earned 425 gold and 230 experience. Part of this reward went to the jungler, and the rest went to his allies.

Let us compare the jungler's reward from taking the dragon with his typical monster farming per minute, which provides 300 gold and 600 experience. These numbers are bigger than the reward for the dragon. Consequently, the jungler personally paid `300 - 125 - 105 = 70` gold and `600 - 150 - 80 = 370` experience for taking the dragon. His team received a total of `320 - 70 = 250` gold.

We can conclude that the jungler lost approximately half a level by taking the dragon. The team's overall gain was modest. This means that taking the dragon is a long-term investment for both the jungler and his team. It does not provide any significant advantage immediately. However, the dragon's buff will give much more value in the late game when converted into gold.

Let us consider the worst-case scenario for taking the dragon. In this scenario, the blue mid laner and ADC help their jungler to take the object. Together, they take the dragon in about 20 seconds. Afterward, the mid laner and ADC will spend another 10 seconds returning to their lanes. Their total gold fee for participating in this team play is as follows:
{line-numbers: false, format: text}
```
150 + 150 + 150 = 450
```

The experience payment is:
{line-numbers: false, format: text}
```
300 + 300 + 300 = 900
```

At the early stages of the game, these values represent a significant investment. We calculated that the team earns 425 gold and 230 experience from taking the dragon. The reward almost compensates for the gold fee for participating in the play, but not the experience.

Now, imagine that the red jungler waits in ambush while the blue champions take the dragon. When the monster has low health, the red jungler finishes him off with Smite and escapes. In this case, the blue champions receive nothing for their participation fee in the play.

The red team gains a significant advantage from the dragon steal. It consists of the following:

1. The participation fee for team play from the blue champions.

2. The dragon reward: gold, experience and the buff.

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

This example shows that stealing a dragon grants the enemy team a significant advantage. It is challenging to compensate for this advantage in the early game.

We can draw several conclusions:

1. The more champions involved in a team play and the longer it lasts, the more expensive it is for the team.

2. Epic monsters should be taken down as quickly as possible. This minimizes the chance of enemy interference.

3. A failed team play gives the enemy a significant advantage. The higher the cost of participating in the play, the greater the consequences of a mistake.

#### 2.2.2.3 Destruction of the tower

In the third example, the team attacks an enemy tower. The tower gives only a gold reward, but no experience. First, let us examine how this reward counts.

Figure 2-1 shows the various tower types: T1, T2, T3, and T4. The tower type determines the reward for destroying it. Table 2-6 provides the specific numbers.

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

When a team destroys an enemy tower, it receives two rewards: global gold and local gold.

**Global gold** is distributed to all champions on the team, including those who are currently dead. **Local gold** is divided equally among champions who are within a 1200 radius of the destroyed tower. If a champion deals damage to the tower within 10 seconds before its destruction, he also receives the local gold, regardless of his distance from the tower.

The outer turrets have a plating mechanic [**turret plating**](https://wiki.leagueoflegends.com/en-us/Turret#General). This mechanic divides the tower's total health into five parts. Each part represents 1000 health, for a total of 5000 health. A champion earns 125 local gold for each plate he destroys. After losing each plate, the tower gains bonus armor and magic resistance for 20 seconds. At the 14th minute, the plates disappear, and players can no longer obtain rewards for them.

Considering tower and plate rewards is crucial when calculating resources. These are two significant sources of income that can provide a team with a substantial advantage.

Let us return to our third example, where players destroy the tower. The blue team takes Baron Nashor. The red team tries to prevent this, leading to a five-on-five teamfight. Three red champions and two blue champions are killed. The red team then retreats, allowing the blue team to finish off Baron Nashor.

The three surviving blue team players must decide on their next action before recalling. For simplicity, we assume that they have only two options:

1. Pursue the two surviving red champions.

2. Destroy the enemy T2 tower on the top lane.

Let us calculate the blue team's reward for pursuing. The reward for each red champion killed includes 300 gold plus an additional 150 gold for the assist. This gives a total of 450 gold. The experience reward for each champion killed is 300.

The maximum gold reward for both red champions would then be:
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

Now, let us calculate the blue team's reward for destroying the T2 top lane tower. Each blue champion will receive 25 global gold. Those champions who destroyed the tower will split 675 local gold. In total, this would give the entire team:
{line-numbers: false, format: text}
```
25 * 5 + 675 = 800
```

Which action is more beneficial for the blue team? If the pursuit results in two kills with assists, it will yield a greater reward. However, this play comes with a risk: both red champions might escape. Then three blue champions will waste their time and gain nothing. It is likely that one red champion would remain behind to delay the blue team's pursuit. In this case, the blue champions kill only him and receive 450 gold and 150 experience.

The reward for destroying the tower is more reliable. Two red champions with depleted resources would be unable to defend the tower. Thus, the blue team can confidently secure 800 gold by attacking the tower. This reward exceeds the likely outcome of the pursuit, which could result in only 450 gold and 150 experience. Therefore, the blue team should choose to attack the tower.

You might wonder why the blue team cannot pursue the enemy first and then destroy the tower. The issue is that pursuing would deplete the blue team’s tempo. The three red champions killed on the Baron will respawn. They will quickly return to the map because the enemy play happens near their base. Then the three blue champions with low resources will find themselves outnumbered in a teamfight. The red champions could surround them near their T2 tower and kill.

When a team has tempo, it needs to decide how to capitalize on it. This typically involves selecting one action from several options. Once the team executes their chosen play, the turn then passes to the enemy.

I> Experienced players recommend making only one team play at a time. Multiple parallel plays can spread the team's resources too thin, often resulting in failure.

### 2.2.3 Practice of resource calculation

We have examined three examples of resource calculation. It might seem that only the jungler needs this skill. He is typically the one who initiates team plays around objectives during the laning phase. Therefore, the jungler must calculate the potential consequences of these plays.

In fact, players in every role need the resource calculation skill. Here are some examples when it is required:

1. The top laner is planning to assist the jungler in taking a Herald. He should calculate how many resources he will pay for joining this play.

2. The mid laner is planning to gank the bottom lane. He should evaluate the team's potential resource gain from a successful gank against the losses from an unsuccessful one.

3. The ADC is planning to assist the jungler in taking a dragon. He should calculate how many resources he will pay for joining this play.

4. The support is planning to gank the mid lane. He should evaluate the team's potential resource gain from a successful gank against the losses from an unsuccessful one.

In each of these scenarios, performing a resource calculation will help determine the profitability of the planned action. If the risk is high and the reward is low, a player should refrain from participating in the team play.

To effectively learn how to calculate resources, the player needs to focus on numbers. However, his attention is in short supply during a game. Therefore, it is better to practice resource calculation by reviewing replays or watching streams.

Beginner players often lack the knowledge for effective self-coaching sessions. On the other hand, resource calculation serves as a universal method for assessing the quality of decisions. It is an excellent starting point for new players. Let us look at an example of how to apply it.

I> [**Outplayed**](https://www.overwolf.com/app/overwolf-outplayed) is one of the best apps for recording replays. It saves video files in MP4 format. You do not need the game client to open these files. This allows you to view replays while waiting for your next match.

Imagine you are watching your replay to conduct a self-coaching session. During the game, there are clear moments when you make decisions. These usually involve participating in an upcoming team play. For example, your jungler pings for help on a dragon. You need to pause the replay at that moment. Then, calculate the resources your team stands to gain from successfully taking the dragon. Subtract your participation fee for joining this play. Also, evaluate what your team would lose if the opponents contest and secure the dragon.

After completing the resource calculations, consider whether your participation in this team play is justified. Is the risk worth the potential reward? Continue watching the replay and check whether your calculations align with the actual results. If they do not, identify any mistakes in your reasoning. This will provide you with immediate feedback.

Becoming accustomed to calculating resources will improve your time management. To participate in any team play, players pay by losing resources. Therefore, the duration of the play determines the team's overall benefit. For instance, capturing a dragon in 30 seconds will give your team an advantage. But the same play done for one minute might benefit your opponents instead. Keep this in mind during your games.

While reviewing replays, note how much time you spend making decisions. This could be choosing an item in the shop or planning your next move on the map. Calculate how much time you spend standing still and thinking during the game. Then convert this time into lost resources. If it is a lot, you should focus on improving your decision-making skills.

You can enhance your decision-making speed by recognizing more patterns in typical game situations. Calculating resources will help you identify the right actions. This enables you to remember both the characteristics of specific situations and the appropriate responses. The next time you encounter a similar situation, you will be able to make the correct decision quickly.

If you want to remember patterns of specific situations more effectively, you need to document them. Text notes may not be the best option. For instance, you might write down in a text file: "Do not take the dragon when the team has no tempo." This is helpful advice in general, but it lacks specificity about a game situation.

Typical patterns in League of Legends are often visual. Therefore, the best way to document them is through visual formats. Take screenshots from replays that illustrate specific patterns. For example, it could be a mistake you want to avoid or good plays you or others make.

I> [Greenshot](https://getgreenshot.org/) is a convenient tool for saving screenshots. It has a built-in graphics editor for adding labels and text.

Give your screenshot files descriptive names, such as "do-not-take-dragon-without-tempo.png." Review your screenshots regularly to refresh your memory of familiar patterns. This way, you will gradually accumulate knowledge about the game. Over time, you will stop making the same mistakes, and your decision-making skills will improve.

Taking screenshots is also beneficial when watching guides, streams, competitions, and any coaching sessions. Save and review any significant patterns that you observe in this content.

I> Esports player Bwipo discusses the economic aspects of League of Legends in more detail in the [following video](https://www.youtube.com/watch?v=fJ-C4PEk-9Y).

{pagebreak}
