## 3.2 Ability animation

>>>R1

The basic attack pattern is the same for all champions: it always has three phases. The proportions of these phases vary. For example, Volibear's windup phase takes up 30% of his attack animation, while Ashe's only 21.93%. The base attack speed and its growth per level also vary. But these are minor details. The algorithms for executing the attack moves and attack ability techniques are the same for all champions.

Working with ability animations is much more complex. Abilities are executed according to different algorithms and interact differently with the champion's other actions. This is an advanced micromanagement topic. Let us look at its basic techniques.

### 3.2.1 Phases of ability animation

>>>R1

When a player issues an ability command, the champion performs its full animation cycle. It has the same phases as auto-attack for most abilities:

1. **Windup** — the preparation for action.

2. **Firing** — the execution of the strike, shot, or application of an effect.

3. **Recovery** — the return to the starting position.

Let us consider abilities with these three phases as a **basic scheme**. Some abilities deviate from it. We will consider these differences as deviations from the basic scheme.

We start with simple abilities that fit within the basic scheme, for example, Ashe W.  Figure 3-8 shows its timeline diagram.

{caption: "Figure 3-8. The timeline diagram for Ashe's W ability", width: "100%"}
![Ashe W ability animation timeline](images/Micromanagement/ashe-w-ability-animation.png)

Let us look at the diagram step by step:

1. At point A, the player issues the ability command. The champion performs the windup animation phase: drawing the bowstring. This always lasts 0.25 seconds for the W ability.

2. At point B, the champion begins the firing phase: firing a volley of arrows. This lasts approximately 0.1 seconds.

3. At point C, the champion begins the recovery phase: drawing the next arrow from the quiver. This lasts approximately 1.65 seconds.

4. At point D, the champion completes the full animation cycle. Two seconds have passed since the player issued the command at point A.

Note that the duration of all phases of the W ability animation is constant. It does not depend on attack speed, champion level, or ability level. However, the animation of some abilities does depend on this.

We have considered the basic scheme of an ability animation. There are two main deviations from it:

1. **Charging** replaces the windup phase.

2. **Channeling** replaces the firing phase.

3. There is no windup phase. The ability animation begins with firing.

If a charging replaces windup or channeling replaces the firing phase, its meaning remains the same. The difference is that the corresponding phase lasts longer. The replacement rules are as follows:

* If a charging replaces a windup, the champion prepares to cast the ability during this phase. After this, he performs the firing animation.

* If a channeling replaces a firing animation, this phase begins after the windup. During the channeling, the champion deals damage or applies some effect.

You can cancel or change the animation of one of the phases of abilities: windup, firing, or recovery. There is no general rule here. It all depends on the specific ability and the champion.

### 3.2.2 Ability classification

>>>R1

Let us focus only on the abilities animation. Their effects are not so important right now. We can divide all abilities into five types. Each has its own specific animation pattern.

If two abilities have the same animation pattern, then you can work with them using the same techniques. Therefore, classification is important. Using it, you do not need to memorize the rules for every ability in the game. Instead, it is enough to remember how animation works for each ability type.

Table 3-1 lists all possible ability types by animation pattern.

{caption: "Таблица 3-1. Champion abilities classification by animation pattern", width: "100%"}
| Ability type | Moves Champion | Animation Phases | Examples |
|  | | | |
| --- | :---: | --- | --- |
|  | | | |
| Auto-attack modifier | No | Windup, firing, recovery | Vi - E, Volibear - Q, Jax - W |
|  | | | |
| Static slow ability | No | Windup, firing, recovery | Ashe - W, Ezreal - Q, Lucian - Q, Darius - Q, Kennen - R |
|  | | | |
| Static fast ability | No | Firing, recovery | Garen - W, Katarina - R, Master Yi - W |
|  | | | |
| Dynamic slow ability | Yes | Windup, firing, recovery | Vi - Q, Viego - W, Fiddlestick - R, Caitlyn - E |
|  | | | |
| Dynamic fast ability | Yes | Firing, recovery | Kayn - Q, Vayne - Q, Riven - E |

This classification is based on two features.

The **first feature** is a deviation from the basic animation scheme. For simplicity, we consider only one possible deviation: the absence of a windup phase. The second possible deviation is the replacement of some phase with charging or channeling. This replacement is not significant for now.

Three types of abilities fit into the basic animation scheme:

1. Basic attack modifier
2. Static slow ability
3. Dynamic slow ability.

The champion performs all three phases of the animation for these abilities. We call them **slow** because their firing phase begins with a delay. This delay occurs due to preparations during the windup phase.

The remaining two types of abilities deviate from the basic scheme. They do not have the windup phase. Therefore, we call them **fast**. Their firing phase begins immediately after issuing the command.

The **second classification feature** is champion movement. If the firing phase of animation moves the champion, the ability is called **dynamic**. Otherwise, it is a **static** ability.

Note that the champion can move during the firing animation of some static abilities. Example: Darius Q. In this case, the movement happens because the player issues the move command. The firing animation of the ability does not cause it. If the player does not issue the move command, the champion performs the entire animation of the ability, staying in one place.

The following player's commands can change one of the ability animation phases:

1. Auto-attack
2. Using another ability
3. Moving
4. Using a summoner spell
5. Casting a dynamic ability towards the wall
6. Using an item's active effect.

Let us go through all ability types and consider which actions change their animations.

### 3.2.3 Auto-attack modifiers

>>>R1

The ability of the **auto-attack modifier** type empowers the next champion's basic attack. When a player issues the ability command, the champion performs a special windup animation. You cannot cancel this animation, and it allows the champion to perform some actions in parallel. Auto-attack modifier animation is the animation of an empowered auto-attack that applies the ability effect.

Most auto-attack modifier abilities have two properties:

1. [**Basic attack reset**](https://wiki.leagueoflegends.com/en-us/Basic_attack#Resets)

2. [**Uncancellable windup**](https://wiki.leagueoflegends.com/en-us/Basic_attack#Uncancellable_Windup).

The work with auto-attack modifier animation is based on these properties. The first one allows you to increase the DPS of the champion. The second one allows you to change the champion's position before the firing phase of the empowered auto attack.

So, here are the goals of working with the auto-attack modifier animation:

1. Increase the champion's damage per second (DPS)

2. Change the champion's position before the firing phase of the ability.

#### 3.2.3.1 Auto-attack reset

>>>R1

A combo that resets the auto-attack cooldown timer allows a champion to deal burst damage. This technique is useful during ganks, tower dives, lane trading, teamfight initiation, and flanking.

I> **Dive** is an attack on the enemy champion who is located in a dangerous area for the player. Examples of such areas are under an enemy tower or behind the enemy frontline.

The mechanics of resetting the auto-attack cooldown timer are as follows. When a player issues the ability command, the current AA timer is reset. This means the champion can perform his next attack. If the AA timer is not running when the ability is issued, the timer reset effect is ineffective. Therefore, you need to perform an AA and start the reset timer every time before issuing the ability.

Let us look at how to build a combo around resetting the auto-attack cooldown timer. For example, we take the **Vi AA-E combo**. Her E ability has both an attack reset and an uncancellable windup effect.

I> In all further examples, Vi has level is 1 and no attack speed items or runes.

Figure 3-9 shows the timeline diagram of Vi AA-E combo.

{caption: "Figure 3-9. The timeline diagram of Vi AA-E combo", width: "100%"}
![Vi AA-E combo](images/Micromanagement/vi-aa-e-combo.png)

The steps of this combo are as follows:

1. At point A, the player right-clicks the target. From this point on, the champion performs the windup animation phase: swinging her fist back to strike. This phase lasts 22.5% of the auto-attack 1.55 second cooldown. This is approximately 0.35 seconds, according to the following calculation:
{line-numbers: false, format: text}
```
windup = 1.55 * 22.5 / 100 ~ 0.35
```

2. At point B, the AA firing animation begins: the champion punches the target. It lasts approximately 0.25 seconds.

3. At point C, the player presses the E button and issues the next attack on the target. Then, the E ability cancels the AA recovery animation and resets the attack cooldown. The champion performs the next attack. Its windup phase lasts 0.35 seconds as usual.

4. At point D, the E firing animation begins. It lasts 0.25 seconds, the same as a regular auto-attack.

5. At point E, the champion begins her E recovery phase. It lasts 0.95 seconds, the same as a regular auto-attack.

You can cancel the E recovery animation on the E-G segment by the following actions:

1. Using another ability
2. Moving
3. Using a summoner spell
4. Using an active item effect.

The auto-attack cannot cancel the E recovery animation. Its cooldown timer begins at point C when the player issues the E ability. The AA cooldown is 1.55 seconds. The C-E segment is only 0.6 seconds. Therefore, the champion can only perform his next auto-attack at point G.

You can issue an attacking ability after a combo with an attack modifier. This way, the champion deals a maximum burst damage. After the attacking ability, you can issue another AA. Here are examples of burst combos that rely on the attack reset property:

1. **Jax A-W-Q-A**

2. **Fiora A-E-Q-A**

3. **Volibear A-Q-W-A**.

#### 3.2.3.2 Position change and auto-attack

>>>R1

The uncancellable windup property of the attack modifier ability allows the champion to change position before the firing phase. This technique is useful only for retreating. It allows you to break distance with opponents after diving, initiating a teamfight, or flanking.

Let us introduce names for combos with changing position. **Defensive combo** changes the champion's position for retreating. **Offensive combo** changes champion's position for attacking.

Changing the champion's position before the firing phase works not only with attack modifiers but also with the basic attack. We start with the second case with AA because it is simpler.

We will consider the **defensive combo Vi AA-F**. Figure 3-10 shows its timeline diagram.

{caption: "Figure 3-10. Timeline diagram of the defensive combo Vi AA-F", width: "100%"}
![Vi AA-F combo](images/Micromanagement/vi-aa-f-combo.png)

The steps of this combo are as follows:

1. At point A, the player right-clicks the target. The champion begins the AA windup animation. It lasts 0.35 seconds and ends at point C.

2. At point B, the player presses Flash immediately after the AA windup animation begins. The champion increases the distance to the target. At the new position, she completes the remaining windup animation. This is segment B-C in the diagram.

3. At point C, the AA firing animation begins. At this point, the target takes damage. The damage will occur even if the distance to the target is greater than Vi's attack range.

4. At point D, the champion begins the AA recovery phase. It can be canceled by movement, a summoner spell, an active item effect, or another champion's ability.

Players make two typical mistakes when performing this combo:

1. They start the combo when the target is out of the champion's attack range. Then, upon receiving the attack command, the champion will move toward the target. In this case, the player could press Flash before the AA windup animation begins. As a result, the champion will not perform an auto-attack.

2. They cancel the AA windup animation after the Flash. For example, a player can accidentally issue the move command. Then, the champion will interrupt the windup phase and not perform an auto-attack.

The uncancellable windup property of the attack modifier ability solves the second problem. It prevents the player from canceling the windup phase with a move command.

#### 3.2.3.3 Position change and auto-attack modifier

>>>R1

Now we will consider combos with Flash and the attack modifier ability. Our example is the **defensive combo Vi E-F**. Figure 3-11 shows its timeline diagram.

{caption: "Figure 3-11. Timeline diagram of the defensive combo Vi E-F", width: "100%"}
![Vi E-F combo](images/Micromanagement/vi-e-f-combo.png)

The steps of this combo are as follows:

1. At point A, the player presses the E button and right-clicks the target. The champion uses the ability and begins the E windup phase.

2. At point B, immediately after the E windup animation begins, the player presses Flash. The champion increases the distance to the target. At the new position, she completes the remaining E windup animation. This is segment B-C in the diagram.

3. At point C, the E firing animation begins. At this point, the target takes damage.

4. At point D, the champion begins the E recovery phase. It can be canceled by movement, a summoner spell, an active item effect, or another champion's ability.

A player could make only one mistake when executing this combo. He can start it when the target is out of the champion's attack range. In this case, the player could press Flash before the E windup animation begins.

There are several similar defensive combos with an attack modifier and Flash. Here are some examples:

* **Darius W-F** — it slows the enemy and increases the distance to him.

* **Garen Q-F** — it silences the enemy and increases the distance to him.

I> The **silence** effect prevents the enemy from using abilities, active item effects, and some summoner spells.

### 3.2.4 Static abilities

>>>R1

Now let us consider the **static abilities**. These are the most common types of abilities in the game. They could have various effects: extra damage, crowd control, healing, buff, and shield.

Most static abilities follow the basic animation scheme shown in Figure 3-8. Some static abilities deviate from it. The deviation could be one of the following or both:

1. Replacing one of the animation phases with charging or channeling

2. Omitting the windup phase.

Working with the animation of a static ability serves the following purposes:

1. To change the champion's position before the firing phase of an ability.

2. To mask the animation of one ability with the animation of another ability.

3. To cancel the recovery animation of an auto-attack or ability.

The first purpose is relevant only to slow, static abilities with a windup phase. Fast static abilities do not have it. Their animation begins with the firing phase.

#### 3.2.4.1 Position Change in attacking Darius combo

>>>R1

You can change the champion's position when using static abilities, both for attack and retreat. Offensive combos are effective in two cases:

1. The ability has a long windup phase.

2. The ability has a long range.

The idea behind an offensive combo is to perform the ability's windup phase in one location and shift its firing phase into another. This makes it harder for the enemy to dodge the ability.

There are two ways to change a champion's position during the windup phase of some static ability:

1. **Flash**. Examples of combos: Darius Q-F, Ezreal Q-F, Ezreal R-F.

2. **Dynamic champion ability**. Examples of combos: Caitlyn E-Q, Caitlyn E-W.

We will consider the changing champion's position using Flash. Let us take the **offensive combo Darius Q-F** as an example. The [following video](https://www.youtube.com/watch?v=bkvlyU1csIQ&t=124s) demonstrates it.

The main drawback of Darius Q ability is its long windup phase. The strike area is highlighted, giving opponents enough time to dodge it. If Darius uses the ability at a short distance, the opponent enters the internal area of the strike and takes less damage. The offensive Q-F combo solves this problem.

Figure 3-12 shows the timeline diagram of the Darius Q-F combo.

{caption: "Figure 3-12. The timeline diagram of Darius Q-F combo", width: "100%"}
![Darius Q-F combo](images/Micromanagement/darius-q-f-combo.png)

The steps of this combo are as follows:

1. At point A, the player presses the Q button. From this point on, the champion performs the Q windup animation phase: swinging the axe. This always lasts 0.75 seconds.

2. At point B, when the Q windup animation comes to an end, the player presses Flash. The champion should reach the position where the enemy is within the outer area of the strike. After this, the champion performs the remainder of the Q windup animation. This is segment B-C in the diagram.

3. At point C, the Q firing animation begins. At this point, all enemies within the strike area take damage. This phase lasts approximately 0.4 seconds.

4. At point D, the champion begins the Q recovery phase. It lasts approximately 0.33 seconds. It can be canceled by an attack, movement, a summoner spell, an active item effect, or another champion ability.

When a player executes the Darius Q-F combo, the opponent sees the animation of the ability in advance. However, he still has little time to react. If he flashes too early in the A-B segment, a Darius player will not flash. This will give him a resource advantage. The opponent can only dodge the Q strike if he flashes in the B-C segment. Therefore, the shorter this segment, the better the combo execution.

Here are the general rules for using Flash in all combos with changing the champion's position:

> In offensive combos, use Flash as late as possible. This will not give the opponent time to react.

> In defensive combos, use Flash as early as possible. This allows the champion to reach a safe distance sooner.

#### 3.2.4.2 Position Change in attacking Ezreal combo

>>>R1

The second example of position change using Flash is **offensive combo Ezreal Q-F**. It is also known as the "Ghost Q" combo. The [following video](https://www.youtube.com/shorts/QG7wX79RXAg) demonstrates it.

Ezreal's Q ability has a long range and a clearly visible windup animation. At high ranks, players watch the animation and dodge the projectile. The Q-F combo solves this problem. It increases the range of the ability and masks its animation. This makes it difficult for the opponent to predict the projectile trajectory.

I> **Animation masking** is the overlay of the animation of one action on top of another. The champion performs both actions, but the animation of the second one is distorted or hidden.

Figure 3-13 shows the timeline diagram for Ezreal Q-F combo.

{caption: "Figure 3-13. The timeline diagram of Ezreal Q-F combo", width: "100%"}
![Ezreal Q-F combo](images/Micromanagement/ezreal-q-f-combo.png)

The steps of this combo are as follows:

1. At point A, the player presses the Q button. The champion performs the Q windup animation phase: he extends his gauntlet forward. It always lasts 0.25 seconds.

2. At point B, the player presses Flash. The champion closes the distance with the target. Flash should be pressed so that its firing animation ends simultaneously with the Q windup animation at point C. This will not only increase the ability's range but also mask the windup animation on the B-C segment.

3. At point C, the champion performs the Q firing animation. This is masked similarly to the Q windup phase: the projectile animation begins at Ezreal's initial position. Its actual trajectory begins at the champion's new position. The firing phase lasts approximately 0.02 seconds.

4. At point D, the champion begins the Q recovery phase. This phase lasts approximately 0.9 seconds. It can be canceled by an attack, movement, a summoner spell, an active item effect, or another champion ability.

Figure 3-14 shows the projectile flight animation when the Ezreal Q-F combo is executed correctly.

{caption: "Figure 3-14. The projectile flight animation in Ezreal Q-F combo", width: "100%"}
![Projectile in Ezreal Q-F combo](images/Micromanagement/ezreal-q-animation-masking.png)

The projectile only travels halfway before hitting the target. This occurs because the projectile's animation differs from its actual trajectory.

During the Ezreal Q-F combo, the champion can flash away from the projectile's direction. The [following video](https://www.youtube.com/watch?v=Ze-nz6w21EE) demonstrates this variation of the combo. It allows you to hit a target while minions or another champion are covering it.

Many static slow abilities are combined with Flash in the same way as Ezreal's Q. For example, Ashe's W. If you press Flash during the Ashe W windup phase, the champion flashes and fires a volley of arrows from a new position. This combo increases the range of the ability.

#### 3.2.4.3 Position Change in defensive Ezreal combo

>>>R1

The third example of position change using Flash is **defensive combo Ezreal R-F**. The [following video](https://www.youtube.com/watch?v=huqdC11CJmU) demonstrates it.

Ezreal's R ability has two problems. **First**, the windup phase lasts one second. During this time, the champion is unable to move, making it an easy target in a teamfight. **Second**, the projectile's trajectory is predictable. The windup animation clearly indicates where the projectile will hit.

The R-F defensive combo solves both problems. Its idea is to mask the windup R animation with the Flash while simultaneously breaking distance from the opponent. This buys time and hides the projectile's direction.

Figure 3-15 shows the timeline diagram for Ezreal R-F combo.

{caption: "Figure 3-15. The timeline diagram of Ezreal R-F combo", width: "100%"}
![Ezreal R-F combo](images/Micromanagement/ezreal-r-f-combo.png)

The steps of this combo are as follows:

1. At point A, the player presses the R button. The champion performs the R windup animation phase: he flies up and extends his gauntlet forward. This always lasts 1 second.

2. At point B, the player presses Flash immediately after the R windup animation begins. The champion increases the distance to the target. At the new position, he completes the remaining windup animation. This is segment B-C in the diagram.

3. At point C, the champion performs the R firing phase animation. This lasts approximately 0.02 seconds.

4. At point D, the champion begins the R recovery phase. This lasts approximately 0.65 seconds. It can be canceled by an attack, movement, a summoner spell, an active item effect, or another champion ability.

When performing the R-F combo, it is important to press Flash as early as possible. Otherwise, the R windup animation will be incompletely masked. The champion will perform one part of the animation in the starting position and the other in the final position. This is bad because the opponent will see the projectile's direction.

Note that after the Flash, the champion will aim in the wrong direction. This distorts the animation. The projectile will still fly in the direction that the player intended when casting the R ability.

During a teamfight, it is better to Flash through a wall or into bushes. This puts the champion in a safe position and gives him time to complete the R windup animation.

I> There is a more complex E-R-F combo with Flash and Ezreal's ultimate ability. The [following video](https://www.youtube.com/watch?v=nxw-9TFjkF0) demonstrates it.

#### 3.2.4.4 Hiding animation in Jinx combo

>>>R1

Using Flash is not the only option to mask the ability animation. Some static abilities of a champion are also suitable for this purpose.

When you overlay animations of two static abilities, you get the following benefits:

1. Increase the champion's DPS in teamfight.

2. Hide the projectile's direction or strike.

Let us look at the **Jinx E-R combo**. The [following video](https://www.instagram.com/p/DAgwmuDMVq-) demonstrates it. First, we will consider animation of the E and R abilities.

The **Jinx R static slow ability** is very similar to Ezreal R. It has the same two drawbacks: a long windup phase and a predictable projectile trajectory. Figure 3-16 shows the timeline diagram of this ability.

{caption: "Figure 3-16. Timeline diagram of the Jinx R ability", width: "100%"}
![Jinx R ability](images/Micromanagement/jinx-r-ability-animation.png)

The R windup animation phase lasts 0.6 seconds, which is quite long.

The **Jinx E static fast ability** does not have a windup phase. When the player presses the E key, the champion immediately begins the firing animation phase: Jinx throws traps in front of her. Figure 3-17 shows the timeline diagram of this ability.

{caption: ""Figure 3-17. Timeline diagram of the Jinx E ability", width: "100%"}
![Jinx E ability](images/Micromanagement/jinx-e-ability-animation.png)

The **Jinx E-R combo** solves both problems of the R ability. The E ability animation hides the R windup phase. Because of this, the enemy does not see that the champion is immobilized and vulnerable. The projectile's direction is also hidden.

Figure 3-18 shows the timeline diagram of the Jinx E-R combo.

{caption: "Figure 3-18. Timeline diagram of the Jinx E-R combo", width: "100%"}
![Jinx E-R combo](images/Micromanagement/jinx-e-r-combo.png)

The steps of this combo are as follows:

1. At point A, the player presses the E button. The champion performs the E firing animation phase. It lasts 0.08 seconds.

2. At point B, the E recovery animation phase begins. The player presses the R button. The R windup phase then begins, but its animation is partially hidden.

3. At point C, the R firing animation phase begins. It lasts 0.07 seconds. It is also masked by the E recovery animation.

4. At point D, the R firing phase ends. Starting from this point, the champion performs only the remainder of the E recovery animation. It hides the R recovery phase.

5. At point E, the E recovery phase ends. The champion then plays the remainder of the R recovery animation.

You can cancel both E and R recovery animations at point D. This can be done by an attack, movement, a summoner spell, an active item effect, or another champion ability.

In our example, the recovery animation phase of one static ability masks the windup phase of another. The following combos work on the same manner:

* [**Riven R-W**](https://youtu.be/bXO-5CpNqJc?si=as1A5boOdGEIUlLg&t=240)

* [**Yasuo W-Q**](https://www.youtube.com/watch?v=iMgLMSFn2jQ&t=18s)

#### 3.2.4.5 Hiding animation in Darius combo

>>>R1

The second example of animation masking is **Darius W-Q combo**. The [following video](https://www.youtube.com/watch?v=83n-RIxQ25k&t=86s) demonstrates it

The idea behind the combo is to perform both the W and Q abilities simultaneously. The W attack modifier has an uncancellable windup property. This allows you to start the W windup phase and immediately begin the Q ability. Then the Q animation will overlay on the W animation.

Figure 3-19 shows the timeline diagram of the Darius W-Q combo.

{caption: "Figure 3-19. Timeline diagram of the Darius W-Q combo", width: "100%"}
![Darius W-Q combo](images/Micromanagement/darius-w-q-combo.png)

The steps of this combo are as follows:

1. At point A, the player presses W and issues an auto-attack. The champion begins the W windup animation phase, swinging the axe from below.

2. At point B, the player presses Q immediately after the W windup animation begins. The champion begins the Q windup animation, swinging the axe from above. This animation hides the W windup animation, which happens in parallel.

3. At point C, the W firing phase begins. The champion deals damage to the enemy with his attack modifier. The Q windup phase hides the strike animation.

4. At point D, the Q firing phase begins. All enemies within the strike area take damage.

5. At point E, the champion begins the Q recovery phase. This can be canceled by an attack, movement, a summoner spell, an active item effect, or another champion ability.

There are several similar combos with an attack modifier and a static ability. Here are some examples:

* **Dr. Mundo E-W**

* **Garen Q-E**

### 3.2.5 Dynamic abilities

>>>R1

Now we consider **dynamic abilities**. They can be offensive, which increases damage, or defensive, which provides some survivability. Both types of abilities move the champion in some way.

Working with the animation of a dynamic ability serves the following purposes:

1. Change the champion's position before or during the firing phase of an ability.

2. End the firing animation phase prematurely.

3. Mask the animation of one ability with the animation of another ability.

4. Cancel the recovery animation of an auto-attack or ability.

Let us look at an example combo for each of these purposes.

#### 3.2.5.1 Position Change in attacking Vi combo

>>>R1

The player can change the champion's position for attack and defense when using dynamic abilities. This technique works well for both slow and fast abilities.

When a champion performs a static ability, he can only change position during the windup animation phase. In contrast, most dynamic abilities allow changing position during the firing phase. Only Flash summoner spell allows you to do it.

Let us look at changing a champion's position using the **Vi Q-F combo** as an example. It has two variants: offensive and defensive. First, we will consider the animation of the Vi Q ability itself. Figure 3-20 shows its timeline diagram.

{caption: "Figure 3-20. The timeline diagram of Vi Q ability", width: "100%"}
![Vi Q ability](images/Micromanagement/vi-q-ability-animation.png)

In this ability, the windup phase is replaced with charging. It has four animation phases in total: windup (charging), charged, firing, and recovery. The second phase occurs when the champion fully charges the ability. You can skip it if you issue a firing before the ability is fully charged.

Vi Q ability does not have a lockout move property. [**Lockout**]((https://wiki.leagueoflegends.com/en-us/Terminology#Lockout)) prevents the champion from performing certain actions during the ability's windup phase. **Lockout move** prevents the champion from moving.

Now let us consider **offensive combo Vi Q-F**. Figure 3-21 shows its timeline diagram.

{caption: "Figure 3-21. The timeline diagram of offensive combo Vi Q-F", width: "100%"}
![Offensive combo Vi Q-F](images/Micromanagement/vi-q-f-attacking-combo.png)

I> We consider the execution of the combo when Vi Q ability is set to Normal Cast.

The steps of this combo are as follows:

1. At point A, the player presses the Q button. The champion begins the Q windup animation phase: charging her fist. This lasts a maximum of 1.25 seconds. The champion can move during this phase.

2. At point B, the champion completes the Q windup phase. After this, she is in a Q-charged state and retains her charge. This lasts up to 2.75 seconds. The champion can move during this phase.

3. At point C, the player presses the Q button. The champion performs the Q firing phase: a dash in the designated direction. At full charge and without impact, the Q firing phase lasts approximately 0.52 seconds.

4. At point D, which is near the end of the Q firing animation, the player presses Flash at the target's location. The champion will flash and end the Q firing animation at a new position. This is guaranteed to hit the target, dealing damage and knocking him back.

5. At point E, the firing phase ends. Immediately after, the champion will perform a basic attack on the target. This action can be canceled with a movement command.

The offensive combo with a dynamic ability and Flash serves the following purposes:

1. Increase the ability's range.

2. Prevent the enemy from reacting.

Here are some examples of attack combos that work similarly to Vi's Q-F:

* [**Yasuo E-Q-F**](https://www.youtube.com/shorts/2NIIS4VZtwY)

* [**Jarvan IV E-Q-F**](https://www.youtube.com/watch?v=5PWV5cW6IT0)

* [**Viego W-F**](https://www.youtube.com/shorts/GM3YOEU7hxM)

#### 3.2.5.2 Position Change in defensive Vi combo

>>>W

Теперь рассмотрим **защитное комбо Vi Q-F**. Его временную диаграмму демонстрирует иллюстрация 3-22.

{caption: "Иллюстрация 3-22. Временная диаграмма защитного комбо Vi Q-F", width: "100%"}
![Защитное комбо Vi Q-F](images/Micromanagement/vi-q-f-defensive-combo.png)

Шаги этого комбо следующие:

1. В точке A игрок нажимает кнопку Q. Чемпион начинает проигрывать фазу анимации Q windup.

2. В точке B сразу после начала анимации Q windup игрок нажимает flash. Так он может разорвать дистанцию с противником или уклониться от летящего снаряда.

3. В точке C чемпион заканчивает фазу Q windup. После этого он находится в состоянии Q charged и сохраняет заряд.

4. В точке D игрок нажимает кнопку Q. Чемпион выполняет фазу Q firing: рывок в указанном направлении. Это может быть отступление или контратака.

5. В точке E чемпион начинает фазу Q recovery. Её можно отменить атакой, передвижением, заклинанием призывателя, активным эффектом предмета или другим умением чемпиона.

Защитные комбо динамического умения и flash решают следующие задачи:

1. Позволяют уклониться от умений противника и контратаковать.

2. Разрывают дистанцию с противником и выигрывают время в сражении.

Вот примеры защитных комбо, которые работают аналогично Vi Q-F:

* [**Ezreal E-F**](https://mobalytics.gg/lol/champions/ezreal/combos)

* [**Caitlyn E-F**](https://mobalytics.gg/lol/champions/caitlyn/combos)

#### 3.2.5.3 Premature end of the firing phase

>>>W

Некоторые динамические умения дают дополнительный эффект после применения. В определённых ситуация он полезнее, чем смена позиции. Эффект можно получить быстрее, если сократить фазу firing умения.

Рассмотрим преждевременное завершение фазы firing на примере **динамического быстрого умения Vayne Q**. Его временную диаграмму демонстрирует иллюстрация 3-23.

{caption: "Иллюстрация 3-23. Временная диаграмма умения Vayne Q", width: "100%"}
![Умение Vayne Q](images/Micromanagement/vayne-q-ability-animation.png)

У умения Q нет фазы windup. Сразу после его применения чемпион начинает анимацию Q firing. Когда она закончится, чемпион получит три эффекта:

1. Следующая автоатака наносит дополнительный урон.

2. Следующая автоатака получает свойство uncancellable windup.

3. Сброс таймера автоатаки.

Всё это увеличивает DPS. Если в сражении не нужно менять позицию, эффекты будут важнее перемещения. Поэтому выгодно получить их как можно быстрее.

Обратите внимание, что фазу Q recovery нельзя отменить стандартными способами: атакой, передвижением, другим умением или активным эффектом предмета.

Чтобы **преждевременно завершить фазу Q firing**, надо направить кувырок в стену. Перед этим чемпион уже должен стоять вплотную к ней. Этот приём демонстрирует [следующее видео](https://www.youtube.com/watch?v=2A3EFucqXbY). Он в два раза сокращает задержку перед усиленной автоатакой.

Иллюстрация 3-24 демонстрирует временную диаграмму умения Vayne Q с сокращённой фазой firing.

{caption: "Иллюстрация 3-24. Временная диаграмма умения Vayne Q с сокращённой фазой firing", width: "100%"}
![Умение Vayne Q без firing](images/Micromanagement/vayne-q-no-firing.png)

Шаги этого приёма следующие:

1. В точке A игрок наводит курсор мыши в сторону стены и нажимает Q. Чемпион начинает проигрывать фазу анимации Q firing: делает кувырок.

2. В точке B чемпион прерывает фазу Q firing, потому что стена блокирует движение. Начинается фаза Q recovery: чемпион поднимается на ноги.

3. В точке C заканчивается фаза Q recovery. Теперь чемпион может выполнить усиленную автоатаку.

Вот примеры динамических умений, для которых можно сократить фазу firing:

* [**Kayn Q**](https://www.youtube.com/watch?v=4Num03szneM) — если сократить фазу firing, уменьшится задержка между первым и вторым ударами.

* **Fiora Q** — если сократить фазу firing, чемпион быстрее нанесёт удар по противнику.

* **Graves E** — если сократить фазу firing, чемпион быстрее получит дополнительный патрон для автоатаки.

* **Ekko E** — если сократить фазу firing, чемпион быстрее получит усиление следующей автоатаки.

#### 3.2.5.4 Hiding animation

>>>W

Мы уже познакомились с двумя способами маскировки анимации:

1. Комбинация двух статических умений
2. Статическое умение и flash.

Теперь рассмотрим третий способ маскировки анимации: комбинация статического и динамического умений. Цели такого приёма следующие:

1. Сменить позицию чемпиона для нападения или отступления.

2. Увеличить DPS чемпиона в сражении.

3. Скрыть направление снаряда или удар.

Рассмотрим **защитное комбо Caitlyn E-Q**. Его демонстрирует [следующее видео](https://www.youtube.com/shorts/Y5t984dWvDg). Сначала разберём умения, из которых оно состоит.

**Статическое медленное умение Caitlyn Q** похоже на Ezreal Q. Дальность Caitlyn Q немного больше, но его фаза windup почти в три раза длиннее. Из-за этого направление снаряда легко предсказать. Также во время подготовки чемпион становится уязвимым в командном сражении.

Иллюстрация 3-25 демонстрирует временную диаграмму умения Q Caitlyn.

{caption: "Иллюстрация 3-25. Временная диаграмма умения Caitlyn Q", width: "100%"}
![Умение Caitlyn Q](images/Micromanagement/caitlyn-q-ability-animation.png)

Фаза Q windup длится 0.63 секунды. За это время противнику легко уклониться от умения.

**Динамическое медленное умение E Caitlyn** имеет фазу windup. После неё чемпион выпускает снаряд и делает рывок назад. Временную диаграмму умения демонстрирует иллюстрация 3-26.

{caption: "Иллюстрация 3-26. Временная диаграмма умения Caitlyn E", width: "100%"}
![Умение Caitlyn E](images/Micromanagement/caitlyn-e-ability-animation.png)

**Защитное комбо Caitlyn E-Q** решает проблему умения Q. При его исполнении чемпион перемещается на фазе Q windup. Так он разрывает дистанцию с противником и скрывает направление снаряда Q.

Иллюстрация 3-27 демонстрирует временную диаграмму комбо Caitlyn E-Q.

{caption: "Иллюстрация 3-27. Временная диаграмма комбо Caitlyn E-Q", width: "100%"}
![Комбо Caitlyn E-Q](images/Micromanagement/caitlyn-e-q-combo.png)

Шаги этого комбо следующие:

1. В точке A игрок нажимает кнопку E. Чемпион начинает проигрывать фазу анимации E windup. Она длится 0.15 секунды.

2. В точке B начинается фаза анимации E firing. Она длится примерно 0.4 секунды.

3. В точке C сразу после начала анимации E firing игрок нажимает кнопку Q. Чемпион начнёт исполнять фазу Q windup. Её анимация наложится на анимацию E firing.

4. В точке D чемпион начнёт фазу Q firing. При правильном исполнении комбо снаряд вылетит из позиции, в которой находился чемпион в момент нажатия кнопки Q.

5. В точке E чемпион начнёт фазу Q recovery. Она длится примерно 1.28 секунды. Её можно отменить атакой, передвижением, заклинанием призывателя, активным эффектом предмета или другим умением чемпиона.

Вот примеры других комбо, которые работают аналогично Caitlyn E-Q:

* [**Caitlyn E-W**](https://youtu.be/bkvlyU1csIQ?si=tL3lcstUSnXZMAMw&t=284)

* [**Riven E-W-Q**](https://youtu.be/bkvlyU1csIQ?si=beyP_a-trYrgUie4&t=329)

* [**Riven E-R**](https://youtu.be/bXO-5CpNqJc?si=oyfbq0rMDX72bseR&t=225)

* **Yasuo E-Q**

* **Samira E-Q**

В последних двух комбо наложение умений приводит к проигрыванию специальной анимации. Несмотря на это, они исполняются точно так же как типичные комбо для маскировки анимации.

### 3.2.6 Complex combos

>>>W

Мы познакомились с базовыми приёмами для работы с анимацией умений. Для каждого из них мы рассмотрели пример простого комбо из двух действий. Комбо некоторых чемпионов намного сложнее. Они состоят из четырёх и более действий. Исполнить их невозможно, если не знать базовые приёмы.

Рассмотрим пример сложного комбо — **Samira fastest S combo**. За одну секунду оно наносит шесть ударов по противнику: два автоатакой и четыре умениями. Каждый удар отличается от предыдущего. После этого срабатывает пассивное умение, которое позволяет применить умение R.

[Следующее видео](https://www.youtube.com/watch?v=S2Uxl5v_f6Q) демонстрирует комбо Samira. Профессиональный игрок Jackspektra объясняет его по шагам в [этом видео](https://www.youtube.com/shorts/Ksvye6VP7-M?app=desktop).

Запишем последовательность команд, которую нужно дать для исполнения комбо. Она выгладит так:
{line-numbers: false, format: text}
```
AA-W-E-Q-AA-R
```

Эта последовательность выглядит просто. Но она не учитывает целый ряд действий с анимацией.

Просмотрите видео комбо в замедленном режиме. Вы заметите, что за каждым дефисом стоит один из приёмов работы с анимацией. Всего в комбо этих приёмов пять:

1. AA-W — умение W отменяет анимацию AA recovery.

2. W-E — умение E маскирует анимацию умения W.

3. E-Q — умение E маскирует анимацию умения Q.

4. Q-AA — AA отменяет анимацию Q recovery.

5. AA-R — умение R отменяет анимацию AA recovery.

Игрок должен понимать каждый из этих приёмов и уметь с ним работать. Только тогда он сможет эффективно исполнить комбо за минимальное время.

### 3.2.7 Training of combos

### 3.2.7.1 Search for information

>>>W

Лучший источник информации по комбо для конкретного чемпиона — видео гайды на Youtube. Вот пример хорошего [гайда для Darius](https://www.youtube.com/watch?v=83n-RIxQ25k).

Второй по качеству источник информации — это сайт [mobafire.com](https://www.mobafire.com). В некоторых гайдах по чемпионам авторы приводят основные комбо. Вот пример хорошего [гайда для Ezreal](https://www.mobafire.com/league-of-legends/build/the-complete-ezreal-guide-627978).

Также основные комбо для каждого чемпиона есть на сайте [mobalytics.gg](https://mobalytics.gg). Бесплатно можно посмотреть описания комбо. Чтобы проиграть видео с демонстрацией, нужна платная подписка. Вот пример [страницы с комбо для Ezreal](https://mobalytics.gg/lol/champions/ezreal/combos).

Если вы не нашли нужной информации, протестируйте потенциальные комбо в "Practice tool" самостоятельно. Для этого сделайте следующее:

1. Определите тип каждого умения чемпиона по таблице 3-1.

2. Для каждого умения составьте список комбо, которые должны работать для его типа.

3. Пройдите по списку и проверьте, работает ли каждое комбо на самом деле.

Обратите внимание, что в механике игры есть исключения из общих правил. Например, какое-то умение теоретически должно комбинироваться с flash. На практике может оказаться, что механика игры этого не позволяет.

Рассмотрим, как работает поиск комбо на примере. Допустим, что у чемпиона есть динамическое медленное умение. С таким типом обычно работают следующие приёмы:

1. Сменить позицию чемпиона до или во время фазы firing умения.

2. Преждевременно завершить фазу анимации firing.

3. Маскировать анимацию одного умения анимацией другого умения.

4. Отменить recovery анимацию автоатаки или умения.

Проверьте каждый вариант и составьте список сработавших приёмов. Подумайте, какие преимущества они дают в сражении. Попробуйте объединить найденные приёмы в более сложные комбинации, чтобы усилить эффект.

### 3.2.7.2 Player skills development

>>>W

Для хорошего исполнения комбо нужна регулярная тренировка. Типичная рейтинговая игра не даёт возможности для достаточной практики. Поэтому перед каждой игровой сессией запускайте "Practice tool" и отрабатывайте основные комбо своего чемпиона.

Интенсивность тренировок в "Practice tool" зависит от чемпиона. Если он механический, освоение его комбо займет намного больше времени. В некоторых случаях это могут быть недели и даже месяцы. Вы должны научиться исполнять основные комбо своего чемпиона на автомате.

I> [**Механический чемпион**](https://www.mobafire.com/league-of-legends/tier-list/champion-difficulty-tier-list-including-milio-4120) (mechanical champion) имеет самые высокие требования к навыкам микроменеджмента игрока. Комбо такого чемпиона сложны. Они требуют точных таймингов и правильного позиционирования. Примеры: Riven, Lee Sin, Yasuo, Azir, Nidalee.

Для качественного исполнения комбо недостаточно правильно прожимать кнопки. Если у вашего чемпиона есть дальнобойные умения, надо научиться ими попадать. Этот навык можно тренировать с помощью следующих инструментов:

1. Программа [Skill Gap](https://skillgap.pro/) с набором тренировочных режимов. Часть из них бесплатная, а часть платная.

2. Сайт [loldodgegame.com](https://loldodgegame.com/choose_game). Все режимы в нём бесплатные.

Обе программы имитируют упрощённую механику игры League of Legends.

Кроме этих инструментов могут быть полезны общие тренажёры на скорость и точность действий:

1. Игра [Don’t Tap](https://www.donttap.com/) на точность нажатий мыши.

2. [Тренажёр для APM](https://www.arealme.com/apm-actions-per-minute-test/ru/)

3. [Тренажёр на точность нажатий мыши](https://mouseaccuracy.com/).

I> **APM** (actions per minute) — это количество действий игрока в минуту.

Используйте эти инструменты, чтобы разогреться перед игровой сессией.

{pagebreak}
