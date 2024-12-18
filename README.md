The objective of this battle system is to take a classic, turn-based battle, and add a twist to it.

In most games, you kill things to get points, but in this one, killing is just *one* of the options. You can choose to befriend it, to leave it alone, to recruit it, to argue with it, to enslave it, or anything you can imagine. These depend on *actions*, which are the building blocks of this system.

This battle system aims to avoid random encounters and also avoid inducing “The Grind”, A.K.A making the player fight the same exact enemy multiple times in a row for no reason. It’s also heavily inspired by Undertale. :-)

---

To actually initiate a battle, you must first find an **entity**. An entity is anyone or anything you encounter within a battle. Some examples include a monster (most common), a person, even an inanimate object!

Battles will have only one entity. Multiple entities are outside the scope of this project, for now.

Some entities react differently to the player. The main four types of entities are:

| **TYPE** | **BEHAVIOUR** |
| --- | --- |
| Perma-passive | Attacks never |
| Passive | Attacks only if attacked |
| Hostile | Attacks only if encountered |
| Perma-hostile | Attacks always |

Perma-hostile is extremely rare to encounter, as the entity will hunt you forever and never stop.

---

An **action** is something the player performs during a battle.

Some actions are considered to be good, some are considered to be bad, but this value is not hardcoded into the game, as it’s up to the player to decide what’s “morally” correct.

Here’s a table that includes every action in the game, showing their name, their description, their energy consumption (whether it gains or loses energy), and finally, the item that the player needs to have to actually perform the action:

| **NAME** | **DESCRIPTION** | **ENERGY** | **ITEM** |
| --- | --- | --- | --- |
| Nothing | Do… nothing? |  |  |
| Flee | Run away from the battle. |  |  |
| Punch | Jab the entity right in the face. | -15 |  |
| Kick | Kick the entity on the abdomen. | -15 |  |
| Fart | Mmm…  c r e a m y  😛 | -5 |  |
| Superfart | Mmm…  d o u b l e   c r e a m y  😛 | -25 | Can o’ Beans |
| Sneeze | a-AA-AAA-CHOOOOÖÖÖÖŒEEEØØØØ | -5 |  |
| Backflip | Perform an epic, perfect backflip. | -25 |  |
| Shoot | Fire a gun to a random spot on the entities body. | -30 | Revolver |
| Trip | Drop the entity face flat onto the floor. | -20 |  |
| Scream | AAAAAHHHHHHH!!! | -15 |  |
| Stab | Pierce the entity’s chest with a knife. | -25 | Knife |
| Dance | Boogie like there’s no tomorrow.  | -25 |  |
| Hug | Give the entity a tight, heartwarming hug. | -10 |  |
| Kiss | Smooch the entity on the cheek. | -10 |  |
| Compliment | Say something nice to the entity. | -5 |  |
| Insult | Say something mean to the entity. | -5 |  |
| Suicide | Slit your throat with a knife. | -50 | Knife |
| Psuedocide | Slit your throat with a… toy knife? | -40 | Toy Knife |
| Relax | Lay down and take a break. | +15 |  |
| Sleep | Zzzzzzz… Huh? | +20 |  |
| Meditate | Inhale, flow in… Exhale, flow out… | +30 |  |
| Twerk | I thought this game was PG? | -15 |  |

Each action isn’t guaranteed to be available for the player to use. For instance, if the player is in a jungle, then they’re unable to use the “Backflip” action because of the choked environment. Similarly, if the player is in hell, they can’t use the “Relax” action because of the blazing heat.

But, most actions will be available at all times, especially the primitive ones, such as “Punch”, “Kick”, “Compliment”, “Insult”, “Scream”, and more.

---

In the context of actions, **energy** is the amount of work the player can do.

Every single action consumes a certain amount of energy from the player, and the player starts out with a 100 points of energy at the start of every battle. The only way to regain energy is to use an energy-regaining item, such as food or potions, or use an energy-regaining action, such as the “Meditate” or “Relax” actions. Obviously, if the player doesn’t have enough energy, they cannot perform a specific action.

Well, what if the player reaches 0 energy? Will the battle end? Of course not! The player will have to use an item or action to get back their lost energy. What if the player doesn't have any items or actions available? If that happens, then the player has nothing to do but flee the battle. What if the flee fails? At that point, the player will automatically lose.

Contrary to what you might’ve assumed, energy doesn’t reset every battle. The player constantly regenerates 1 energy point every minute while not in battle, and 2.5 energy points per minute when in battle. When the player gets attacked by the entity in battle, they immediately lose energy, but the amount they lose depends on how strong the attack was.

---

The **commentator** is a person who visits in the form of a textbox who narrates the battle.

Depending on the things the player or entity performs, the commentator will say different things to make the battle more interesting and provide subtle hints to the player.

Some example scenarios include:

1. *player punches*
2. “what a punch! the enemy looks… unfazed!”
3. *entity farts*
4. “… EEEEW! nasty!”
5. *player dances*
6. “am i supposed to clap, or…?”
7. *player wins*
8. “i was kind of rooting for that goblin though…”

The commentator is always in lowercase because he hates his job a lot and he's depressed.

---

An **item** is an object that the player can use to gain a special effect or fulfill a requirement.

They’re mainly used in battles to fulfill an action’s requirement. For example, a “Stab” action requires a “Knife” item. If the player doesn’t have the item, then they cannot perform the action.

Items can be found anywhere, primarily on the ground in a random area in the game, but they can also be obtained via traders/shops for a set amount of a form of currency.

Here’s a table showing all the different items that exist in the game:

| **NAME** | **DESCRIPTION** |
| --- | --- |
| Water Bottle | A plastic bottle containing H2O. |
| Knife | A small, but sharp blade. |
| Toy Knife | A small blade. Not sharp at all. |
| Revolver | A six-shooter handgun. |
| Can o’ Beans | A fart-inducing snack. |

---

The main in-game currency are **doodles** (singular: doodle) and can be used to purchase items, bribe entities, gamble, and much more.

Doodles’ symbol is portrayed in the game as a randomly-generated scribble, hence their name.

---

Items are stored in the player’s **inventory**. The inventory is a 3x3 grid that can be filled with items, but each grid can only hold one unit of an item, even if the item is of the same type.

The player can use items from their inventory by accessing it at any time when wandering (not in battle) and can be accessed while in a battle via an action.

---

The entity can retaliate towards the player via a bullet hell mechanic similar to Undertale’s.

An arena with platforms pops up, and a stickman spawns in. This stickman has the ability to walk, run, and jump onto the platforms. Shortly after, the enemy begins its attack and releases a multitude of projectiles, minions, threats, or anything, really. It depends on the entity.

It’s the players job to dodge these attacks. The sequence shouldn’t take too long. After that, the player returns to the main interface to start another round.

The player can get hit by one of the projectiles and immediately die. There is no health stat for the player, it’s only one hit and death. If the player dies, then the battle ends.

---

In conclusion, the main game loop looks something like this:

1. Battle begins
2. Player chooses an action
3. Action executes
4. Entity reacts
5. Arena sequence begins
6. Player dodges attacks
7. Arena sequence ends
8. Repeat from step 2 until either side wins
9. Battle ends

---
