# FTLEventTags

When is a Crew Kill no better than a Ship Kill? Which Blue Option gives the best reward? What are the chances of losing crew to Giant Alien Spiders?

This mod tags approximately 1000 lines of in-game text to show the possible outcomes of various choices and events. No information is displayed that can't otherwise be found in the game files, or from Googling dialogue. It doesn't effect the gameplay mechanics themselves in any way.

Tags include: 
* Choice outcomes, including Blue Options
* Rewards from ship/crew kills
* Surrender/escape triggers and timers
* Enemy ship classes
* Weapon effect (breach/stun/fire) chances (added to weapon descriptions)
* Beacon count (Stores/Empty/Nebula etc) per sector type (added to the first beacon of each sector)

This mod is useful for players wanting to learn the possible results of ingame events. It is also useful for players wanting to play optimally without having to refer to the wiki or XML diving.

## Notes
 * To avoid giving players an unfair advantage, some dialogue remains untagged or tagged ambiguously. For example the outcomes of the real/decoy Rebel ship fights in the Engi Homeworlds quest, or the 'moon counting' event.
 * I'm unsure what the 'chance', 'min', 'max', and 'timer' values actually mean for surrenders and escapes, but have tagged them anyway 'as is' from the XMLs.
 * Works with FTL v1.6. For FTL v1.5.13, use [this](https://github.com/thrnz/FTLEventTags).
 * Languages other than English aren't supported
 * Consistent with FTL v1.6.8

## To-do
 * ~~Re-do screenshots.~~

## Legend
* SF: Ship Fight
* DR: Default Rewards: K: MStd, CK: [ x3 MStd | 2x HStd | 2x HScrapFuel | Crew+ LScrap | LScrapWeapon ] 
* DLR: Default Lanius Rewards K: [ 3x MStd | HStd ], CK: [ 3x MStd | 2x HStd | HScrapFuel | Crew+ LScrap | LScrapDrone ]
* K: Kill reward
* CK: Crew Kill reward
* DB: Double reward
* S: Surrender (Chance, Min-Max, Offer)
* Esc: Escape (Chance, Min-Max, Timer)
* BO: Blue Option
* Crew-/+: Gain/lose crew
* CB+/-: Whether clone bay revives(+) or not (-) lost crew
* Fleet+/-: Fleet advance/delay
* x2, x3: Number of times an identical event is in the event pool
* Nil: Nothing happens
* More...: More options follow. Used to avoid excessively long tags. Should always be safe to click. The worst that can happen will be a ship fight.
* Rbl: Rebel class ship
* Prt: Pirate class ship
* Fed: Federation class ship
* Auto - Auto assault or scout class ship
* Eng - Engi class ship
* Mts - Mantis class ship
* Ztn - Zoltan class ship
* Slg - Slug class ship
* Rck - Rock class ship
* Lns - Lanius class ship
* Cry - Crystal class ship
* PZtn, PRck - Pirate class Zoltan/Rock ship etc.
 

## Rewards
* L/M/H/R Prefix: Low/Medium/High/Random
* Std: Standard Rewards (Scrap + 2 random resources + small chance of augment/weapon/drone)
* Stuff: Less scrap, but more resources.
* ScrapFuel: Scrap + Fuel
* ScrapMiss: Scrap + Missiles
* ScrapDrones: Scrap + Drones
* ScrapDrone: Scrap + Drone schematic
* ScrapWeapon: Scrap + Weapon
* ScrapAugment: Scrap + Augment
* Fuel: Fuel only
* Miss: Missiles only
* Drones: Drones only
* Drone: Drone schematic only
* Weapon: Weapon only
* Augment: Augment only

## Example tags:

* [ Prt SF DR | Nil | Weapon ] 

One of 3 possible outcomes: either a ship fight against a pirate class ship with default rewards, nothing, or a free random weapon.

* [ x2 Nil | Crew+ | Crew- (CB+) ]

One of 4 possible outcomes: Two chances at having nothing happen, one chance of gaining a random crew member, and one chance of losing a crew member that can be negated by a clonebay.

* [ Rbl SF K: MStd; S: 0.2, 3-4, RStuff; Esc: 0.4, 3-4; CK: HStd ]

A ship fight against a Rebel class ship. Killing the ship gives medium scrap + 2 resources. Getting a crew kill gives high scrap + 2 resources. The ship has a chance of trying to escape/surrendering.

* [ Fleet-- ]

The fleet is delayed by 2 jumps

## Screenshots:

https://imgur.com/a/9kywd
