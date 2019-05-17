## Codefest Gameplay

This page defines general gameplay rules for the Codefest game. Certain minor points are omitted.

The game is turn-based. On each turn each character will be asked to make a move. There are three types of moves: `ATTACK, SKILL, BLOCK`. ATTACK beats SKILL, SKILL beats BLOCK, BLOCK beats ATTACK. Each team will build a simple AI for their character based on some information from the opponent and existing moves. Once both characters make their moves, the winning character will deal damage to the losing character in that turn. The damage is calculated based on the winning character attributes. If both characters pick the same move, the turn ends with no damage to either characters. Once one character's hp drops below 0, the game ends.


### Attributes

Each character has 150 hp and the following starting attributes:

```
private int strength = 1;
private int vitality = 1;
private int intellect = 1;
private int luck = 5;
```

Each character is given 35 points to invest in any of the 4 attributes. Strength greatly increases ATTACK damage, vitality greatly increases BLOCK damage and intellect greatly increases SKILL damage. Luck slightly increases damage with all moves. The attributes can be reset and reallocated at any time.


### Critical

Each character is given 2 critical points to use during battle. The decision to make the move as "critical" is completed before the next turn using `setNextMoveAsCritical()`. If the character wins that turn, then a critical modifier will be applied to any damage dealt by the character. The critical point is lost at the end of the turn regardless of turn outcome. Characters with high level of luck may get a single critical point refunded regardless of turn outcome.


### Invulnerability

Each character is given 1 point of invulnerability to use during battle. The decision to become invulnerable is completed before the next turn using `setNextMoveInvulnerable()`. If the character loses that turn, then no damage will be dealt to the character. The invulnerability point is lost at the end of the turn regardless of turn outcome.


### Elements

Each character has 1 element on their weapon and 1 element on their armour.
For example, attacking an EARTH armour with a FIRE weapon will deal increased damage.
The damage modifier table is given below. The row is read first (weapon), then the column (armour). So, NEUTRAL against NEUTRAL is 1x, NEUTRAL against other elements is 0.75x, FIRE against NEUTRAL is 1.25x, FIRE against FIRE is 0.25x, etc.

```
    def NEUTRAL,FIRE,WATER,AIR,EARTH
atk
NEUTRAL(1.00, 0.75, 0.75, 0.75, 0.75),
FIRE   (1.25, 0.25, 0.50, 0.65, 2.00),
WATER  (1.25, 2.00, 0.25, 0.50, 0.65),
AIR    (1.25, 0.65, 2.00, 0.25, 0.50),
EARTH  (1.25, 0.50, 0.65, 2.00, 0.25);
```

Characters may change their weapon / armour elements at any point during the game.