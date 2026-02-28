## 3.1 Basic attack animation

Every champion in League of Legends has a unique **combo**, which is a sequence of actions that enhances his effectiveness. For instance, an attacking combo increases a champion's damage per second (DPS).

To execute any combo, it is essential to understand how to work with animations. When a player issues an action command, the champion performs specific movements to act. These movements are called **action animation**. Typically, each action has its own distinct animation.

Manipulating animation is a complex but crucial aspect of gameplay. Mastering it requires time and regular practice. Without a solid understanding of how to work with animation, a player may struggle to perform the following tasks effectively:

1. Farm jungle monsters.
2. Farm minions in the lane.
3. Participate in teamfights.
4. Win trades in lane.
5. Win duels in lane or jungle.

I> A **trade** is an exchange of damage between opponents in a lane. Each side aims to inflict more damage on the opponent than it receives in return. A trade is considered successful when one champion gains an advantage in dynamic resources.

In summary, understanding animation is vital for acquiring and utilizing resources effectively in the game. Neither is achievable without this skill.

Let us begin with the simplest animation: a champion's basic attack.

### 3.1.1 Attack speed

A [**basic attack**](https://wiki.leagueoflegends.com/en-us/Basic_attack), also known as an auto-attack or AA, is the standard method for dealing damage to an enemy. Every champion can perform a basic attack. To issue this command, simply right-click on an enemy.

The basic attack animation depends on a champion's stat called **total attack speed** (or total AS). It is calculated based on several components:

1. The champion's **base attack speed** (or base AS).

2. **Bonus attack speed** (or bonus AS) per champion level.

3. Bonus AS from items.

4. Bonus AS from runes.

5. Bonus AS from abilities.

6. Bonus AS from buffs.

7. **Attack speed penalty** from debuffs.

We will calculate total attack speed (AS) using an example. Let us take the champion Ashe, with a base AS of 0.66. The champion's total AS equals the base AS at level 1 when she does not have any items, abilities, attack speed runes, or buffs. This means that Ashe's total AS is currently 0.66.

Let us assume that Ashe purchases the item [Berserker's Greaves](https://wiki.leagueoflegends.com/en-us/Berserker's_Greaves). It provides a 35% bonus to AS. We calculate the total AS using the following formula:
{line-numbers: false, format: text}
```
total_AS = base_AS * (1 + bonus_AS / 100)
```

When we substitute the numbers here, we get the following:
{line-numbers: false, format: text}
```
total_AS = 0.66 * (1 + 35 / 100) = 0.89
```

I> Each champion has an **attack speed ratio** (or AS ratio). This is a multiplier for bonus AS. Most champions have an AS ratio of 1. The Berserker's Greaves item gives them 35% bonus AS. Some champions have an AS ratio less than 1 (for example, Senna and Twisted Fate). The Berserker's Greaves item gives them less than 35% bonus AS.

We have calculated the total attack speed (total AS). It determines the duration of the animation for a single basic attack. This duration is called the **attack cooldown**. Here is the formula to calculate it:
{line-numbers: false, format: text}
```
attack_cooldown = 1 / total_AS
```

We can substitute here the numbers that we got for Ashe with the Berserker's Greaves item:
{line-numbers: false, format: text}
```
attack_cooldown = 1 / 0.89 = 1.12
```

This means that at least 1.12 seconds must pass between two basic attacks. In other words, the champion will not perform the second basic attack until the cooldown has expired.

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

>>>R1

Canceling the auto-attack recovery phase is often used in practice. It has several variants. The **attack move** (attack and move) technique cancels the recovery animation with a move command.

I> The following [video on the Skill Capped channel](https://www.youtube.com/watch?app=desktop&v=-oyxOgtT33U) explains the attack move in detail.

Figure 3-2 shows the timeline diagram for the attack move technique.

{caption: "Figure 3-2. The timeline diagram for the attack move technique", width: "100%"}
![Attack move timeline](images/Micromanagement/ashe-attack-move.png)

The steps of this technique are as follows:

1. At point A, the player issues an attack command. The champion plays the windup animation phase.

2. At point B, the champion begins the firing phase.

3. On segment B-C or at point C, the player issues a move command. The champion begins moving immediately after the firing animation completes. This occurs on segment C-D, which lasts 1.13 seconds.

4. At point D, the basic attack cooldown timer ends. From this point on, the player can issue the next attack command.

The attack move technique is used in two situations:

1. To pursue and damage an enemy.

2. To retreat and damage an enemy.

In the **first case**, the technique increases damage to a retreating enemy. Let us look at the difference between the attack command and the attack move:

* If you issue an **attack command** to a champion, he will stand still and play through all three animation phases. When an enemy moves out of Ashe's attack range, she will only react to this at point D. In other words, she will begin moving after the recovery phase ends.

* If you use **attack move**, the champion will move toward the enemy instead of playing the recovery animation. This means that Ashe will react to his movement much faster.

In the **second case**, the technique reduces damage to the retreating player's champion. Let's consider the difference between the attack move and individual commands:

* If a player issues an **attack command**, the champion stands still and plays all three animation phases. In this case, he simply trades damage with the enemy. This exchange is called a [**stat check**](https://www.reddit.com/r/leagueoflegends/comments/10q7lmk/comment/j6ob8tk/). The champion with the higher stats wins it.

* A player can issue a **move command** and only retreat. In this case, he will take damage until he moves out of the enemy's attack range. The enemy will not take any damage during this time.

* If you use **attack move**, the champion will trade damage with the enemy while maintaining distance from him. This opens up two possibilities. A player can either retreat if he loses the trade or go all-in if he wins it.

I> **All-in** term means an active fight to victory, using all available champion's abilities and attack methods. An all-in typically ends with the death of one of the participants if it is a duel.

When a ranged champion uses an attack move against a melee opponent, it is called **kiting**. If the champion's movement speed is greater, the opponent will be unable to attack him.

### 3.1.4 Execution of the attack move

>>>R1

Let us look at how to perform an attack move in practice. To do this, you need to change two game settings and a mouse setting.

The **first game setting** is located in the "HOTKEYS" tab and is called "Player Attack Move Click" hotkey. Figure 3-3 shows it.

{caption: "Figure 3-3. 'Player Attack Move Click' hotkey", height: "50%"}
![Player Attack Move Click hotkey](images/Micromanagement/options-player-attack-move-click.png)

This hotkey issues a movement command to a specified point. As soon as an enemy is within attack range, the champion will begin attacking him. You need to assign the A key to this action. Then, when you press it, the champion will attack the closest target within attack range.

The **second game setting** is located in the "GAME" tab and is called "Attack move on cursor". Figure 3-4 shows it.

{caption: "Figure 3-4. 'Attack move on cursor' setting", width: "100%"}
![Attack move on cursor setting](images/Micromanagement/options-attack-move-on-cursor.png)

Changing this setting provides the following effect:

* Enable — the attack move command (A key) selects the target closest to the mouse cursor.

* Disable — the attack move command (A key) selects the target closest to the champion.

You need to enable this setting. Then you can select an attack target using the mouse cursor position.

**The third setting** is to turn off mouse acceleration in the OS settings. Here are the steps for Windows 11 users:

1. Click "Start" -> "Settings". The "Settings" window will open.

2. Select the "Bluetooth & devices" option in the left-side menu.

3. Select the "Mouse" item in the right part of the window. The mouse settings menu will open.

4. Disable the "Enhance pointer precision" option.

Figure 3-5 shows turning off mouse acceleration.

{caption: "Figure 3-5. 'Enhance pointer precision' setting", width: "100%"}
![Enhance pointer precision setting](images/Micromanagement/mouse-acceleration-disable.png)

This setting controls mouse acceleration. When it is enabled, the position of the pointer depends on two factors:

1. The distance you move the mouse.

2. The speed at which you move the mouse.

Mouse acceleration is useful when working on large monitors. But it greatly hinders the development of muscle memory in all computer games. Therefore, you should turn off this option. Then, the pointer position will depend only on the distance you move the mouse, but not on the speed.

Now, let us look at how to perform an attack move technique with the new settings. Perform the following steps to execute it:

1. Move the mouse cursor close to the target. It does not have to be exactly on the target.

2. Press the A hotkey. The champion will begin the windup phase of the attack animation.

3. Move the mouse cursor to the point where you want the champion to move. This should be either toward or away from the enemy.

4. When the champion begins the firing or recovery phase, right-click. The champion will move to the specified point.

5. Calculate the auto attack cooldown timer. When it ends, begin your next attack from step 1.

When performing the attack move technique, players make the following common mistakes:

* Issuing the move command too early. If it happens during the windup phase, it cancels the champion's attack. This significantly reduces the champion's DPS.

* Allows the champion to move longer than his attack cooldown timer. This prevents the champion from utilizing his high attack speed.

Practice the attack move technique in the "Practice Tool" mode. Get a feel for your champion's attack rhythm at different levels and with different items. Then you will learn to attack precisely when the cooldown timer ends.

Note the relationship between attack speed and the champion's movement pattern. With low attack speed, the champion moves with long segments. With high attack speed, these segments are shortened.

### 3.1.5 Basic attack and using an ability

>>>R1

We have looked at canceling an attack animation with a move command. This is only one of four methods. Here is a full list of actions that cancel the attack animation:

1. Movement
2. Champion ability
3. Summoner spell
4. Active item ability.

Let us look at the second option: canceling an attack animation with a champion ability. We can call this technique similar to the first option — **attack ability** (attack and ability). The third and fourth options work in the same way.

Figure 3-6 shows the timeline diagram for the technique when a champion ability cancels an attack animation.

{caption: "Figure 3-6. The timeline diagram for the attack ability technique", width: "100%"}
![Attack ability timeline](images/Micromanagement/ashe-attack-ability.png)

The steps of this technique are as follows:

1. At point A, the player issues an attack command. The champion plays the AA windup animation phase.

2. At point B, the champion begins the AA firing phase.

3. On the B-C segment or at point C, the player issues the W command. The champion begins its animation immediately after the AA firing phase ends. This occurs on the C-D segment and beyond.

4. At point D, the auto-attack cooldown timer ends. From this point on, the player can issue the next attack command.

The attack ability is used when maximum damage per second (DPS) is needed. The target should be within attack and ability range. This works especially well against a rooted target. If the target moves out of range, the player will have to alternate between attack moves and attack ability techniques.

### 3.1.6 Execution of the attack ability

>>>R1

You need to set all champion's abilities to "Quick Cast to perform the attack ability technique effectively. This setting is located in the "HOTKEYS" tab. Figure 3-7 shows it.

{caption: "Figure 3-7. 'Quick Cast All' setting", width: "100%"}
![Quick Cast All setting](images/Micromanagement/quick-cast.png)

You need to press the "Quick Cast All" button in the "HOTKEYS" tab. This will cause the champion to cast the ability as soon as you release the corresponding key (e.g., W). You no longer need to press the key twice. This significantly speeds up in-game actions, but it takes some getting used to.


Please note that some abilities with [**charge**](https://wiki.leagueoflegends.com/en-us/Channel#Charged_Abilities) should not be set to Quick Cast. If a champion can move while charging, he can change his position with a summoner spell [**Flash**](https://wiki.leagueoflegends.com/en-us/Flash). Holding down the Quick Cast key while flashing is inconvenient. It is easier to execute when the ability is set to Normal Cast (the default). Here are some examples of abilities that do not require Quick Cast: Vi Q, Viego W.

Now, let us look at how to perform the attack ability technique with abilities that are set to Quick Cast. Perform the following steps to execute it:

1. Move the mouse cursor close to the target. It does not have to be exactly on the target.

2. Press the A hotkey. The champion will begin the windup phase of the attack animation.

3. Position the mouse cursor so the ability hits the target.

4. When the champion begins the firing or recovery phase, press the ability hotkey. The champion will use it instead of playing the recovery animation.

A common mistake when performing this technique is to use the ability during the windup phase of the attack animation. In this case, the champion cancels the auto-attack and uses the ability. This greatly reduces the champion's DPS and can break the combo.

You can practice the attack ability technique in the "Practice Tool." Try to remember two things about your main champion:

1. What your champion's firing animation looks like, as well as its approximate timing at different levels and items. Then you would not cancel it with an ability.

2. The area of ​​effect of all abilities. This way, you would not have to hold down buttons to check the radius of abilities. This can save seconds that can decide the outcome of the fight.

{pagebreak}
