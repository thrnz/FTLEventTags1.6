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
 * Consistent with FTL v1.6.9

## To-do
 * ~~Re-do screenshots.~~
 * Double check quest reference

## Legend
* SF: Ship Fight
* DR: Default Rewards: K: MStd, CK: [ x3 MStd | 2x HStd | 2x HScrapFuel | Crew+ LScrap | LScrapWeapon ] 
* DLR: Default Lanius Rewards K: [ 3x MStd | HStd ], CK: [ 3x MStd | 2x HStd | HScrapFuel | Crew+ LScrap | LScrapDrone ]
* K: Kill reward
* CK: Crew Kill reward
* DB: Double reward. You will get this reward regardless of how the ship is defeated
* S: Surrender (Chance, Min-Max, Offer)
* Esc: Escape (Chance, Min-Max, Timer)
* BO: Blue Option
* Or: You will be offered a choice between outcomes
* |: 'or', the game will choose one of these outcomes
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

* [ Prt SF K: MStd; CK: HStd; DB: [ Crew+ | MStd | LStd | LWeap | +5 Hull | Nil ] ]
A ship fight against a Pirate class ship. Killing the ship gives medium scrap + 2 resources. Getting a crew kill gives high scrap + 2 resources. On defeating the ship (either via ship kill or crew kill), you will then get one of six outcomes: new crew member, medium scrap + 2 resources, low scrap + 2 resources, low scrap + weapon, 5 point hull repair, or nothing.

* [ Fleet-- ]

The fleet is delayed by 2 jumps

## Quests
To save space, Quests are generally tagged by name and not outcome. For reference, here is a list of all Quest beacon outcomes:
* Abadoth
  * [ Fleet+, MStd or Ztn SF DR ] or Slug BO: [ MStd or Ztn SF DR ]
* Construction
  * [ Rbl SF Enemy ASB; K: MStd; CK: HStd, DB: MScrap ] or Nil
  * [ Nil | x2 LScrap | [ LScrap | CloneBay BO [ x2 Crew+ | 1 Boarder ] ] | 2 Boarders, Prt SF DR | 2-4 Boarders, Enemy ASB ] or Nil
  * [ MScrap, -4 Fuel ] or -1 Fuel or Nil
* Crew Kill
  * Prt SF K: -15 Hull; CK: HScrapWeapon
* Crystal Unlock
  * MFuel, +10 Hull, Crystal Vengeance Augment
* Defector
  * HStuff
  * LScrap
* Engi Unlock (Decoy)
  * Rbl SF K: MStd; CK: MStd (Decoy); Esc: 18-18, 40s; S: 4-4, Nothing ] (Note, the decoy has a ',' in the text. The real one does not)
* Engi Unlock (Real)
  * Rbl SF K: MStd; CK: HStd; Esc: 18-18, 40s; S: 4-4, Engi Unlock Quest
* Engi Unlock
  * Mts w/Human crew SF K: Nil; CK: MStd; DB: +20 Hull, HStd, Titanium System Casing
* Escort
  * Rbl SF DR
  * HStd
  * +5 Hull, Store
  * Reactor+1
* Federation Base Assist
  * x2 Auto SF, K: LStd, DB: [ Crew+, +7 Hull, HStd | LScrapWeapon, Crew+ ]
  * Friendly ASB, Rbl Elite SF, K: LStd, CK: MStd, DB: [ Crew+, MScrap ]
  * Friendly ASB, Auto SF, K: LStd, DB: [ Crew+, +7 Hull, HStd ]
* Hidden Federation Base
  * HScrapDrone
  * LStd, Crew+
  * MStd, +35 Hull
  * Nil or Lvl2 Scanner [ MStd ] or Lvl3 Scanner [ MScrapWeapon ] or LRS [ MScrapWeapon ]
  * Same as Federation Base Assist Quest
* Mantis Chase
  * Mts SF K: MStd Weapon; CK: HStd Weapon; S: 2-2, HScrapWeap; Esc: 6-6, 12s, HStd
* Mantis Thief Stash
  * HScrapWeapon
* Mantis War Camp Quest
  * [ Nil | Mts SF K: MStd, CK: HStd ] or [ Missile Weapon BO: -1 Miss, Mts SF K: MStd, CK: HStd ] or [2 Fire Bomb BO: -2 Miss, HStuff, EngiCrew+ ]
* Merchant Delivery
  * -5 Drones for 20-30 Scrap or [ -5 Drones for 40-55 Scrap or Nil ] or MindControl BO: -5 Drones for 40-55 Scrap or Lvl6 Weapons BO: -5 Drones for 55-75 Scrap 2-3 Fuel
  * [ MDrones | Crew+, 3-4 Human Boarders | Crew- (CB-), avoid w/Lvl 2+ Medbay ] or AP Drone BO: [ x2 -1 Drone | -1 Drone, MStd ]
* Merchant Investigate
  * MStd, [ MScrapDrone Quest or [ Weapon | HStd | MScrapDrone Quest ] ]
  * Crew+ MScrapDrone Quest or [ Weapon | HStd | MScrapDrone Quest ] or Teleport BO: [ Weapon | HStd | MScrapDrone Quest ]
  * Prt SF K: MStd; CK: MStd
* Merchant Investigate Deliver
  * MScrapDrone
* Primitives
  * [ Ztn SF; K: LStd, Fleet+; CK: RStd, Fleet+ ] or [ Rbl SF K: LScrapWeapon, CK: MScrapWeapon ] or [ Nil ]
* Rock Homeworlds
  * Rck SF w/Solar-flare K: MStd, CK: HStd, Esc: 28-28, 32s, Quest [ Rock Plating , +29 Hull ]
* Rock Marriage
  * [ Random Augment, LScrap ] or [ +1 Rock Crew, Rck SF K: MStd, CK: HStd ]
* Slug Pirate Trap
  * [ Prt SF K: MStd; CK: HStd; S:HScrap ] or [ Prt SF K: LStd; CK: MStd ]
* Slug Unlock
  * [ Slg SF K: HStd; CK: HStd ] or [ SlugCrew/Lvl2 Sensor BO: Slg SF K: HStd, Slug Gel; CK: HStd, Slug Gel; Esc: 22-22, 35s ]
* Space Dock Rescue
  * Rbl SF K: MScrap; CK: MScrap; DB: [ +5 Hull, Store ]

## Screenshots:

https://imgur.com/a/9kywd
