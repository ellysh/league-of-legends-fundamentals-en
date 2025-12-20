## 2.1 Basic concepts

In this section, we will review the fundamental concepts of the game. It would be beneficial to organize them systematically. For this purpose, the following list of questions will assist us:

1. What is the initial state of the objects on the map?

2. What disrupts the equilibrium of the objects?

3. What actions are advantageous?

4. How to identify an advantage?

5. How to acquire an advantage?

6. How to use an advantage to achieve victory?

Each of these questions relates to a specific game concept.

The order of the questions is important: each one logically follows from the previous one. Similarly, the game concepts are interconnected: more complex ideas build on simpler ones.

The basics may seem trivial, but many new players struggle to understand them. This lack of understanding can prevent them from mastering essential techniques, such as wave management. Until a player grasps the general patterns of League of Legends mechanics, information from guides may appear disjointed and chaotic to him. Absorbing information in this fragmented manner is nearly impossible.

We will examine each concept in detail to eliminate any misunderstandings.

### 2.1.1 Equilibrium

The first question on our list is as follows:

> What is the initial state of the objects on the map?

Initially, all objects on the map are in equilibrium. **Equilibrium** refers to a balanced and stable state of the game's elements. All subsequent concepts are based on this idea.

You can easily determine the equilibrium of game objects by examining the Summoner's Rift map. Figure 2-1 demonstrates it.

I> Please note that the general structure of the map has remained unchanged between Seasons 14 and 15. Some diagrams in this book depict the Season 13 map, but all of them still apply to the newer versions.

{caption: "Figure 2-1. Summoner's Rift map for Season 13", height: "50%"}
![Summoner's Rift ma](images/Theory/map-season-13-no-champions.png)

Letters and geometric shapes indicate interactive objects on the map. Note that player champions are excluded for simplicity.

The symbols used on the map are as follows:

* T1, T2, T3, T4 — [**towers**](https://wiki.leagueoflegends.com/en-us/Turret) of each team.

* I — [**inhibitors**](https://wiki.leagueoflegends.com/en-us/Inhibitor) of each team.

* N — [**Nexus**](https://wiki.leagueoflegends.com/en-us/Nexus) of each team.

* Green circle — the neutral [**monster**](https://wiki.leagueoflegends.com/en-us/Monster) camp.

* Blue rectangle — the [**minion**](https://wiki.leagueoflegends.com/en-us/Minion) (creep) wave of the blue team.

* Red rectangle the minion wave of the red team.

You can identify three forms of equilibrium on the map:

1. Landscape equilibrium.

2. Resource equilibrium.

3. Teams' power equilibrium.

**Landscape equilibrium** refers to the geometry of the map and all static objects on it: walls, bushes, buildings, and roads (lanes). As shown in Figure 2-1, these objects are symmetrical about the map's center.

Here are some examples of landscape equilibrium:

* The blue team's base is located in the lower-left corner. The red team's base is symmetric about the map's center and is in the upper-right corner.

* The blue team's jungle with [Red Brambleback](https://wiki.leagueoflegends.com/en-us/Red_Brambleback) (red buff) is at the bottom. The red team's jungle, containing the same camps, is at the top, symmetrically aligned with the map center. The same is true for both jungles with [Blue Sentinel](https://wiki.leagueoflegends.com/en-us/Blue_Sentinel) (blue buff).

* The [baron pit](https://wiki.leagueoflegends.com/en-us/Baron_pit) is located in the upper river. The [dragon pit](https://wiki.leagueoflegends.com/en-us/Dragon_pit) is in the lower river, symmetrical to the map center.

* Each structure belonging to the blue team has a corresponding structure for the red team that is symmetrical around the center.

**Resource equilibrium** refers to the availability of resources for both teams, encompassing both what they currently possess and what they can potentially acquire on the map.

Several objects on the map provide rewards when destroyed. One example is neutral monsters, which are indicated by green circles in Figure 2-1. Each green circle has a symmetrical counterpart relative to the center of the map, meaning that both teams can earn equal amounts of resources from the jungle.

Enemy minions also serve as a source of income. Every 30 seconds, each Nexus spawns the same number of minions, allowing both teams to kill an equal number of them.

Additionally, we can consider all buildings as resources. Destroying an enemy building rewards the attacking team. Due to the landscape's equilibrium, these resources are also balanced for both teams.

**Teams' Power Equilibrium** refers to all their units: towers, inhibitors, the Nexus, minions, and champions. Towers, inhibitors, and the Nexus are immobile structures. They are subjects of the landscape equilibrium and are symmetrical about the map's center. This means teams have an equal number of each type of structure.

Minions are mobile units that represent both team power and enemy resources. They move in groups called **waves**. Waves spawn near the Nexuses at regular intervals — the first wave spawns at 1:05 game time, and then every 30 seconds thereafter.

Three waves of minions spawn simultaneously on each side and move along three lanes: top, middle, and bottom. These lanes connect the bases of both teams. In each lane, the blue and red waves of minions meet exactly in the middle and engage in combat.

Minion waves maintain equilibrium. If the clash front remains in the middle of the lane, it will not move. Its position will remain constant, as shown in Figure 2-1. This stability occurs because each successive wave arrives just as the last minions from the previous wave die.

Champions are the primary mobile units of each team. If a champion becomes significantly weaker compared to opponents, he can no longer effectively contribute to the game. In such cases, the champion becomes a resource for the enemy team, like a minion.

We have considered three forms of equilibrium for game objects. Each of these forms is dynamic. This means that if something disturbs the equilibrium of an object, it returns to its original state over time. Let us explore some examples.

Abilities of certain champions can disrupt the **landscape equilibrium**. They create new walls (Anivia W) or passages (Bard E). These actions disturb the balance of static objects. However, the effects of such abilities are temporary. The landscape will revert to its original state after a few seconds.

When a player destroys an object, it disrupts the **resource equilibrium**. First, the player receives a reward that the enemy can no longer obtain. Second, the destroyed object disappears from the map. For example, killing a jungle monster leaves its camp empty. Nevertheless, the monster will respawn at its camp after a specific period. The respawn time varies by monster type and ranges from 2 to 6 minutes.

The dynamic **equilibrium of power** between teams is more intricate. First, only some structures can recover after being destroyed, while others cannot. Second, the minion clash front can shift along its lane. If it strays from the center of the lane, it will gradually return to the center. We will discuss this mechanics in more detail in section "4.1 Minion wave management."

### 2.1.2 Action

Here is the second question on our list:

> What disrupts the equilibrium of the objects?

Player champions are the only entities capable of disrupting the equilibrium of game objects. Even their mere presence on the map alters the balance of the teams. This happens because cannot select the same champion.

When a champion takes action, it affects a game object and changes its state. This disrupts one of the three forms of equilibrium.

We can categorize all possible actions by champions into two types: micro and macro. The most basic actions fall under the **micro-level** and aim for short-term goals. Here are a few examples:

* Moving a few steps back to avoid an incoming projectile.

* Using a crowd control (CC) ability on an enemy to stop him.

A sequence of micro-level actions combines to form a single **macro-level** action. It is aimed at achieving a long-term goal. For example, a champion uses auto-attacks and abilities to kill enemy minions quickly. This is considered one macro action, commonly known as pushing a lane.

Here is a list of basic macro-level actions that can disrupt the balance of game objects:

1. Attacking enemy minions.
2. Attacking an enemy champion.
3. Attacking an enemy tower.
4. Attacking an enemy inhibitor, if possible.
5. Attacking the enemy Nexus, if possible.
6. Attacking jungle monsters.

A series of basic macro actions can combine to form a complex macro action. It is aimed at executing a plan consisting of several steps. Here are examples of complex macro actions:

* Split pushing to create a threat on a side lane and gain map control.

* Sieging the enemy base from two directions to destroy one of the inhibitors.

Each player must choose and execute the most advantageous macro action at any given moment. This action should disrupt any type of equilibrium in favor of the player's team. This way, he increases his team's chances of winning.

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

The **mid game** phase typically begins at the 14th minute and lasts until the 25th minute. It ends around the time when players collect their third item. Teams' goals during this phase are following:

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

>>>R1

Now we reach the third question in our list:

> What actions are beneficial?

Let us look at an example to answer this question. There is beginning of the laning phase. Both mid laners come to their lane. The players should choose and execute some action every second. We could limit the list of possible actions by the mid lane scope only. Then we get the following list:

1. Attack the enemy champion
2. Attack the enemy tower
3. Farm enemy minions
4. Retreat to a safe area under ally tower.

There is the equilibrium of power on the mid lane. This means that the minions clash front is in the middle of lane. There are equal numbers of minions on each side. Also, the health, mana, levels, and items of both champions are equal.

What options does the blue team's mid laner have?  **First**, attacking the enemy champion is risky because of the equilibrium of power. The player could kill the opponent and gain a reward with a 50% probability. In the other 50% of cases, the player will die. This way his opponent will gain a reward. Therefore, attacking the enemy champion is disadvantageous action. It does not increase the team's chances of winning.

**Second**, the player cannot attack the enemy tower without support of ally minions. They should absorb the tower's shots while the champion is attacking the structure. Otherwise, the tower kills the champion quickly. Therefore, attacking the enemy tower in the current situation is unfavorable.

**Third**, farming enemy minions is a standard action during the laning phase. It maintains resource equilibrium between the mid laners. If the blue team's player is better at last-hitting minions, he will gain an advantage with minimal risk. It is the best scenario in the current situation.

**Fourth**, retreating to the safe zone means giving up farming. This decision gives the enemy mid laner a resource advantage. Therefore, this is disadvantageous action that increases the enemy team's chances of winning.

Now let us assume that the situation changes. The blue team's jungler comes to mid lane. This increases chances to kill red team's mid laner. Therefore, attacking him becomes a profitable action.

What happened in our example when the jungler appeared? The blue team gained a numerical advantage in the mid lane. Advantage is the second fundamental concept. It follows from the concept of equilibrium.

A team gains an **advantage** when any form of equilibrium shifts in its favor. An advantage can be gained not only by a team, but also by an individual player. When the equilibrium on the lane shifts in his favor, the player gains an advantage.

Advantage comes in different types. It depends on which form of equilibrium has been disrupted. Experienced players distinguish the following types of advantage:

1. **By quantity** — one team has more champions participating in the teamfight than the other.

2. **By items** — one or more champions on the team have more items or they are more expensive than their opponents.

3. **By level** — one or more champions on the team have a higher level than their opponents.

4. **By resources** — one or more champions on the team have one of the following while their opponents do not:

   * health

   * mana

   * ready-to-use [**summoner spells**](https://wiki.leagueoflegends.com/en-us/Summoner_spell)

   * ready-to-use [**abilities**](https://wiki.leagueoflegends.com/en-us/Champion_ability), especially ultimate

   * individual or team [**buffs**](https://wiki.leagueoflegends.com/en-us/Buff) received for killing a neutral monsters.

5. **Map control** means a team has vision and influence over key areas of the map. Vision is granted by special items called [**wards**](https://wiki.leagueoflegends.com/en-us/Ward). Influence is gained when champions are within range of key points on the map. We will cover this concept in section "4.2 Map Control."

6. **Positional advantage** has two meanings. First, a champion has advantageous position in a lane than his opponent. Second, a team has advantageous position before the teamfight. Here are examples: flanking, controlling narrow passages or zoning out the enemy team.

7. **By team composition** — champions on the team interact and strengthen each other better than champions on enemy team .

8. **By tempo**. We will consider the concept of tempo further.

Please note that a team can have multiple types of advantages at once. Opponents can also have advantages, but of a different type.

Let us look at the example. The blue team has a stronger champion composition and better map control. The red team has the [**Elder Dragon**](https://wiki.leagueoflegends.com/en-us/Dragon_Slayer#Aspect_of_the_Dragon) buff. The dragon buff is the decisive advantage in this case. **Decisive advantage** is one that disrupts the equilibrium of power between teams or champions in a lane more than other types of advantage.

Please note that the importance of each type of advantage depends on the current state of the game. For example, a level advantage is more important than an item advantage during the laning phase. This rule applies until champions reach level 6. Therefore, a level advantage is decisive on first minutes. Items provide more power after level 6 and become the decisive advantage.

Let us return to the question we asked at the beginning of this section. Here are beneficial actions in the descending order:

1. Use the existing advantage.

2. Take action that gives some type of advantage.

3. A standard action in the current conditions.

**Using an advantage** is the most beneficial action in general. A team or a single champion is already stronger than the enemy. Players must somehow capitalize on this and gain something in return. For example, contest some object when the team has a numerical advantage.

**Take action that gives some type of advantage**. It is the second most beneficial choice. If you manage to tip some form of equilibrium in your favor, you can take advantage of it. For example, attack a dragon to gain its buff.

The **standard action** is the most disadvantageous choice on our list. It is usually aimed at maintaining the current equilibrium of teams power. A player will only benefit from this action if he executes it significantly better than his opponent. For example, farm minions on lane.

### 2.1.5 Macro cycle

>>>R1

Here is the fourth question on our list:

> How do you discover an advantage?

A player needs two things fo doing this:

1. Learn templates for recognizing typical game situations.

2. Effectively manage his attention during the game.

We will explore templates for various gameplay aspects and proper actions further in this book. Now, let us talk about attention management.

There is the concept of a macro cycle in **real-time strategy** (RTS) games. A **macro cycle** is an approach to effectively managing a game's economy. The idea is to create a list of tasks and execute them sequentially.

Here is an example macro cycle for a typical strategy game:

1. Produce workers.
2. Deploy workers to mine resources.
3. Produce military units.
4. Construct new buildings.
5. Perform technical upgrades.

When a player follows a macro cycle, he performs the actions in the list in order. Upon reaching the last action, the player starts the list over again.

The advantage of a macro cycle is that the player would not forget anything important. The macro cycle forms a strong habit after repeated use.  If an action is listed, the player will definitely perform it. He does not have to waste unnecessary cognitive resources on memorization. The macro cycle allows for equal attention distribution across all aspects of the game.

Random events occur in any strategy game. Some of these events require the player's full attention. After resolving the problem, the player must restart the macro cycle. This is his default mode.

League of Legends does not have an economy like a typical strategy game. Players do not build a base or produce new units. However, the idea of ​​a macro cycle remains relevant. Because the game has many aspects, players need to balance their attention between them.

A common mistake among new players is focusing on only one aspect of the game. For example, a novice top laner might focus exclusively on the enemy minion wave, trying not to miss an opportunity to last-hit them. This prevents the player from seeing the health, mana, or level of his champion. He does not notice when he gains an advantage in health, mana, or level. Therefore, the player fails to capitalize on this advantage. A macro cycle helps to avoid such mistakes.

The macro cycle for each of the five team roles will be different. For example, we will look at possible macro cycles for a mid laner and a jungler.

Figure 2-2 shows the objects on the map that the mid laner must switch his attention between.

{caption: "Figure 2-2. Macro cycle for mid laner", height: "50%"}
![Mid laner macro cycle](images/Theory/map-season-13-midlaner-macrocycle.png)

This is an expanded version of Figure 2-1. It has the blue and red circles that mark the champions of each team.

Let us have a look on Figure 2-2. The pink circle with number 1 marks the the blue team's mid laner. The pink text marks the objects that the player should check during his macro cycle. Here are these objects:

1. State of his own champion:

   * health
   * mana
   * level
   * ready abilities
   * items and their effects' readiness.

2. State of the enemy champion on the lane:

   * health
   * mana
   * level
   * ready abilities (remember cooldowns)
   * items.

3. Enemy minions wave:

   * is there a minion for the last hit?
   * total number of minions in the wave
   * location of the next wave (symmetrical to the next allied wave).

4. Allied minion wave:

   * is there a minion for the last hit?
   * total number of minions in the wave
   * location of the next wave.

5. Allied or enemy tower, if it is nearby:

   * health and plate count
   * its attack range.

6. Minimap:

   * Allied jungler location
   * Enemy jungler location (requires tracking skill)
   * State of adjacent lanes (minion wave positions, presence of champions in lanes)
   * State of nearby jungle monster camps (especially epic ones: Herald, Baron, Dragon).

7. Game stats by the Tab key:

   * levels of all champions
   * items of all champions.

I> [**Cooldown**](https://wiki.leagueoflegends.com/en-us/Cooldown) (CD) occurs immediately after using an ability. It is the time during which the ability is unavailable. Cooldowns apply not only to champion abilities, but also to runes, summoner spells, and item effects.

The list shows objects and game aspects that a player should regularly pay attention to. A typical pattern may emerge in one of them. This pattern could indicate a temporary advantage and an opportunity to capitalize on it. It is impossible to notice the pattern without focusing on the corresponding game object.

> To find a pattern in something, you have to look at it.

Let us look at the blue team's jungler macro cycle. This role is unique because the player spends almost the entire laning phase in the jungle. Therefore, his macro cycle is significantly different from the others.

Figure 2-3 shows the objects on the map that are part of the jungler's macro cycle.

{caption: "Figure 2-3. Macro cycle for jungler", height: "50%"}
![Jungler macro cycle](images/Theory/map-season-13-jungler-macrocycle.png)

The blue team's jungler is marked with a pink circle with the number 1. Here are the objects in his macro cycle:

1. State of his own champion:

   * health
   * mana
   * level
   * ready abilities
   * items and their effects' readiness.

2. Location and state of the enemy jungler (requires tracking skill):

   * minimap
   * game stats window.

3. Nearest jungle monster camps:

   * current farming target
   * next farming target.

4. Lane state, starting with the closest:

   * minion wave position
   * presence of champions in the lane
   * champions state (health, mana, level, items).

5. Next epic monster to contest:

   * its respawn timer
   * allied champions in range
   * enemy champions in range.

6. Game stats by the Tab key:

   * levels of all champions
   * items of all champions.

Please note that a jungler cannot read all information from minimap. He should switch the camera to each lane and check what is happening there. The best way for doing it is using hotkeys F1, F2, F3, and F4. The [following video](https://www.youtube.com/watch?v=pizMcCWv8y8) explains how to configure them.

You could try to introduce macro cycle into your games step by step:

1. Make a list of the minimum required actions to repeat. A good starting point could be the following:

   * check game objects on the main screen
   * check the minimap
   * check game stats by pressing the Tab key.

2. Install and set the [metronome app](https://play.google.com/store/apps/details?id=com.andymstone.metronome&hl=en) to 15 seconds. It gives your a regular sound signal.

3. When the signal happens, perform the macro cycle. Consistently switch your attention between the items on the list.

4. If some game event distracts you, you should process it first. Then return to the macro cycle and start it from the beginning.

You could start practicing the macro cycle in "Co-op vs. AI" mode. It will be easier to control your attention there. The minimal macro cycle will become a habit soon. Add new actions to the list that you consider as important. Gradually reduce the delay between sound signals.

Distributing your attention between important aspects of the game is essential for each role. This is especially true for the jungler. If jungler is your primary role, you need to learn a minimal macro cycle before your next ranked game.

### 2.1.6 Tempo

>>>R1

Here is the fifth question on our list:

> How do you gain an advantage?

Experienced players accumulate advantages **from small to large**. This is the most reliable way to win against an equally strong opponent.

The player starts to accumulate an advantage when one of the equilibrium forms shifts in his favor. He should notice this shift and take advantage of the opportunity. It means that the player should act according to some plan in which each step provides a small benefit. Gradually, this plan leads to a major advantage.

Tempo is the starting point from which experienced players begin to accumulate an advantage. Let us explore what this term means.

There is the concept of a turn in turn-based strategy (TBS) games. A **turn** is a specific moment in time when a player is allowed to act. Turns follow one after another sequentially. Each player acts on his turn.

League of Legends is a real-time game. Its mechanics allow players to act continuously. The only exception is death. In this case, the player must wait for a respawn timer. However, the game does have a concept of a turn which is called a play.

I> A **play** is a single action by a team or player that pursues a specific goal. For example, taking an epic monster or destroying an enemy tower.

A team and each of its champions can only operate effectively under certain conditions. Two things determine these conditions: the available resources and the players' positions on the map. If resources are available and the positions are favorable, a play can be made. Otherwise, the team or champion cannot act.

The conditions under which a team or champion can operate effectively are called [**tempo**](https://wiki.leagueoflegends.com/en-us/Snowball#Qualities). Coach Kairos explains this concept in detail in [the this video](https://www.youtube.com/watch?v=vHVeltI0IkE). He gives the following **tempo formula** for a specific champion:
{line-numbers: false, format: text}
```
tempo = champion power / distance to object
```

**The first part of the formula** is champion power. It is made up of a champion's resources. We can divide them into two types:

1. Static
2. Dynamic.

**Static resources** are things that a champion has already acquired and can no longer lose. Examples: level, items, gold, and permanent stacks of certain abilities.

**Dynamic resources** are things that a champion can spend or lose. Examples: health and mana, temporary buffs, readiness of abilities, summoner spells, and item effects.

We have talked about the equilibrium of game objects. One of its forms is resource equilibrium, which is restored over time. Dynamic resources restore over time. It is obvious. For example, each champion passively replenishes health and mana, even without returning to the fountain. Their abilities and item effects also recharge after a cooldown.

It is less obvious that the equilibrium of static resources is also restored over time. Here is an example. The blue team's mid laner is the first player who has reached level 18 and get all items. This is a significant advantage and he could carry his team to victory. However, if the game drags on, the red team returns to the game. After some time, its champions will reach level 18 and get all items. Therefore, the blue mid laner, who led in static resources, will lose his advantage over time. Then, the balance of power between the teams will be restored along with the equilibrium of static resources.

Coach Kairos suggests considering only a portion of a champion's static and dynamic resources for simplicity. Table 2-1 shows them.

{caption: "Table 2-1. Champion resources for tempo calculation", width: "100%"}
| Designation | Description | Scale |
|  | | |
| --- | --- | --- |
|  | | |
| resources | Health and mana | from 1 to 3, where 2 is half |
|  | | |
| stats | Base champion stats per level | from 1 to 5, where 3 is equality of levels |
|  | | |
| items | Items and their stats | from 1 to 5, where 3 is the equality of items |
|  | | |
| cooldowns | Readiness of abilities, summoner spells, and item effects | from 1 to 5, where 3 means that some CDs are ready |

Here is the formula to calculate champion power:
{line-numbers: false, format: text}
```
champion power = resources * (stats + items + cooldowns)
```

Note that resources are the multiplier. It means that health and mana are the determining factors. A champion has no tempo at low health, regardless of his other stats.

**The second part of the tempo calculation formula** is the distance to the object. An object can be anything besides an epic monster or enemy structure. In the context of tempo, it can also be a lane for gank, a teamfight, a jungle camp, or even a minion wave.

Note that tempo is calculated for a given map object. For example, suppose a champion is on the bottom lane. His tempo on a dragon will be high, but his tempo on baron will be low.

The distance to an object is measured in seconds to reach it. For example, if a player is at base but has a teleport spell ready, his distance to the object is small.

Coach Kairos suggests a scale from 1 to 10 that allows to estimate the distance:

* 1 — the champion is already at the objective.
* 5 — the champion is halfway to the objective.
* 10 — the champion is at the base or dead.

Let us calculate tempo for a specific example. There is a blue jungler Viego. We want to know his tempo on the dragon. For simplicity, we will only consider the junglers of both teams and ignore other champions.

Viego has full health and mana. Therefore, his resources equal 3. He has level 8, and the red jungler has level 6. It mans that Viego's stats equal 5. He bought his first item, and the enemy jungler does not have it. Then Viego's items equal 4. All of Viego's abilities and spells are ready. Therefore, the champion's cooldowns equal 5. Viego enters the lower river from his jungle. Then his distance to the object equals 2.

Here is the tempo on the dragon calculation for Viego:
{line-numbers: false, format: text}
```
tempo = 3 * (5 + 4 + 5) / 2 = 21
```

This is a very high value. Let us compare it to the tempo of the red jungler Ekko, who is in top jungle now. His distance to the object is 7. His resources are the following:

* Full health and mana: resources = 3.

* Sixth level when the enemy has eighth:
stats = 1.

* No first item when the enemy has it: items = 2.

* All abilities and spells ready: cooldowns = 5.

Here is the tempo on the dragon calculation for Ekko:
{line-numbers: false, format: text}
```
tempo = 3 * (1 + 2 + 5) / 7 = 3.4
```

This is a very low value. It means Ekko can not contest the dragon.

Coach Kairos' formula shows how a player can increase his tempo. He needs to get one of the following things:

1. Resource advantage (health, mana).

2. Champion level advantage.

3. Item advantage.

4. Cooldown advantage for abilities, spells, and item effects.

5. Being close to the object.

This list also works in reverse. If the opponent has any of these things, he gains tempo. Consequently, the player loses tempo.

Coach Kairos suggests to calculate a team's tempo as the sum of its players' tempos. The formula looks like this:
{line-numbers: false, format: text}
```
team tempo = top tempo + jungle tempo + mid tempo + adc tempo + support tempo
```

If you apply this formula to both teams, you can determine one that has tempo at the specific object at the moment. The team with tempo is more likely to win the fight and get the object.

A player can easily gain a small tempo advantage if he comes to a closer position to the object. However, a tempo advantage is dynamic. It creates a window of opportunity when a team or player can exploit the advantage. If this opportunity is missed, the tempo advantage will be useless.

### 2.1.7 Victory condition

>>>R1

Here is the last question on our list:

> How to turn an advantage into a victory?

We already know that there are different types of advantage. The advantage within a given type can also vary in quantity. Let us compare the gold gap between teams with 1000 and 14000 gold for example. In the second case, every champion of the leading team is a full item ahead of his opponent in lane. This opens up far more opportunities than a small advantage of 1000 gold.

Not every advantage is enough to win a game. A **win condition** is a specific type of advantage in sufficient quantity to guarantee a victory.

A team's goal for the game is to achieve its win condition. Note that this depends on the team composition. In other words, different champion combinations have different win conditions.

A team needs a **general game plan** to achieve a win condition. It guides the team's decisions and actions throughout the game. The plan is based on the following factors:

1. Combination of champions in the team.

2. Combination of opponent champions.

3. Each player's plan for the laning phase.

**Combination of champions in the team** determines how they can interact and enhance their capabilities. Players should choose the right strategies for map control and teamfights depending on their champions setup.

**Combination of opponent champions** defines the enemy team's capabilities. Some of them can completely neutralize the capabilities of player's team. Players should take this into account when developing a game plan.

**Player's plan for the laning phase** determines how he intends to gain an advantage during the laning phase. Some champions can rotate and assist their allies during the laning phase. Others are forced to remain in their lane constantly. Otherwise, they will fall behind in the mid game. Players must factor this into their game plan.

There are several typical plans in the current game balance. Players choose one of them in the vast majority of games. These plans work in both competitive and ranked games on all Elo levels.

Here is a list of typical game plans:

1. **Early game aggression**. The team picks champions that are very strong in the laning phase. Examples: Renekton, Lee Sin, Lucian. They outperform their opponents in lane with equal resources thanks to early power spikes from abilities. These power spikes allow them to kill opponents and gain an early resource advantage. The game plan is to accumulate the advantage from small to large.

I> A **power spike** is a moment in the game when a champion becomes significantly stronger. This happens after reaching a certain level or buying a key item.

2. **Late game scaling**. The team has at least one hypercarry champion. Examples: Kayle, Jinx, Smolder, Aurelion Sol. They are weak early on but become very strong in the late game. The plan is to slow down the game and gain resources on par with opponents. The same resources give the hypercarry stronger power spikes than other champions. Then, they dominate teamfights in the mid game. The entire team's plays revolve around hypercarry.

I> **Scaling** is the increase in a champion's power as a result of resource acquisition and over time.

I> **Carry** is a champion with good abilities scaling from AD or AP statistics. He becomes the primary damage dealer in the team after buying a few items. His presence in teamfights is crucial in mid and late game.

3. [**Split push**](https://leagueoflegends.fandom.com/wiki/User_blog:Fistful_of_Force/Split_push.) is a single champion pushing on the side lane. The plan is to create a threat to destroy an enemy tower or inhibitor. This threat forces opponents to react. Therefore, the team gains map control and a number advantage in contesting some objective.

I> [**Pushing**](https://www.mobafire.com/league-of-legends/wiki/game-mechanics/pushing) is the rapid killing of enemy minions in a lane. This is usually done by using a champion's offensive abilities.

4. **Teamfight**. The team picks champions who excel in five-on-five combat. Their abilities allow them to engage or deal area-of-effect (AoE) damage. Examples: Malphite, Amumu, Rumble, Zyra, Brand. The plan is to speed up the game. The team forces frequent fights for objectives on the map. A suitable combination of champions gives the team an advantage in these fights.

5. **Siege**. The team picks champions with long range abilities or auto attacks. Examples: Jayce, Ziggs, Caitlyn, Ezreal, Zoe. The plan is to deal damage to the opponents from a safe distance. This drains dynamic resources of the enemy team. Player and his team should force a fight for the objective on the map once opponents can not act because of lacking resources.

The more champions in a team are suitable for the specific game plan, the better it works. On the other hand, the enemy team could pick champions that completely neutralize the specific game plan. Therefore, players combine several plans in competitive games and on high Elo level. For example, a team picks one hypercarry and several champions that focus on early aggression. This way players compensate weaknesses of their champions.

The team should have a general game plan. Also, an individual player could have it too. Individual game plan is important on low Elo level. It is hard to communicate with the team and reach any agreement quickly on this Elo. Some game plans are built around a single champion (for example, split-push or scaling). Experienced players take these game plans and execute them on their own. This way, they are less dependent on the team's decisions and can achieve the win condition independently.

Let us return to our question: how to turn an advantage into a victory? The team should use its advantage to implement the general game plan. For example, the advantage should be gradually accumulated until it becomes decisive in the "early aggression" plan. Another example, the team's advantage should be realized in the objective contests in the "teamfight" game plan. The team achieves its win condition by doing these.

{pagebreak}
