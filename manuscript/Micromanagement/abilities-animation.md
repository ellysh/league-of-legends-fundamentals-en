## 3.2 Ability animation

The basic attack pattern is consistent across all champions and consists of three phases. However, the proportions of these phases can vary. For instance, Volibear's windup phase accounts for 30% of his attack animation, while Ashe's windup phase is only 21.93%. Additionally, the base attack speed and its growth per level differ among champions, but these are minor details. The algorithms for executing the attack moves and attack ability techniques are the same for all champions.

In contrast, working with ability animations is more complex. Abilities are executed using different algorithms and interact in unique ways with the champion's other actions. This complexity demands advanced micromanagement skills from the player. Let us explore some of the basic techniques involved.

### 3.2.1 Phases of ability animation

When a player issues an ability command, the champion executes a complete animation cycle. This cycle includes three phases, similar to an auto-attack for most abilities:

1. **Windup** — preparation for the action.

2. **Firing** — execution of the strike, shot, or application of an effect.

3. **Recovery** — returning to the starting position.

Abilities that follow this sequence can be referred to as adhering to a **basic scheme**. Some abilities deviate from this structure. We will consider these variations as deviations from the basic scheme.

Let us start with simple abilities that fit within the basic scheme, such as the Ashe W ability. Figure 3-8 illustrates its timeline diagram.

{caption: "Figure 3-8. The timeline diagram for the Ashe W ability", width: "100%"}
![Ashe W ability](images/Micromanagement/ashe-w-ability-animation.png)

Now, let us examine the diagram step by step:

1. At point A, the player issues the ability command. The champion begins the windup animation phase: drawing the bowstring. This phase always lasts 0.25 seconds for the W ability.

2. At point B, the champion begins the firing phase: launching a volley of arrows. This phase lasts approximately 0.1 seconds.

3. At point C, the champion begins the recovery phase: drawing the next arrow from the quiver. This phase lasts approximately 1.65 seconds.

4. At point D, the champion completes the full animation cycle. A total of two seconds have passed since the player issued the command at point A.

It is important to note that the duration of all phases of the W ability animation is constant. It does not vary based on attack speed, champion level, or ability level. However, some other abilities may have their animation durations affected by these factors.

We have discussed the basic scheme of an ability animation. There are three primary deviations from it:

1. **Charging** replaces the windup phase.
  
2. **Channeling** replaces the firing phase.

3. There is no windup phase, and the ability animation starts directly with firing.

When charging replaces the windup or channeling replaces the firing phase, the intention of the corresponding phase remains unchanged. However, the duration of this phase becomes longer. The rules for replacements are as follows:

* If a charging replaces a windup, the champion prepares to cast the ability during this phase. After this, he performs the firing animation.

* If a channeling replaces a firing animation, this phase begins after windup. During the channeling, the champion deals damage or applies the ability effect.

You can cancel or change the animation of any of the ability phases: windup, firing, or recovery. There are no general rules for this. It depends on the specific ability and the champion.

### 3.2.2 Ability classification

Let us focus only on the abilities animation. Their effects are not so important at the moment. We can categorize all abilities into five types. Each type has its own specific animation pattern.

If two abilities follow the same animation pattern, you can apply the same techniques to both. Therefore, classification is crucial. By using this system, you do not need to remember the rules for every ability in the game. Instead, it suffices to understand how animation works for each ability type.

Table 3-1 lists all ability types classified by their animation patterns.

{caption: "Таблица 3-1. Classification of champion abilities by animation pattern", width: "100%"}
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

This classification is based on two key features.

The **first feature** is the deviation from the basic animation scheme. For simplicity, we consider only one possible deviation: the absence of a windup phase. Another possible deviation is replacing some animation phase with charging or channeling. We can ignore this deviation for now.

Three types of abilities in Table 3-1 follow the basic animation scheme:

1. Basic attack modifier
2. Static slow ability
3. Dynamic slow ability.

For these abilities, the champion performs all three phases of the animation. We call them **slow** because their firing phase begins with a delay. This delay occurs due to preparations during the windup phase.

The remaining two types of abilities deviate from the basic scheme. They do not have the windup phase. Therefore, we call them **fast**. Their firing phase begins immediately after using the ability.

The **second classification feature** is the champion movement. If the firing phase of the ability animation results in moving the champion, the ability is categorized as **dynamic**. If the champion stays at the same position, the ability is classified as **static**.

It is important to note that a champion can move during the firing animation phase of some static abilities. A good example is the Darius Q ability. In this case, the movement occurs because the player issues a move command. If the player does not issue the move command, the champion performs the entire animation of the ability, staying in one place.

The following player commands can change the phases of an ability’s animation:

1. Auto-attack
2. Using another ability
3. Moving
4. Casting a summoner spell
5. Using a dynamic ability towards the wall
6. Activating an item’s effect.

Let us examine each ability type and consider which actions may change their animations.

### 3.2.3 Auto-attack modifiers

The ability of the **auto-attack modifier** type empowers a champion's next basic attack. When a player uses this ability, the champion performs a special windup animation that cannot be canceled. During this animation, the champion can carry out extra actions. Auto-attack modifier animation is the animation of an empowered auto-attack that applies the ability effect.

Most auto-attack modifier abilities have two key properties:

1. [**Basic attack reset**](https://wiki.leagueoflegends.com/en-us/Basic_attack#Resets)

2. [**Uncancellable windup**](https://wiki.leagueoflegends.com/en-us/Basic_attack#Uncancellable_Windup).

When you work with auto-attack modifier animation, you rely on these properties. The first property allows you to increase the DPS of the champion. The second property allows you to change the champion's position before the firing phase of the empowered auto-attack.

Here are the goals when working with the auto-attack modifier animation:

1. Increase the champion's damage per second (DPS)

2. Change the champion's position before the firing phase of the ability.

#### 3.2.3.1 Auto-attack reset

A combo that resets the auto-attack cooldown timer allows a champion to deal burst damage. This technique is useful in various scenarios, including ganks, tower dives, lane trading, teamfight initiation, and flanking.

I> **Dive** is an attack on the enemy champion located in a dangerous area for the player. Examples of such areas are under an enemy tower or behind the enemy frontline.

The mechanics of resetting the auto-attack cooldown timer work as follows. When a player issues an ability command, the current AA timer is reset. This reset means the champion can perform his next attack. If the AA timer is not running when the ability is issued, the timer reset has no effect. Therefore, you need to perform an AA and start the reset timer every time before issuing the ability.

Let us look at how to build a combo around resetting the auto-attack cooldown timer. We take the **Vi AA-E combo** as an example. Vi E ability has both an attack reset and an uncancellable windup effect.

I> In all further examples, Vi is at level 1 and has no attack speed items or runes.

Figure 3-9 shows the timeline diagram of the Vi AA-E combo.

{caption: "Figure 3-9. The timeline diagram of the Vi AA-E combo", width: "100%"}
![Vi AA-E combo](images/Micromanagement/vi-aa-e-combo.png)

The steps to execute this combo are as follows:

1. At point A, the player right-clicks the target. From this moment, the champion begins the windup animation phase: swinging her fist back to strike. This phase lasts 22.5% of the auto-attack cooldown, which equals 1.55 seconds. This duration is approximately 0.35 seconds, according to the following calculation:
{line-numbers: false, format: text}
```
windup = 1.55 * 22.5 / 100 ~ 0.35
```

2. At point B, the AA firing animation phase begins: the champion punches the target. This phase lasts approximately 0.25 seconds.

3. At point C, the player presses the E button and issues the next attack on the target. The E ability cancels the AA recovery animation and resets the attack cooldown, which allows the champion to perform the next attack. Its windup phase lasts 0.35 seconds as usual.

4. At point D, the E firing animation begins. It lasts 0.25 seconds, the same duration as a regular auto-attack.

5. At point E, the champion begins the E recovery phase. It lasts 0.95 seconds, similar to a regular auto-attack.

You can cancel the E recovery animation during the E-G segment by the following actions:

1. Using another ability
2. Moving
3. Using a summoner spell
4. Activating an item effect.

The auto-attack cannot cancel the E recovery animation. The cooldown timer for the auto-attack begins at point C when the player issues the E ability. The AA cooldown is 1.55 seconds. The C-E segment is only 0.6 seconds. Therefore, the champion can only perform his next auto-attack at point G.

You can issue an attacking ability after a combo with an attack modifier. This way, the champion deals a maximum burst damage. After the attacking ability, you can issue another AA. Here are examples of burst combos that rely on the attack reset property:

1. **Jax A-W-Q-A**

2. **Fiora A-E-Q-A**

3. **Volibear A-Q-W-A**.

#### 3.2.3.2 Position change and auto-attack

The uncancellable windup property of the attack modifier ability allows a champion to change position before the firing phase. This technique is useful for retreating. It allows you to increase the distance from opponents after diving, initiating a teamfight, or flanking.

We can categorize position-changing combos into two types:

1. **Defensive combos**, which reposition the champion for retreating

2. **Offensive combos**, which reposition the champion for attacking.

Changing a champion's position before the firing phase applies not only to attack modifiers but also to basic attack. We will begin with the AA case because it is simpler.

Let us consider the **defensive combo Vi AA-F**. Figure 3-10 shows its timeline diagram.

{caption: "Figure 3-10. Timeline diagram of the defensive combo Vi AA-F", width: "100%"}
![Vi AA-F combo](images/Micromanagement/vi-aa-f-combo.png)

The steps to execute this combo are as follows:

1. At point A, the player right-clicks the target. The champion begins the AA windup animation phase. This phase lasts 0.35 seconds and ends at point C.

2. At point B, the player presses Flash immediately after the AA windup animation begins. The champion moves away from the target. At the new position, she completes the remaining windup animation. This movement matches segment B-C in the diagram.

3. At point C, the AA firing animation begins. At this point, the target takes damage. The damage occurs even if the distance to the target exceeds Vi's attack range.

4. At point D, the champion begins the AA recovery phase. It can be canceled by movement, a summoner spell, an active item effect, or another champion's ability.

Players make two common mistakes when executing this combo:

1. A player begins the combo when the target is outside the champion's attack range. As a result, when he issues the attack command, the champion moves toward the target. In this case, the player could press Flash before the AA windup animation begins by mistake. Then, the champion skips an auto-attack and just performs Flash.

2. A player cancels the AA windup animation after using Flash. For example, a player may accidentally issue the move command. Then, the champion stops the AA windup phase and skips an auto-attack.

The uncancellable windup property of the attack modifier ability solves the second problem. It prevents the player from canceling the windup phase with a move command.

#### 3.2.3.3 Position change and auto-attack modifier

Now we will consider combos that involve Flash and the attack modifier ability. Our example is the **defensive combo Vi E-F**. Figure 3-11 shows its timeline diagram.

{caption: "Figure 3-11. Timeline diagram of the defensive combo Vi E-F", width: "100%"}
![Vi E-F combo](images/Micromanagement/vi-e-f-combo.png)

The steps to execute this combo are as follows:

1. At point A, the player presses the E button and right-clicks the target. The champion uses the ability and begins the E windup animation.

2. At point B, immediately after the E windup animation begins, the player presses Flash. The champion increases the distance to the target. At the new position, she completes the remaining E windup animation. This corresponds to segment B-C in the diagram.

3. At point C, the E firing animation begins. At this moment, the target takes damage.

4. At point D, the champion begins the E recovery phase. This phase can be canceled by movement, a summoner spell, an active item effect, or another champion's ability.

A player could make only one mistake when executing this combo. He can start it when the target is outside of the champion's attack range. In this case, the player could press Flash before the E windup animation begins.

Several similar defensive combos involve an attack modifier ability and Flash. Here are a few examples:

* **Darius W-F** — it slows the enemy and increases the distance from him.

* **Garen Q-F** — it silences the enemy and increases the distance from him.

I> The **silence** effect prevents the enemy from using abilities, active item effects, and certain summoner spells.

### 3.2.4 Static abilities

Now let us consider the **static abilities**. Most abilities in the game are of this type. They can have various effects: dealing extra damage, crowd control, healing, buffs, and shields.

Most static abilities adhere to the basic animation scheme shown in Figure 3-8. However, some static abilities may deviate from this scheme in the following ways:

1. Replacing one of the animation phases with charging or channeling

2. Omitting the windup phase entirely.

You can achieve the following purposes when working with the animations of a static ability:

1. Changing the champion's position before the firing phase of an ability.

2. Masking the animation of one ability with the animation of another.

3. Canceling the recovery animation of an auto-attack or ability.

The first purpose applies only to slow, static abilities with a windup phase. The animation of fast static abilities begins with the firing phase, without windup.

#### 3.2.4.1 Position Change in attacking Darius combo

You can change the champion's position while using static abilities, whether for attacking or retreating. Offensive combos are effective in two cases:

1. When the ability has a long windup phase.

2. When the ability has a long range.

The concept behind an offensive combo is to perform the ability's windup phase in one location and then shift its firing phase to another. This technique makes it more difficult for the enemy to dodge the ability.

There are two ways to change a champion's position during the windup animation phase of a certain static ability:

1. **Flash**. Examples of combos: Darius Q-F, Ezreal Q-F, Ezreal R-F.

2. **Dynamic champion ability**. Examples of combos: Caitlyn E-Q, Caitlyn E-W.

Now, we will focus on changing the champion's position using Flash. Let us examine the **offensive combo Darius Q-F**. The [following video](https://www.youtube.com/watch?v=bkvlyU1csIQ&t=124s) demonstrates this combo.

The main drawback of Darius Q ability is its long windup animation phase. The strike area is highlighted, giving opponents ample time to dodge it. If Darius uses the ability from a short distance, the enemy can move into the inner area of the strike, resulting in less damage taken. The offensive Q-F combo solves this issue.

Figure 3-12 shows the timeline diagram of the Darius Q-F combo.

{caption: "Figure 3-12. The timeline diagram of the Darius Q-F combo", width: "100%"}
![Darius Q-F combo](images/Micromanagement/darius-q-f-combo.png)

The steps to execute this combo are as follows:

1. At point A, the player presses the Q button. From this moment, the champion begins the Q windup animation phase: swinging the axe. This phase lasts 0.75 seconds.

2. At point B, when the Q windup animation concludes, the player presses Flash. The champion should reposition to where the enemy is within the outer area of the strike. After this movement, the champion completes the remainder of the Q windup animation. The segment B-C in the diagram represents this phase.

3. At point C, the Q firing animation begins. At this point, all enemies within the strike area take damage. This phase lasts approximately 0.4 seconds.

4. At point D, the champion begins the Q recovery phase. It lasts approximately 0.33 seconds. This phase can be canceled by an attack, movement, a summoner spell, an active item effect, or another champion ability.

When executed properly, the Darius Q-F combo allows an opponent to see the ability's animation in advance. However, the enemy has little time to react. If he flashes too early during the A-B segment, the Darius player will not follow up with a Flash. This trade gives the player a resource advantage. The opponent can only dodge the Q strike by using Flash in the B-C segment. Therefore, the shorter this segment is, the better the combo execution.

Here are the general rules for using Flash in combos that involve changing a champion's position:

> In offensive combos, use Flash as late as possible. This minimizes the time the opponent has to react.

> In defensive combos, use Flash as early as possible. This allows the champion to reach a safe distance more quickly.

#### 3.2.4.2 Position Change in attacking Ezreal combo

The second example of a position change using Flash is the **offensive combo Ezreal Q-F**. It is also known as the "Ghost Q" combo. The [following video](https://www.youtube.com/shorts/QG7wX79RXAg) demonstrates it.

Ezreal's Q ability has a long range and a clearly visible windup animation. At high Elo ranks, players often watch this animation and dodge the projectile. The Q-F combo solves this issue by increasing the ability's range while masking its animation. This masking makes it harder for opponents to predict the projectile's trajectory.

I> **Animation masking** is the technique of overlaying the animation of one action over another. The champion performs both actions, but the second action's animation is distorted or concealed.

Figure 3-13 shows the timeline diagram for the Ezreal Q-F combo.

{caption: "Figure 3-13. The timeline diagram of the Ezreal Q-F combo", width: "100%"}
![Ezreal Q-F combo](images/Micromanagement/ezreal-q-f-combo.png)

The steps to execute this combo are as follows:

1. At point A, the player presses the Q button. The champion performs the Q windup animation phase: he extends his gauntlet forward. This phase always lasts 0.25 seconds.

2. At point B, the player presses Flash. The champion closes the distance to the target. Flash should be activated so that its firing animation ends simultaneously with the Q windup phase at point C. This timing not only extends the ability's range but also masks the windup animation during the B-C segment.

3. At point C, the champion performs the Q firing animation phase. This phase is masked similarly to the Q windup phase: the projectile animation begins from Ezreal's initial position. However, its actual trajectory starts from the champion's new location. The firing phase lasts approximately 0.02 seconds.

4. At point D, the champion begins the Q recovery phase. This phase lasts approximately 0.9 seconds. It can be canceled by an attack, movement, a summoner spell, an active item effect, or another champion ability.

Figure 3-14 shows the projectile flight animation when the Ezreal Q-F combo is executed correctly.

{caption: "Figure 3-14. The projectile flight animation in the Ezreal Q-F combo", width: "100%"}
![Projectile in Ezreal Q-F combo](images/Micromanagement/ezreal-q-animation-masking.png)

You can see that the projectile only travels halfway before striking the target. This effect occurs because the projectile's animation differs from its actual trajectory.

During the Ezreal Q-F combo, the champion can flash away from the direction of the projectile. The [following video](https://www.youtube.com/watch?v=Ze-nz6w21EE) demonstrates this variation of the combo. It allows you to hit a target that might be obscured by minions or another champion.

Many static slow abilities are combined with Flash in a manner similar to the Ezreal Q ability. For example, the Ashe W ability can be executed this way. If you press Flash during the Ashe W windup phase, the champion flashes and fires a volley of arrows from a new position. This combo increases the range of the ability.

#### 3.2.4.3 Position Change in defensive Ezreal combo

The third example of position change using Flash is the **defensive combo Ezreal R-F**. The [following video](https://www.youtube.com/watch?v=huqdC11CJmU) demonstrates this combo.

Ezreal's R ability has two problems. **First**, the windup phase lasts one second. During this time, the champion cannot move, making him an easy target in a teamfight. **Second**, the trajectory of the projectile is predictable. The windup animation clearly shows where the projectile will go.

The R-F defensive combo solves both problems. The idea of the combo is to mask the R windup animation with Flash while simultaneously increasing the distance from the opponent. This move provides extra time and hides the projectile's intended direction.

Figure 3-15 shows the timeline diagram for the Ezreal R-F combo.

{caption: "Figure 3-15. The timeline diagram of the Ezreal R-F combo", width: "100%"}
![Ezreal R-F combo](images/Micromanagement/ezreal-r-f-combo.png)

The steps to execute this combo are as follows:

1. At point A, the player presses the R button. The champion begins the R windup animation phase: he flies up and extends his gauntlet forward. This phase always lasts 1 second.

2. At point B, the player presses Flash immediately after the R windup animation begins. The champion increases the distance from the target. At the new position, he continues the remaining windup animation. The segment B-C in the diagram represents this phase.

3. At point C, the champion performs the R firing animation. This phase lasts approximately 0.02 seconds.

4. At point D, the champion begins the R recovery phase. This phase lasts approximately 0.65 seconds. It can be canceled by an attack, movement, a summoner spell, an active item effect, or another champion ability.

When performing the R-F combo, it is crucial to press Flash as early as possible. Otherwise, the R windup animation will be partially masked. The champion will perform part of the animation in the starting position and the other part in the final position. This mistake can reveal the projectile's direction to the opponent.

Note that after using Flash, the champion will aim in the wrong direction. This feature distorts the animation. However, the projectile will still travel in the direction that the player has pointed when casting the R ability.

During a teamfight, it is better to Flash through a wall or into bushes. This move places the champion in a safer position and provides time to complete the R windup animation.

I> There is a more complex E-R-F combo with Flash and Ezreal's ultimate ability R. The [following video](https://www.youtube.com/watch?v=nxw-9TFjkF0) demonstrates this advanced technique.

#### 3.2.4.4 Hiding animation in Jinx combo

Using Flash is not the only way to mask ability animations. Some static abilities of a champion can also serve this purpose.

When overlaying animations of two static abilities, you gain the following benefits:

1. Increased damage per second (DPS) in teamfights.

2. Hide a strike or projectile direction.

Let us look at the **Jinx E-R combo**. The [following video](https://www.instagram.com/p/DAgwmuDMVq-) demonstrates it. First, we will consider animation of the E and R abilities.

The **Jinx R static slow ability** is quite similar to Ezreal R. It has the same two drawbacks: a long windup phase and a predictable projectile trajectory. Figure 3-16 shows the timeline diagram of this ability.

{caption: "Figure 3-16. Timeline diagram of the Jinx R ability", width: "100%"}
![Jinx R ability](images/Micromanagement/jinx-r-ability-animation.png)

The R windup animation phase lasts 0.6 seconds, which is relatively long.

The **Jinx E static fast ability** does not have a windup phase. When the player presses the E button, the champion immediately begins the firing animation phase: Jinx throws traps in front of her. Figure 3-17 shows the timeline diagram of this ability.

{caption: ""Figure 3-17. Timeline diagram of the Jinx E ability", width: "100%"}
![Jinx E ability](images/Micromanagement/jinx-e-ability-animation.png)

The **Jinx E-R combo** solves both problems of the R ability. The E ability animation hides the R windup phase. Because of this, the enemy does not realize that the champion is immobilized and vulnerable. The projectile direction is also hidden.

Figure 3-18 shows the timeline diagram of the Jinx E-R combo.

{caption: "Figure 3-18. Timeline diagram of the Jinx E-R combo", width: "100%"}
![Jinx E-R combo](images/Micromanagement/jinx-e-r-combo.png)

The steps for executing this combo are as follows:

1. At point A, the player presses the E button. The champion begins the E firing animation phase. It lasts 0.08 seconds.

2. At point B, the E recovery animation phase starts. The player presses the R button. The R windup phase then begins, but its animation is partially hidden.

3. At point C, the R firing animation phase begins. It lasts 0.07 seconds. It is also masked by the E recovery animation.

4. At point D, the R firing phase ends. Starting from this point, the champion continues only the remainder of the E recovery animation. It hides the R recovery phase.

5. At point E, the E recovery phase ends. Then the champion completes the remaining R recovery animation.

You can cancel both E and R recovery animations at point D. This can be done by an attack, movement, a summoner spell, an active item effect, or another champion ability.

In this example, the recovery animation of one static ability masks the windup phase of another. The following combos function in the same manner:

* [**Riven R-W**](https://youtu.be/bXO-5CpNqJc?si=as1A5boOdGEIUlLg&t=240)

* [**Yasuo W-Q**](https://www.youtube.com/watch?v=iMgLMSFn2jQ&t=18s)

#### 3.2.4.5 Hiding animation in Darius combo

The second example of animation masking is the **Darius W-Q combo**. The [following video](https://www.youtube.com/watch?v=83n-RIxQ25k&t=86s) demonstrates it

The idea behind the combo is to use the W and Q abilities simultaneously. The W attack modifier has the uncancellable windup property. This technique allows you to start the W windup phase and immediately use the Q ability. This results in the Q animation overlaying the W animation.

Figure 3-19 shows the timeline diagram of the Darius W-Q combo.

{caption: "Figure 3-19. Timeline diagram of the Darius W-Q combo", width: "100%"}
![Darius W-Q combo](images/Micromanagement/darius-w-q-combo.png)

The steps of this combo are as follows:

1. At point A, the player presses W and issues an auto-attack. The champion begins the W windup animation phase, swinging the axe from below.

2. At point B, the player presses Q immediately after the W windup animation starts. The champion begins the Q windup animation, swinging the axe from above. This Q animation hides the W windup animation, which continues in parallel.

3. At point C, the W firing phase begins. The champion deals damage to the enemy with the attack modifier. The Q windup phase hides the strike animation.

4. At point D, the Q firing phase begins. All enemies within the strike area take damage.

5. At point E, the champion begins the Q recovery phase. This phase can be canceled by an attack, movement, a summoner spell, an active item effect, or another champion ability.

There are several similar combos with an attack modifier and a static ability. Here are a few examples:

* **Dr. Mundo E-W**

* **Garen Q-E**

### 3.2.5 Dynamic abilities

Now, let us explore **dynamic abilities**. These abilities can be categorized as offensive, which increase damage, or defensive, which enhance survivability. Both types of abilities change the champion's position in some way.

Working with the animation of a dynamic ability serves several purposes:

1. Change the champion's position before or during the firing phase of an ability.

2. End the firing animation phase prematurely.

3. Mask the animation of one ability with the animation of another ability.

4. Cancel the recovery animation of an auto-attack or ability.

We will look at an example combo for each of these purposes.

#### 3.2.5.1 Position Change in attacking Vi combo

The player can change the champion's position for attack and defense when using dynamic abilities. This technique works well for both slow and fast abilities.

When a champion performs a static ability, he can change position during the windup and recovery phases. In contrast, most dynamic abilities allow changing position during the firing phase. Flash summoner spell is the only option to do it.

Let us examine changing a champion's position using the **Vi Q-F combo** as an example. This combo has two variants: offensive and defensive. First, we will consider the animation of the Vi Q ability. Figure 3-20 shows its timeline diagram.

{caption: "Figure 3-20. The timeline diagram of the Vi Q ability", width: "100%"}
![Vi Q ability](images/Micromanagement/vi-q-ability-animation.png)

In this ability, the windup phase is replaced with charging. There are four animation phases in total: windup (charging), charged, firing, and recovery. The charged phase occurs when the ability is fully charged. You can skip it by issuing a firing command before full charge is reached.

The Vi Q ability does not have a lockout move property. [**Lockout**]((https://wiki.leagueoflegends.com/en-us/Terminology#Lockout)) prevents the champion from performing certain actions during the ability's windup phase. **Lockout move** prevents the champion from moving.

Now let us consider the **offensive combo Vi Q-F**. Figure 3-21 shows its timeline diagram.

{caption: "Figure 3-21. The timeline diagram of the offensive combo Vi Q-F", width: "100%"}
![Offensive combo Vi Q-F](images/Micromanagement/vi-q-f-attacking-combo.png)

I> We consider how to execute this combo when the Vi Q ability is set to Normal Cast.

The steps of this combo are as follows:

1. At point A, the player presses the Q button. The champion begins the Q windup animation phase: charging her fist. This phase lasts a maximum of 1.25 seconds, during which the champion can move.

2. At point B, the champion completes the Q windup phase and enters a Q-charged state. This state lasts up to 2.75 seconds. The champion can move during this time.

3. At point C, the player presses the Q button again. The champion performs the Q firing phase: a dash in the specified direction. When fully charged and without any impact, this phase lasts approximately 0.52 seconds.

4. At point D, which is near the end of the Q firing animation, the player presses Flash toward the target's location. This action causes the champion to flash and concludes the Q firing animation at a new position. Using flash guarantees to hit the target, dealing damage, and knocking him back.

5. At point E, the firing phase ends. Immediately after that, the champion performs a basic attack on the target. This action can be canceled with a movement command.

The offensive combo with a dynamic ability and Flash serves the following purposes:

1. Increase the ability's range.

2. Prevent the enemy from reacting.

I> There is a more complex version of the Vi Q-F combo. It allows you to push the enemy in the opposite direction of the Q ability. The [following video](https://www.instagram.com/p/DWwRzZRFR_g/) demonstrates it.

Here are some examples of attack combos that function similarly to the Vi Q-F combo:

* [**Yasuo E-Q-F**](https://www.youtube.com/shorts/2NIIS4VZtwY)

* [**Jarvan IV E-Q-F**](https://www.youtube.com/watch?v=5PWV5cW6IT0)

* [**Viego W-F**](https://www.youtube.com/shorts/GM3YOEU7hxM)

#### 3.2.5.2 Position Change in defensive Vi combo

Now let us consider the **defensive combo Vi Q-F**. Figure 3-22 shows its timeline diagram.

{caption: "Figure 3-22. The timeline diagram of the defensive combo Vi Q-F", width: "100%"}
![Defensive combo Vi Q-F](images/Micromanagement/vi-q-f-defensive-combo.png)

The steps of this combo are as follows:

1. At point A, the player presses the Q button. The champion begins the Q windup animation phase.

2. At point B, the player presses Flash immediately after the Q windup animation begins. This technique allows the champion to increase the distance from the opponent or dodge the incoming projectile.

3. At point C, the champion completes the Q windup phase. Then, she enters the Q-charged state.

4. At point D, the player presses the Q button again. The champion executes the Q firing phase: dashing in the specified direction. This move can be a retreat or a counterattack.

5. At point E, the champion begins the Q recovery phase. This phase can be canceled by an attack, movement, a summoner spell, an active item effect, or another champion ability.

The defensive combo with a dynamic ability and Flash serves the following purposes:

1. Dodge enemy abilities and execute a counterattack.

2. Create distance between the champion and the enemy.

Here are some examples of defensive combos that function similarly to Vi Q-F:

* [**Ezreal E-F**](https://mobalytics.gg/lol/champions/ezreal/combos)

* [**Caitlyn E-F**](https://mobalytics.gg/lol/champions/caitlyn/combos)

#### 3.2.5.3 Premature end of the firing phase

Some dynamic abilities provide an additional effect after being cast. In certain situations, this effect can be more useful than repositioning the champion. You can activate the effect more quickly by shortening the firing animation of the ability.

Let us consider the premature end of the firing phase using the **Vayne Q dynamic fast ability** as an example. Figure 3-23 shows its timeline diagram.

{caption: "Figure 3-23. The timeline diagram of the Vayne Q ability", width: "100%"}
![Vayne Q ability](images/Micromanagement/vayne-q-ability-animation.png)

The Q ability has no windup phase. Immediately after casting it, the champion begins the Q firing animation. When this animation ends, the champion gains three effects:

1. The next basic attack deals bonus damage.

2. The next basic attack gains an uncancellable windup.

3. The basic attack timer is reset.

These buffs increase the champion's DPS. If repositioning is not necessary during a fight, obtaining the buffs quickly becomes more important than movement. Therefore, it is beneficial to activate them as soon as possible.

Note that you cannot cancel the Q recovery phase in usual ways: attacking, moving, using another ability, or using an active item effect.

You need to aim the Q ability at a wall to **prematurely end its firing phase**. The champion should already stand close to the wall before doing this. The [following video](https://www.youtube.com/watch?v=2A3EFucqXbY) demonstrates this technique. It halves the delay before the empowered basic attack.

Figure 3-24 shows the timing diagram for the Vayne Q ability with a shortened firing phase.

{caption: "Figure 3-24. The timeline diagram of the Vayne Q ability with a shortened firing phase", width: "100%"}
![Vayne Q ability without firing](images/Micromanagement/vayne-q-no-firing.png)

The steps of this technique are as follows:

1. At point A, the player moves the mouse cursor over a wall and presses Q. The champion begins the Q firing animation phase: she tumbles.

2. At point B, the champion interrupts the Q firing phase because the wall blocks her movement. The Q recovery phase begins: the champion rises to her feet.

3. At point C, the Q recovery phase ends, allowing the champion to perform a charged basic attack.

Here are some examples of dynamic abilities where you can reduce the firing animation phase:

* [**Kayn Q**](https://www.youtube.com/watch?v=4Num03szneM) — reducing the firing phase decreases the delay between the first and second strikes.

* **Fiora Q** — reducing the firing phase allows the champion to strike the enemy faster.

* **Graves E** — reducing the firing phase allows the champion to gain an additional ammo for his basic attack faster.

* **Ekko E** — reducing the firing phase allows the champion to empower his next basic attack faster.

#### 3.2.5.4 Hiding animation

>>>R1

We have already covered two methods of animation masking:

1. Combining two static abilities
2. Combining a static ability and Flash.

Now, let us consider a third method of animation masking: combining a static and a dynamic ability. The goals of this technique are as follows:

1. Reposition the champion for attack or retreat.

2. Increase the champion's DPS in the fight.

3. Hide the projectile's direction or strike.

We will consider **defensive combo Caitlyn E-Q**. The [following video](https://www.youtube.com/shorts/Y5t984dWvDg) demonstrates this technique. First, we will look at the abilities it consists of.

Caitlyn's **static slow ability Q** is similar to Ezreal's Q. Caitlyn's Q has a slightly longer range, but its windup phase is almost three times longer. This makes the projectile's direction easy to predict. During the windup phase, the champion also becomes vulnerable in a teamfight.

Figure 3-25 shows the timeline diagram of Caitlyn's Q ability.

{caption: "Figure 3-25. The timeline diagram of the Caitlyn Q ability", width: "100%"}
![Caitlyn Q ability](images/Micromanagement/caitlyn-q-ability-animation.png)

The Q windup animation phase lasts 0.63 seconds. During this time, the enemy can easily dodge the ability.

Caitlyn's **dynamic slow E ability** has a windup animation phase. When this phase finishes, the champion fires a projectile and dashes back. Figure 3-26 shows the timeline diagram of the ability.

{caption: "Figure 3-26. The timeline diagram of the Caitlyn E ability", width: "100%"}
![Caitlyn E ability](images/Micromanagement/caitlyn-e-ability-animation.png)

**Defensive combo Caitlyn E-Q** solves the problem of the long windup phase of the Q ability. When performing the combo, the champion moves during this phase. This creates distance between her and the enemy. Also, the movement hides the direction of the Q projectile.

Figure 3-27 shows the timeline diagram of the Caitlyn E-Q combo.

{caption: "Figure 3-27. The timeline diagram of the Caitlyn E-Q combo", width: "100%"}
![Caitlyn E-Q combo](images/Micromanagement/caitlyn-e-q-combo.png)

The steps of this combo are as follows:

1. At point A, the player presses the E button. The champion begins the E windup animation phase. It lasts 0.15 seconds.

2. At point B, the E firing animation phase begins. It lasts approximately 0.4 seconds.

3. At point C, the player presses the Q button immediately after the E firing animation begins. The champion begins the Q windup phase. Its animation overlaps with the E firing animation.

4. At point D, the champion begins the Q firing phase. If the combo is executed correctly, the projectile launches from the starting champion's position at point C.

5. At point E, the champion begins the Q recovery phase. This phase lasts approximately 1.28 seconds. It can be canceled by an attack, movement, a summoner spell, an active item effect, or another champion ability.

Here are several examples of other combos that work similarly to Caitlyn E-Q:

* [**Caitlyn E-W**](https://youtu.be/bkvlyU1csIQ?si=tL3lcstUSnXZMAMw&t=284)

* [**Riven E-W-Q**](https://youtu.be/bkvlyU1csIQ?si=beyP_a-trYrgUie4&t=329)

* [**Riven E-R**](https://youtu.be/bXO-5CpNqJc?si=oyfbq0rMDX72bseR&t=225)

* **Yasuo E-Q**

* **Samira E-Q**

In the last two combos, combining two abilities triggers a special animation. Despite this, they are executed the same as typical animation masking combos.

### 3.2.6 Complex combos

>>>R1

We have covered the basic techniques for working with ability animations. For each of them, we looked at an example of a simple combo with two actions. Combos of some champions are much more complex, consisting of four or more actions. You cannot perform them properly without knowing the basic techniques.

Let us look at an example of a complex combo: **Samira fastest S combo**. It deals six hits to the enemy in one second: two basic attacks and four from abilities. Each hit is different from the previous one. They fully stack the passive ability that allows Samira to use her R ability.

The [following video](https://www.youtube.com/watch?v=S2Uxl5v_f6Q) demonstrates the Samira fastest S combo. The esports player Jackspektra explains the combo step by step in the [following video](https://www.youtube.com/shorts/Ksvye6VP7-M?app=desktop).

The sequence of commands, which you need to perform the combo, looks like this:
{line-numbers: false, format: text}
```
AA-W-E-Q-AA-R
```

This sequence looks simple. But it does not take into account a whole series of actions with the abilities animation.

Take a break and watch the video with the combo demonstration in slow motion. You will notice that each hyphen in the sequence corresponds to one of the animation techniques. There are five of these techniques in the combo:

1. AA-W — the W ability cancels the AA recovery animation.

2. W-E — the E ability masks the W ability animation.

3. E-Q — the E ability masks the Q ability animation.

4. Q-AA — AA cancels the Q recovery animation.

5. AA-R — the R ability cancels the AA recovery animation.

The player must understand each of these techniques and be able to apply them. Only then could he execute the combo effectively in the shortest possible time.

### 3.2.7 Training of combos

### 3.2.7.1 Search for information

>>>R1

The best source of information on combos for a specific champion is YouTube video guides. Here is an example of a good [guide for Darius](https://www.youtube.com/watch?v=83n-RIxQ25k).

The second best source of information is [mobafire.com](https://www.mobafire.com). Some champion guides provide the most commonly used combos. Here is an example of a good [guide for Ezreal](https://www.mobafire.com/league-of-legends/build/the-complete-ezreal-guide-627978).

Basic combos for each champion are also available on [mobalytics.gg](https://mobalytics.gg). You can view combo descriptions for free. But you need a paid subscription to watch the videos. Here is an example [combo page for Ezreal](https://mobalytics.gg/lol/champions/ezreal/combos).

If you have not found the required information, you can check possible combos in the "Practice Tool". Here are the steps to do this:

1. Determine the type of your champion's abilities using Table 3-1.

2. For each ability, create a list of combos that should work for its type.

3. Go through the list and check whether each combo actually works.

Note that game mechanics have exceptions to the general rules. For example, some abilities should, in theory, combine with Flash. In practice, the game mechanics may not allow this.

We can consider how searching combos could work with an example. Let us assume our champion has a dynamic slow ability. The following techniques typically work with this type of ability:

1. Changing the champion's position before or during the firing phase of the ability.

2. Ending the firing animation phase prematurely.

3. Masking the animation of one ability with the animation of another ability.

4. Canceling the recovery animation of an auto-attack or ability.

Try each option and make a list of the techniques that worked. Estimate the advantages that each combo could provide you in a fight. Try combining the techniques you find into more complex combos to enhance their effect.

### 3.2.7.2 Player skills development

>>>R1

Performing combos well requires regular practice. A typical ranked game does not provide sufficient opportunity for such practice. Therefore, it could help a lot to launch the "Practice Tool" and repeat your champion's basic combos before each game session.

The intensity of practicing combos varies by champion. If this is a mechanical champion, mastering his combos will take much longer. In some cases, it can take weeks or even months. You must learn to execute your champion's basic combos on autopilot.

I> [**Mechanical champion**](https://www.mobafire.com/league-of-legends/tier-list/champion-difficulty-tier-list-including-milio-4120) has the highest requirements for players' micromanagement skills. Combos of such champions are complex, requiring precise timing and proper positioning. Examples: Riven, Lee Sin, Yasuo, Azir, Nidalee.

To execute combos well, it is not enough to press the buttons correctly. If your champion has long-range abilities, you need to land them. You can train this skill using the following tools:

1. The [Skill Gap](https://skillgap.pro/) program with a variety of training modes. Some are free, while others are paid.

2. The [loldodgegame.com](https://loldodgegame.com/choose_game) website. All modes are free.

Both programs simulate simplified League of Legends game mechanics.

In addition to these tools, general speed and accuracy trainers may be useful:

1. The [Don't Tap](https://www.donttap.com/) game for mouse click accuracy.

2. [APM Trainer](https://www.arealme.com/apm-actions-per-minute-test/ru/)

3. [Mouse Accuracy Trainer](https://mouseaccuracy.com/).

I> **APM** (actions per minute) is the number of actions a player takes per minute.

Use these tools to warm up before your gaming sessions.

{pagebreak}
