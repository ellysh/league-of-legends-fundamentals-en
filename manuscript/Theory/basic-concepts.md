## 2.1 Basic concepts

In this section, we will review the fundamental concepts of the game. It would be beneficial to organize them systematically. For this purpose, the following list of questions will assist us:

1. What is the initial state of the objects on the map?

2. What disrupts the equilibrium of the objects?

3. What actions are advantageous?

4. How to identify an advantage?

5. How to acquire an advantage?

6. How to turn an advantage into a victory?

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

You can identify three types of equilibrium on the map:

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

We have considered three types of equilibrium for game objects. Each type is dynamic. This means that if something disturbs the equilibrium of an object, it returns to its original state over time. Let us explore some examples.

Abilities of certain champions can disrupt the **landscape equilibrium**. They create new walls (Anivia W) or passages (Bard E). These actions disturb the balance of static objects. However, the effects of such abilities are temporary. The landscape will revert to its original state after a few seconds.

When a player destroys an object, it disrupts the **resource equilibrium**. First, the player receives a reward that the enemy can no longer obtain. Second, the destroyed object disappears from the map. For example, killing a jungle monster leaves its camp empty. Nevertheless, the monster will respawn at its camp after a specific period. The respawn time varies by monster type and ranges from 2 to 6 minutes.

The dynamic **equilibrium of power** between teams is more intricate. First, only some structures can recover after being destroyed, while others cannot. Second, the minion clash front can shift along its lane. If it strays from the center of the lane, it will gradually return to the center. We will discuss this mechanics in more detail in section "4.1 Minion wave management."

### 2.1.2 Action

Here is the second question on our list:

> What disrupts the equilibrium of the objects?

Player champions are the only entities capable of disrupting the equilibrium of game objects. Even their mere presence on the map alters the balance of the teams. This happens because cannot select the same champion.

When a champion takes action, it affects a game object and changes its state. This disrupts one of the three types of equilibrium.

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

We have examined the actions of player champions. It is important to emphasize that players act within strict boundaries. These boundaries are dictated by the game's design and balance, as developers aim for each game to follow a specific scenario. To achieve this, they adjust the parameters of game objects to ensure players benefit from adhering to that scenario.

A typical ranked game scenario can be divided into three phases:

1. Laning – the beginning.
2. Mid game – the middle.
3. Late game – the end.

The **laning** phase begins at the first second and lasts until approximately the 14th minute. It ends when players destroy the first tower on any lane. The primary goals for teams during this phase are to gather resources and prevent the enemy from doing the same.

During the laning phase, players are distributed across the map to maximize their income. It comes from enemy minions and jungle monsters. Therefore, at least one champion should occupy each lane and the jungle.

The standard champion distribution across the map during the laning phase is as follows:

1. One player goes to the top lane.

2. One player goes to the mid lane.

3. Two players (the ADC and the support) go to the bottom lane.

4. One player goes to the jungle.

Typically, two players occupy the bot lane. One of them is the support, who does not kill minions. Instead, the support has a special item that provides gold in an alternative way.

The **mid game** phase typically begins at the 14th minute and lasts until the 25th minute. It ends around the time when players complete their third item. During this phase, teams aim to achieve the following goals:

1. Control the map.
2. Capture objectives.

I> An **objective** refers to an epic jungle monster or enemy structure. Destroying an objective increases the team's strength or provides significant rewards. Objectives include dragons, Herald, Baron Nashor, Voidgrubs, enemy towers, and inhibitors.

When the mid game phase begins, players often swap their lanes. The standard lane swap occurs as follows:

1. The ADC moves from the bot lane to the mid lane.

2. The top laner moves from the top lane to the bot lane.

3. The mid laner moves from the mid lane to the top lane.

These swaps allow the team to control the map better. The champions' abilities for each role dictate which lane they should occupy during the mid game. We will discuss this topic in more detail in section "4.2 Map Control."

During the mid game, champions frequently leave their lanes to group up. Grouping allows them to contest objectives more effectively.

I> **Contest** refers to the battle between teams for a specific objective, such as a building or an epic monster.

The late game phase begins around the 25th minute. By this time, teams usually have destroyed all T1, T2, and T3 towers on one or more lanes.

The goals for teams in the late game phase include:

1. Winning decisive team fights.

2. Capturing epic monsters.

3. Destroying structures in the enemy base (T3 and T4 towers, inhibitors, and the Nexus).

Teams often engage in five-on-five fights during the late game. The outcome of these battles determines which team gains control of the next epic monster. Victory in a decisive teamfight allows the destruction of the enemy's T4 towers and Nexus.

### 2.1.4 Advantage

Now we reach the third question in our list:

> What actions are advantageous?

Let us look at an example to answer this question. At the beginning of the laning phase, both mid laners arrive in their lane. The players should choose and execute some action every second. If we limit the list of possible actions to the mid lane scope, the players have the following options:

1. Attack the enemy champion.
2. Attack the enemy tower.
3. Farm enemy minions.
4. Retreat to a safe area under the ally tower.

In this context, there is an equilibrium of power in the mid lane. This means that the minion clash is in the middle of the lane, with equal numbers of minions on both sides. Additionally, both champions have similar health, mana, levels, and items.

What options does the blue team's mid laner have?

**First**, attacking the enemy champion is risky because of the equilibrium of power. There is a 50% chance the player will kill the opponent and receive a reward. But there is also a 50% chance that the player will die, allowing the opponent to gain a reward instead. Therefore, attacking the enemy champion is a disadvantageous action that does not increase the team's chances of winning.

**Second**, the player cannot attack the enemy tower without the support of allied minions. They should absorb the tower's shots while the champion attacks the structure. If the champion tries to do this without minions, the tower will quickly kill him. Thus, attacking the enemy tower in the current situation is unprofitable.

**Third**, farming enemy minions is a standard action during the laning phase. This maintains resource equilibrium between the mid laners. If the blue team's player excels at last-hitting minions, he can gain an advantage with minimal risk. This is the best scenario in the current situation.

**Fourth**, retreating to a safe zone means giving up farming. This decision provides the enemy mid laner with a resource advantage. Therefore, this is also a disadvantageous action that increases the enemy team's chances of winning.

Now, let us assume that the situation changes and the blue team's jungler comes to the mid lane. This increases the chances of killing the red team's mid laner. Thus, attacking him becomes a profitable action.

What happened in our example when the jungler appeared? The blue team gained a numerical advantage in the mid lane. This brings us to the second fundamental concept: advantage. It follows from the concept of equilibrium.

A team gains an **advantage** when any type of equilibrium shifts in its favor. Every player can gain an advantage in a similar manner when the equilibrium on his lane shifts in his favor.

Advantage comes in various forms, depending on which type of equilibrium has been disrupted. Experienced players identify the following types of advantages:

1. **By quantity** — one team has more champions participating in a team fight than the other.

2. **By items** — one or more champions on the team have more items than their opponents, or these items are of higher value.

3. **By level** — one or more champions on the team are at a higher level than their opponents.

4. **By resources** — one or more champions on the team have one of the following resources, while their opponents do not:

   * health

   * mana

   * ready-to-use [**summoner spells**](https://wiki.leagueoflegends.com/en-us/Summoner_spell)

   * ready-to-use [**abilities**](https://wiki.leagueoflegends.com/en-us/Champion_ability), especially ultimate

   * individual or team [**buffs**](https://wiki.leagueoflegends.com/en-us/Buff) received for killing a neutral monsters.

5. **Map control** means a team has vision and influence over key areas of the map. Vision is provided by special items called [**wards**](https://wiki.leagueoflegends.com/en-us/Ward). Influence is gained when champions are within range of key points on the map. We will discuss this concept in section "4.2 Map Control."

6. **Positional advantage** has two meanings. First, a champion holds a favorable position in a lane compared to his opponent. Second, a team has an advantageous position before the teamfight. Here are examples: flanking, controlling narrow passages, or zoning out the enemy team.

7. **By team composition** — The champions on one team synergize and enhance each other's abilities better than those on the opposing team.

8. **By tempo**. We will explore the concept of tempo further.

It is important to note that a team can hold multiple types of advantages simultaneously. At the same time, opponents may also have advantages, but of a different kind.

Let us look at the example. The blue team has a stronger champion composition and better map control. The red team has the [**Elder Dragon**](https://wiki.leagueoflegends.com/en-us/Dragon_Slayer#Aspect_of_the_Dragon) buff. The dragon buff is the decisive advantage in this case. A **decisive advantage** disrupts the equilibrium of power between teams or champions in a lane more significantly than other types of advantages.

Additionally, the significance of each type of advantage can vary depending on the current state of the game. For instance, during the laning phase, a level advantage is generally more critical than an item advantage. This holds true until champions reach level 6. Therefore, a level advantage is crucial in the early minutes, while item advantages become more impactful after level 6.

Let us revisit the question we asked at the beginning of this section. Here are beneficial actions ranked in descending order:

1. Utilize the existing advantage.

2. Take actions that provide some type of advantage.

3. Perform actions that are standard in the current conditions.

**Utilizing an advantage** is generally the most beneficial action. A team or individual champion may already be stronger than the enemy, and players should capitalize on this strength to gain an advantage. For example, contest an objective when the team has a numerical advantage.

**Taking actions that provide some type of advantage** is the second most beneficial choice. If a player can shift the balance of power in his favor, he should take advantage of that situation. For instance, attack a dragon to secure its buff.

**Performing standard actions** is the least advantageous option. This type of action typically aims to maintain the current equilibrium of team power. A player will only gain an advantage from a standard action if he executes it significantly better than his opponent. The example is farming minions in the lane.

### 2.1.5 Macro cycle

Here is the fourth question on our list:

> How to identify an advantage?

A player needs two key elements to identify an advantage:

1. Learn templates for recognizing typical game situations.

2. Manage his attention during the game effectively.

We will explore templates for various gameplay aspects and appropriate actions further in this book. Now, let us discuss attention management.

There is a concept of a macro cycle in real-time strategy (RTS) games. A **macro cycle** is an approach to effectively managing the game's economy. The idea is to create a list of tasks and execute them sequentially.

Here is an example macro cycle for a typical strategy game:

1. Produce workers.
2. Deploy workers to mine resources.
3. Produce military units.
4. Construct new buildings.
5. Perform technical upgrades.

When a player follows a macro cycle, they perform the actions in the order listed. Upon reaching the last action, the player restarts the list.

The advantage of a macro cycle is that it helps players remember essential tasks. Repeated use of the macro cycle builds a strong habit. If an action is included in the list, the player is likely to perform it without expending unnecessary cognitive resources on memorization. This approach ensures that attention is evenly distributed across all aspects of the game.

Random events occur in any strategy game. Some of these events require the player's full attention. Once the issue is resolved, the player must return to the macro cycle, which serves as his default mode.

League of Legends does not incorporate an economy in the same way as a typical strategy game. Players do not build a base or produce new units. However, the idea of ​​a macro cycle remains relevant. The game encompasses multiple aspects, so players need to balance their attention among them.

A common mistake among new players is focusing exclusively on one aspect of the game. For instance, a novice top laner might concentrate only on the enemy minion wave, striving not to miss any last-hitting opportunities. This narrow focus can prevent the player from noticing his champion's health, mana, or level. As a result, the player may fail to recognize when he has a health, mana, or level advantage, missing the opportunity to capitalize on it. A macro cycle can help players avoid such mistakes.

The macro cycle for each of the five team roles varies. For instance, let us examine the macro cycles for a mid laner and a jungler.

Figure 2-2 shows the map objects that a mid laner must monitor.

{caption: "Figure 2-2. Macro cycle for mid laner", height: "50%"}
![Mid laner macro cycle](images/Theory/map-season-13-midlaner-macrocycle.png)

You see the expanded version of Figure 2-1. It has the blue and red circles that mark the champions of each team.

Now, let us take a closer look at Figure 2-2. The pink circle with the number 1 marks the blue team's mid laner. The pink text indicates the objects that the player should check during his macro cycle. These objects are as follows:

1. State of his own champion:

   * Health
   * Mana
   * Level
   * Ready-to-use abilities
   * Ready-to-use runes
   * Items and readiness of their effects.

2. State of the enemy champion on the lane:

   * Health
   * Mana
   * Level
   * Ready-to-use abilities (remember cooldowns)
   * Ready-to-use runes (remember cooldowns)
   * Items.

3. Enemy minions wave:

   * Is there a minion available for last hitting?
   * Total number of minions in the wave
   * Location of the next wave (symmetric to the next allied wave).

4. Allied minion wave:

   * Is there a minion available for last hitting?
   * Total number of minions in the wave
   * Location of the next wave.

5. Allied or enemy tower if it is nearby:

   * Health and plate count
   * Attack range.

6. Minimap:

   * Location of the allied jungler
   * Location of the enemy jungler (requires tracking skill)
   * State of adjacent lanes (minion wave positions, presence of champions)
   * State of nearby jungle monster camps (especially epic ones: Herald, Baron, Dragon).

7. Game stats (accessed by pressing the Tab key):

   * Levels of all champions
   * Items of all champions.

I> [**Cooldown**](https://wiki.leagueoflegends.com/en-us/Cooldown) (CD) occurs immediately after using an ability. It is the period when the ability is unavailable. Cooldowns apply not only to champion abilities but also to runes, summoner spells, and item effects.

This list highlights the objects and game aspects a player should consistently monitor. A typical pattern may emerge in one of them. This pattern could indicate a temporary advantage and an opportunity to capitalize on it. It is impossible to notice the pattern without focusing on the corresponding game object.

> To find a pattern in something, you have to look at it.

Let us examine the macro cycle of the blue team's jungler. This role is distinct because the player spends almost the entire laning phase in the jungle. Therefore, his macro cycle is significantly different from that of other roles.

Figure 2-3 illustrates the key elements in the jungler's macro cycle.

{caption: "Figure 2-3. Macro cycle for jungler", height: "50%"}
![Jungler macro cycle](images/Theory/map-season-13-jungler-macrocycle.png)

The blue team's jungler is marked with a pink circle with the number 1. The elements in his macro cycle include:

1. State of his own champion:

   * Health
   * Mana
   * Level
   * Ready-to-use abilities
   * Ready-to-use runes
   * Items and readiness of their effects.

2. Location and state of the enemy jungler (requires tracking skill):

   * Minimap
   * Game stats window.

3. Nearest jungle monster camps:

   * Current target for farming
   * Next target for farming.

4. Lane state, starting with the closest:

   * Position of the minion wave
   * Presence of champions in the lane
   * State of champions (health, mana, level, items).

5. Next epic monster to contest:

   * Respawn timer
   * Allied champions in range
   * Enemy champions in range

6. Game stats (accessed by pressing the Tab key):

   * Levels of all champions
   * Items of all champions.

Keep in mind that a jungler cannot gather all necessary information from the minimap alone. It's essential to switch the camera to each lane and assess what is happening there. Using the hotkeys F1, F2, F3, and F4 is the most efficient method for this. The [following video](https://www.youtube.com/watch?v=pizMcCWv8y8) explains how to configure these hotkeys.

To gradually incorporate the macro cycle into your gameplay, follow these steps:

1. Make a minimal list of actions to repeat. A solid starting point might include:

   * Checking game objects on the main screen
   * Checking the minimap
   * Viewing game stats by pressing the Tab key.

2. Install and set the [metronome app](https://play.google.com/store/apps/details?id=com.andymstone.metronome&hl=en) to 15 seconds. This will provide a consistent sound signal.

3. When you hear the signal, perform your macro cycle. Consistently switch your focus between the items on your list.

4. If a game event distracts you, process that event first. Then return to your macro cycle and start over.

You can begin practicing the macro cycle in "Co-op vs. AI" mode. It will be easier to manage your focus there. The minimal macro cycle will soon become a habit. Afterwards, you can add new actions to the list as you identify them as essential. Gradually decrease the time between sound signals.

Distributing your attention across the game's key elements is crucial for every role, particularly for the jungler. If jungler is your primary role, you need to master a minimal macro cycle before your next ranked game.

### 2.1.6 Tempo

Here is the fifth question on our list:

> How to acquire an advantage?

Experienced players accumulate advantages **from small to large**. This is the most reliable way to win against an equally strong opponent.

A player begins to gain an advantage when one type of equilibrium shifts in his favor. He should recognize this shift and take advantage of the opportunity. This means the player should follow a plan in which each step provides a small benefit, gradually leading to a significant advantage.

Tempo is the starting point from which experienced players begin to build an advantage. Let us explore what this term means.

There is a concept called a turn in turn-based strategy (TBS) games. A **turn** is a specific moment in time when a player is allowed to act. Turns follow one another in sequence. Each player acts on his turn.

League of Legends is a real-time game. Its mechanics allow players to act continuously. The only exception to this is when a player dies. In this case, he must wait for a respawn timer. However, the game does have a concept akin to a turn, called a play.

I> A **play** is a single action taken by a team or player that pursues a specific goal. Examples are taking an epic monster or destroying an enemy tower.

A team and each of its champions can only operate effectively under certain conditions. Two factors determine these conditions: available resources and players' positions on the map. If resources are available and the positions are favorable, a play can be made. Otherwise, the team or champion cannot act.

The conditions under which a team or champion can operate effectively are called [**tempo**](https://wiki.leagueoflegends.com/en-us/Snowball#Qualities). Coach Kairos explains this concept in detail in [this video](https://www.youtube.com/watch?v=vHVeltI0IkE). He provides the following **tempo formula** for a specific champion:
{line-numbers: false, format: text}
```
tempo = champion power / distance to object
```

**The first part of the formula** is champion power. It is the sum of the champion's primary resources. We can categorize these resources into two types:

1. Static
2. Dynamic.

**Static resources** are those that a champion has already acquired and cannot lose. Here are examples: level, items, gold, and permanent stacks of specific abilities.

**Dynamic resources** are those that a champion can spend or lose. Examples include: health, mana, temporary buffs, cooldowns of abilities, summoner spells, and item effects.

We have previously discussed the equilibrium of game objects. One form of this is resource equilibrium, which restores over time. It is obvious that dynamic resources restore over time. For example, each champion passively recovers health and mana, even without returning to the fountain. Additionally, his abilities and item effects also recharge after a cooldown.

It is less obvious that the equilibrium of static resources also restores over time. Here is an example. The blue team's mid laner is the first player to reach level 18 and acquire all six items. This gives him a significant advantage that can lead his team to victory. However, if the game drags on, the red team comes back. After some time, every red champion will reach level 18 and get all six items. Consequently, the blue mid laner, who initially had an advantage in static resources, will eventually lose that advantage. This way, the balance of power between the teams is restored, along with the equilibrium of static resources.

Coach Kairos suggests evaluating only a portion of a champion's static and dynamic resources for simplicity. Table 2-1 shows these resources.

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

It is important to note that resources serve as the multiplier. This means that health and mana are crucial factors. A champion has no tempo at low health, regardless of his other stats.

**The second part of the tempo calculation formula** is the distance to the object. The object can be anything, not just an epic monster or an enemy building. In the context of tempo, this could include a lane for a gank, a teamfight, a jungle camp, or even a minion wave.

Tempo is calculated with respect to a specific map object. For example, suppose a champion is on the bottom lane. His tempo on a dragon will be high, but his tempo on Baron will be low.

The distance to an object is measured in seconds required to reach it. For instance, if a player is at the base but has a teleport spell available, his distance to the object is considered small.

Coach Kairos suggests using a scale from 1 to 10 to estimate a champion's distance to an objective:

* 1 — the champion is already at the objective.
* 5 — the champion is halfway to the objective.
* 10 — the champion is at the base or dead.

Let us calculate the tempo for a specific example. There is a blue jungler Viego. We want to know his tempo on the dragon. For simplicity, we will only consider the junglers of both teams and ignore other champions.

Viego has full health and mana, giving him a resource score of 3. He is at level 8, while the red jungler Ekko is at level 6. This means Viego's stats score is 5. Viego has purchased his first item, whereas the enemy jungler has not yet acquired one. Then Viego's items score is 4. All of Viego's abilities and spells are ready, resulting in a cooldown score of 5. As Viego enters the lower river from his jungle, his distance to the objective is 2.

Here is Viego's tempo on the dragon:
{line-numbers: false, format: text}
```
tempo = 3 * (5 + 4 + 5) / 2 = 21
```

This is a very high value.

Next, we will calculate the tempo of the red jungler Ekko, who is currently in the top jungle. His distance to the object is 7. His resources are the following:

* Full health and mana: resources = 3.

* He is at level 6 while the enemy is level 8:
stats = 1.

* He does not have his first item while the enemy does: items = 2.

* All abilities and spells ready: cooldowns = 5.

Here is Ekko's tempo on the dragon:
{line-numbers: false, format: text}
```
tempo = 3 * (1 + 2 + 5) / 7 = 3.4
```

This results in a very low value, indicating that Ekko cannot contest the dragon.

Coach Kairos' formula shows how a player can increase his tempo. To do this, a player needs to gain one of the following advantages:

1. Resource advantage (health, mana).

2. Champion level advantage.

3. Item advantage.

4. Cooldown advantage for abilities, spells, and item effects.

5. Proximity to the objective.

This list works both ways: if the opponent has any of these advantages, he gains tempo. Consequently, the player loses tempo.

Coach Kairos suggests calculating a team's tempo as the sum of each player's tempo. The formula looks as follows:
{line-numbers: false, format: text}
```
team tempo = top tempo + jungle tempo + mid tempo + adc tempo + support tempo
```

By applying this formula to both teams, you can determine which one currently has the tempo for a specific object. The team that has tempo is more likely to win the fight and secure the objective.

A player can easily gain a slight tempo advantage by moving closer to the objective. However, the tempo advantage is dynamic. It creates a window of opportunity when a team or player can exploit the advantage. If this opportunity is missed, the tempo advantage becomes useless.

### 2.1.7 Victory condition

Here is the final question on our list:

> How to turn an advantage into a victory?

We already know that there are different types of advantages. The advantage within a given type can also vary in quantity. For instance, let us compare the gold gap between teams with 1000 and 14000 gold. In the second scenario, every champion of the leading team is a complete item ahead of his opponent in the lane. This opens up far more opportunities than a 1000-gold advantage.

However, not every advantage guarantees a win. A **win condition** is a specific type of advantage in sufficient quantity to secure a victory.

A team's goal for the game is to achieve its win condition. Note that this goal is influenced by team composition. In other words, different champion combinations have different win conditions.

A team needs a **general game plan** to achieve a win condition. It guides the team's decisions and actions throughout the game. The plan is based on the following factors:

1. The combination of champions in the team.

2. The combination of the opponent's champions.

3. Each player's plan for the laning phase.

**The combination of champions in the team** determines how they can interact and enhance each other's capabilities. Players should choose the right strategies for map control and teamfights depending on their champions setup.

**The combination of opponents' champions** defines the capabilities of the enemy team. Some enemy champions may completely neutralize the capabilities of the player's team. Players should take this into account when developing a game plan.

**Player's plan for the laning phase** determines how he intends to gain an advantage before the mid game starts. Some champions can rotate and assist their allies during the laning phase. Others are forced to remain in their lane constantly. Otherwise, they will fall behind in the mid game. Players must factor this into their game plan.

There are several typical game plans in the current League of Legends balance. Players choose one of them in the vast majority of games. These plans work in both competitive and ranked matches across all Elo levels.

Here is a list of typical game plans in League of Legends:

1. **Early game aggression**. The team picks champions who are very strong during the laning phase. Examples include Renekton, Lee Sin, and Lucian. These champions outperform their opponents in the lane with equal resources due to their early power spikes from abilities. These power spikes enable them to secure kills and gain an early resource advantage. The game plan is to build this advantage from small to large.

I> A **power spike** is a moment in the game when a champion becomes significantly stronger. This happens after reaching a certain level or buying a key item.

2. **Late game scaling**. The team has at least one hypercarry champion. Examples include Kayle, Jinx, Smolder, Aurelion Sol. These champions may be weak early on, but become exceptionally powerful in the late game. The plan is to slow down the game and gain resources on par with opponents. The same resources give the hypercarry stronger power spikes than other champions. Then they dominate teamfights in the mid and late game. The team's plays revolve around hypercarry.

I> **Scaling** is the increase in a champion's power as a result of resource acquisition.

I> **Carry** is a champion whose abilities scale well with Attack Damage (AD) or Ability Power (AP). He becomes the primary damage dealer for the team after buying key items. His presence in teamfights is crucial in the mid and late game.

3. [**Split push**](https://leagueoflegends.fandom.com/wiki/User_blog:Fistful_of_Force/Split_push.). This strategy involves a single champion pushing a side lane. The game plan is to create a threat to destroy an enemy tower or inhibitor, forcing opponents to react. This reaction gives the team map control and a numerical advantage when contesting objectives.

I> [**Pushing**](https://www.mobafire.com/league-of-legends/wiki/game-mechanics/pushing) is the rapid killing of enemy minions in a lane. This is usually done by using a champion's damaging abilities.

4. **Teamfight**. The team picks champions who excel in five-on-five combat. These champions have abilities that allow them to engage opponents or deal area-of-effect (AoE) damage. Examples include Malphite, Amumu, Rumble, Zyra, Brand. The plan is to accelerate the pace of the game and force frequent fights for objectives on the map. A well-combined roster of champions provides the team with an advantage in these plays.

5. **Siege**. The team picks champions with long-range abilities or auto-attacks. Examples include Jayce, Ziggs, Caitlyn, Ezreal, Zoe. The game plan is to deal damage to the opponents from a safe distance. This drains the enemies dynamic resources. The team should force a fight for the objective once opponents are unable to act due to a lack of resources.

The effectiveness of a game plan increases with the number of champions on a team that align with it. However, the enemy team can also select champions that counter a specific game plan. Therefore, experienced players combine several plans in competitive games and at high Elo levels. For instance, a team might pick one hypercarry accompanied by several champions that focus on early aggression. This way, players compensate for the weaknesses of their champions.

The team should have a general game plan. Also, an individual player could have it too. An individual game plan is essential at low Elo levels, where it is challenging to communicate with teammates and reach consensus quickly. Some game plans are built around a single champion, such as split-pushing or scaling. Experienced players can execute these plans on their own. This way, they are less dependent on team decisions and can achieve the win condition independently.

Let us return to our question: how to turn an advantage into a victory? The team must utilize its advantage to implement its general game plan. For instance, the players should gradually accumulate the advantage until it becomes decisive in the "early aggression" plan. Another example, the players should capitalize on their advantage in the objective contests in the "teamfight" game plan. The team achieves its win condition by consistently adhering to the game plan.

{pagebreak}
