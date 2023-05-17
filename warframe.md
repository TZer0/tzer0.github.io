# Useful Warframe Knowledge

This document contains useful knowledge for playing Warframe.

## Useful Websites/Links
[Warframe.market](https://warframe.market/) - Trading

[Ducanator](https://warframe.market/tools/ducats) - Helps you figure out what to trade away for ducats

[Riven average price list](https://semlar.com/rivenprices)

[Official drop tables for the entire game](https://www.warframe.com/droptables)

[Overframe.gg](https://overframe.gg/) - helps you theorycraft builds

[Warframe Hub](https://hub.warframestat.us/#/) - cycle timers, fissures, invasions and more

## General tips

### Starting out

If you're a new player (or about to start playing), I have the following recommendations:
* Don't pick Volt as your starting frame.
* Join a clan (gets you access to Volt).
* The moment you hit mastery rank 4, get the Hek blueprint from the market and build it. It'll carry you well.
* Buy every MK1 from the market in turn, level them to 30 and throw them in the bin.
* Check what weapons are required as ingredients for other weapons before you throw away any of them [here](https://warframe.fandom.com/wiki/Weapons_Required_as_Crafting_Ingredients).
* Get a Kuva Nukor when you can (you won't regret it).
* Don't spend plat on something you could earn by just playing the game.
* Don't sell non-prime frames if you get the prime variant. Get the helminth segment instead and subsume the frame.
* Get a Railjack (start by purchasing the railjack cephalon from the in-game marketplace after The Second Dream). Railjack is great for earning credits, cracking relics while getting new ones, mastery, and getting unique weapons.

### Progressing through the game
There are a few things to do to progress:
* Gain mastery ranks
* Check the requirement of junctions, those will guide you through the game.
* Check the codex station for quests

### Late-game tips

* Perspicacity from helminth at rank 3 is useful for sorties. Allows you to hack panels without doing the minigame (because ciphers do not work).
* Golden Instinct from helminth at rank 15 is useful for general content. Helps find you ayatan sculptures and rare crates.
* Get galvanized mods from arbitration and arcanes from steel path to boost any primary/secondary weapon you own.

## Making Plat


### Zariman runs

#### Overview
Mode: any

Requirements: must have completed [The New War](https://warframe.fandom.com/wiki/The_New_War)

Recommended nodes: any on the Zariman

Recommended setup: any that can deal with the missions, but it is recommended you bring [Golden Instinct](https://warframe.fandom.com/wiki/Golden_Instinct) and [Parallax](https://warframe.fandom.com/wiki/Parallax)

Market links: [Molt Augmented](https://warframe.market/items/molt_augmented) [Molt Efficiency](https://warframe.market/items/molt_efficiency) [Molt Reconstruct](https://warframe.market/items/molt_reconstruct) [Molt Vigor](https://warframe.market/items/molt_vigor)

#### Details

This farm is very simple.

1. All you need to do is to run any mission you feel like, pick up the [voidplumes](https://warframe.fandom.com/wiki/Voidplume) as you come across them, finding them with a combination of Golden Instinct and Parallax. Even better if you bring friends who also have this skill and lander.
2. Trade them in with for standing with Archimedean Yonta
3. Go buy the arcanes from Cavalero.
4. Sell them on the market.

### Granum Void farming

Note (September 2022): this method is now less efficient.

#### Overview
Mode: solo

Requirements: must have completed [The Deadlock Protocol](https://warframe.fandom.com/wiki/The_Deadlock_Protocol)

Recommended (fastest) nodes: Skyresh (Phobos, normal), Fossa (Venus, normal, coincides with Jackal), Adresta (Jupiter, extended), Hydra (Pluto, nightmare)

Recommended setup: Mesa with Arcane Velocity + decent energy + some decent damage on the regulators.

Reward table can be found [here](https://warframe.fandom.com/wiki/Granum_Void#Rewards).

Market links: [Stropha](https://warframe.market/items/stropha_set) [Velox](https://warframe.market/items/velox_set) [Stahlta](https://warframe.market/items/stahlta_set)

Assuming you can do 15 runs per hour: will yield about 115 plat per hour (this includes selling sets, accounts for cosmetic and Protea-drops)

#### Details
Running anything but solo makes enemy spawns more random and inconsistent (I didn't fail a single attempt in solo) + the required kill count increases by 25 for each player present. In solo it is possible to beat the challenge on any difficulty within roughly 30 seconds as a solo Mesa. Jump onto any small hill and get your auto-aim focus area tiny and drag it between the 3-4 spots the enemies will keep spawning in.

Playing as mesa also trivialises killing the treasurer.
The treasurer will spawn 2-5 minutes into the mission. If he hasn't spawned by the time you reach the end, just wait by the extraction point, he'll show up eventually.

The disadvantage of running solo is that you won't be able to run a surplus of crowns.

You can see a successful nightmare (top level) run [here](https://www.youtube.com/watch?v=cposSpiwYeo).

### Requiem Mods

Requirements: must have completed [The War Within](https://warframe.fandom.com/wiki/The_War_Within)

You can easily farm requiem mods from hunting [liches](https://warframe.fandom.com/wiki/Kuva_Lich) and cracking [relics dropped from their thralls](https://warframe.fandom.com/wiki/Void_Relic#Requiem_Relics).

The requiem mods sell for 10-15 plat each.

Market links: [Lohk](https://warframe.market/items/lohk) [Xata](https://warframe.market/items/xata) [Jahu](https://warframe.market/items/jahu) [Vome](https://warframe.market/items/vome) [Ris](https://warframe.market/items/ris) [Fass](https://warframe.market/items/fass) [Netra](https://warframe.market/items/netra) [Khra](https://warframe.market/items/khra)

## Increasing Weapon Damage
These are general tips for optimising raw damage and does not account for extra damage or damage multipliers from statuses.

### Damage formula
In order to understand how to maximise weapon damage, you need to understand the damage formula.

The average damage per second formula is as follows (disregarding status effects):

`DPS = base damage * %damage increase factor * %elemental damage increase factor * fire rate * crit factor * multi-shot * bonus damage`

`base damage` is the damage you see in your weapon with no mods installed.

`%damage increase factor` is `1 + total_damage_increase_in_percent/100`, so if you're running a top level hornet strike (220%) and nothing else, this number is `1 + (220)/100 = 3.2`.

`%elemental damage increase factor` is `1 + total_elemental_damage_increase_in_percent/100`, so having primed cryo rounds at max rank (165%) and infected clip at max rank (90%), this number is `1 + (165 + 90)/100 = 3.55`  

`fire rate` is literally just the fire rate. Calculated the same with increases as the above factors: `base_fire_rate * (1 + total_fire_rate_increase_in_percept/100)`. Example with [gunslinger](https://warframe.fandom.com/wiki/Gunslinger) on an [aklex](https://warframe.fandom.com/wiki/Aklex): `1.58 * (1 + 0.72) = 2.7176`

`crit factor` is a combination of critical chance and critical damage. The formula is `1 + (critical_chance/100) * (critical_damage_multiplier - 1)`, so if you have a crit chance of 250% and multiplier of 4.5x, this number is `1 + (250/100) * (4.5 - 1) = 9.75` This means that on average each shot will deal 9.75x damage due to crits - half the hits will deal 8x damage and the other half will deal 11.5. `critical_chance` and `critical_damage_multiplier` are both calculated the same way as the other factors: `base * (1 + percent_increase/100)`

`multi-shot` is literally just the multi-shot number as seen in the stats: `base * (1 + percent_increase/100)`.

`bonus damage` are effects such as toxic lash (Saryn), roar (Rhino) and smite/cleanse/expel/bane mods. These are multiplied with one another, so if you cast toxic lash and it gives you +50% toxin damage, the factor is `1.5`, if you're also roar-buffed for another 50% damage, the number is `1.5 * 1.5 = 2.25`.

#### Notes
* +damage% from weapon arcanes apply additively to `%damage increase factor`. So if you have max stacks on a primary or secondary arcane, that number increases by 3.6.
* [Arcane Avenger](https://warframe.fandom.com/wiki/Arcane_Avenger) adds absolute percentage points to the critical chance rather than applying to the base critical chance. This is incredibly powerful on weapons with a low base crit rate, but high crit multiplier such as the [Kuva Nukor](https://warframe.fandom.com/wiki/Kuva_Nukor), increasing the damage by a factor of 4.275x with a max rank [Primed Target Cracker](https://warframe.fandom.com/wiki/Primed_Target_Cracker) installed.
* Most arcanes apply additively to their respective factors, so on a weapon that has a fire rate of 5, [Lethal Torrent](https://warframe.fandom.com/wiki/Lethal_Torrent) and [Arcane Velocity](https://warframe.fandom.com/wiki/Arcane_Velocity) equipped, while the latter is active, the fire rate will be `5 * (1 + 0.6 + 1.2) = 14.0`.

### Optimising
The general trick to optimising the numbers is to spread out the increases as much as possible. Let's focus on just `%damage increase factor`, `%elemental damage increase factor` and `fire rate`.

Suppose for simplicity we have mods that can increase any of these numbers by 100%, fire rate for simplicty starts off at 1, and that we can only install 6 mods.

The base damage per second is `1 * 1 * 1 = 1` and anything but spreading out the modifiers as much as possible yields suboptimal results. Therefore, the optimal solution here is to apply +200% to each number giving us `3 * 3 * 3 = 27`, you can try shifting the gains around, but I guarantee you, this is the optimal solution (unless you want to fire more often/less often).

Therefore, what you need to consider when picking mods is how much the given factor is already affected. 
If you have a weapon (with base damage 1) that already has +300% damage, but no %elemental damage increase, and you're given the choice between an additional +100% damage or +75% elemental damage, disregarding any needs for specific damage types, the latter option will give a better raw DPS result.

`1 * (1 + (300 + 100) / 100) * 1 = 4`

vs.

`1 * (1 + (300) / 100) * (1 + (75) / 100) = 4.75`

There are therefore some rules of thumb for making well-performing weapons:
* Go for cheap increases in any factor.
* Try to spread out the increases into every factor.
* Weapons are usually either high status chance or high crit chance/damage. Pick mods accordingly: increase already high base numbers and consider crit damage and crit chance as one number (unless the weapon has a low fire rate and you need reliability).

#### Tips
* A lot of this can be done sort of automatically through Overframe - just keep adding mods that are the best at increasing effective damage, but do note that Overframe does some odd assumptions about certain things, here's a list of things you need to be aware of (and hence why it is important to know about the formula above):
  * Not including Kuva Nukor's microwave effect when calculating extra damage due to status effects on mods such as [Galvanized Shot](https://warframe.fandom.com/wiki/Galvanized_Shot).
  * No option to include warframe arcanes in the calculations.
  * No option to apply only specific conditionals.
  * Not taking into special conditions such as a knell's infinite ammo on headshot (thus undervaluaing a mod like anemic agility)
* Make sure to turn apply conditionals in Overframe on and off when modding to have an idea how the weapon performs with and without stacks.
