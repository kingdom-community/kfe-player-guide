# Commands

Everything on this page is available to every player from the moment you join. Nothing here needs staff, an application, or a server rank. The one thing that does gate a command is your role inside your own tribe, and only your tribe decides that.

This is not the full list. Each plugin carries its own help command — `/f help`, `/wp help`, `/rphelp`, `/ss help`, `/m help`, `/pl help`, `/dsh help` — and those are the complete versions. What follows is what you need on your first day.

---

## Finding your way

| Command | What it does |
|---|---|
| `/sethome` | Marks where you are standing as your home |
| `/home` | Teleports you to it |
| `/de getpos` | Tells you your current coordinates |

Two kinds of sign also work without any command. A `[Spawn]` sign carries you to one of the four origin clearings and makes it your respawn point — clicking a different one later replaces the choice. A `[Warp]` sign teleports whoever right-clicks it, always within the world you are already in.

---

## Your tribe

Tribes are Medieval Factions. Anyone can start one.

| Command | What it does |
|---|---|
| `/f create <name>` | Founds a tribe. Names are capped at 20 characters |
| `/f invite <player>` | Invites someone to yours |
| `/f join <tribe>` | Joins one you were invited to |
| `/apply <tribe>` | Asks to join one you were not invited to. Note the missing `/f` — this one is its own command |
| `/f leave` | Leaves the one you are in |
| `/f info` / `/f who <player>` | Shows your tribe, or which one a player belongs to |
| `/f list` | Lists every tribe on the server |
| `/f chat faction` | Toggles chat that only your tribe hears |

Disbanding is `/f disband`, and it only works if you lead the tribe and are its last remaining member.

---

## Land

| Command | What it does |
|---|---|
| `/f claim` | Claims the chunk you are standing in for your tribe |
| `/f claim <radius>` | Claims a circle of chunks around you, up to a configured maximum |
| `/f unclaim` | Releases the chunk you are standing in |
| `/f checkclaim` | Says who owns the chunk you are standing in |
| `/f map` | Draws a text map of nearby claims |
| `/f sethome` / `/f home` | Sets and teleports to your tribe's home. The home has to sit on your own claimed land, and the teleport has a short delay |
| `/f power` | Shows power statistics for you, or for a tribe you name |

Power is a ceiling on claims rather than something claiming spends, so a tribe can only hold as much land as it has power for. That is the limit on how far a tribe can spread, and it is the number `/f power` is telling you about.

Which of these you can actually run depends on your role in the tribe. A member who has not been given the role for it will be refused.

Locks are separate from claims and work anywhere:

| Command | What it does |
|---|---|
| `/lock` | Turns on lock mode — right-click a block to lock it |
| `/unlock` | Turns on unlock mode — right-click one of your locked blocks |
| `/accessors add` | Right-click a locked block, then type the player's name in chat, to let them in |
| `/accessors remove` | The same, to shut them out |
| `/accessors list` | Right-click a locked block to see who can open it |

---

## Your character

The character card is six fields. Filling it in is optional and takes a minute.

| Command | What it does |
|---|---|
| `/card` | Shows your card |
| `/card lookup <player>` | Shows someone else's |
| `/card name <name>` | Sets your character's name. Changing it again is on a cooldown |
| `/card race <race>` | Sets race |
| `/card subculture <subculture>` | Sets subculture |
| `/card religion <religion>` | Sets religion |
| `/card age <age>` | Sets age |
| `/card gender <gender>` | Sets gender |

No field is checked against a list. Whatever you type is what the card says, which is deliberate — see [`getting-started.md`](getting-started.md) for why the setting is left open.

---

## Talking

`/local` and `/global` are switches. They change where your ordinary typing goes, and they stay switched until you change them back.

| Command | What it does |
|---|---|
| `/local` (or `/rp`) | Sends your normal chat to nearby players only, in character |
| `/global` (or `/ooc`) | Sends it back to server-wide chat |
| `/local hide` / `/local show` | Stops and restarts incoming roleplay chat. While hidden you cannot speak in local chat either |

The rest are one-off messages and do not change your channel:

| Command | What it does |
|---|---|
| `/whisper <message>` | Heard only by players standing right next to you |
| `/yell <message>` | Heard about twice as far out as normal local chat |
| `/lo <message>` | A nearby out-of-character aside |
| `/emote <action>` | A roleplay action, shown to players nearby |
| `/roll` / `/roll 2d6` / `/roll 1d20+5` | Rolls dice, announced to players within 25 blocks. A bare `/roll` is one d20 |
| `/bird <player> <message>` | Sends a bird carrying a message. It flies in real time and arrives later, so distance costs you. Both of you must be online and in the same world, and you can only have one bird out at a time |

The roleplay engine also registers `/me` for emotes, but Minecraft has an `/me` of its own and which one answers has not been checked in-game, so `/emote` is the form to rely on. The same collision applies to `/title`, further down.

---

## Mail

Birds need the other player online. Mailboxes do not.

| Command | What it does |
|---|---|
| `/m send <player> "<message>"` | Sends mail. The quotes are required |
| `/m send <player> "<message>" -attach` | Sends it with the item in your hand attached |
| `/m list` | Lists your mail. `/m list unread` and `/m list archived` narrow it |
| `/m open <id>` | Reads a message and hands you anything attached to it |
| `/m archive <id>` / `/m delete <id>` | Files or destroys one |

---

## Animals

Any entity the server has enabled can be tamed, not just the vanilla few.

| Command | What it does |
|---|---|
| `/wp tame` | Enters taming mode — right-click the animal while holding the right item |
| `/wp list` | Lists the pets you own |
| `/wp select <name>` | Picks which pet the next command applies to. Right-clicking a pet does the same thing |
| `/wp info` / `/wp locate` | Shows details of, or the last known location of, the selected pet |
| `/wp rename <name>` | Renames it, up to 20 characters |
| `/wp follow` / `/wp wander` | Tells it to follow you, or to roam |
| `/wp call` / `/wp gather` | Brings the selected pet, or all of them, to you |
| `/wp lock` / `/wp unlock` | Right-click one of your pets to stop others mounting it, or to allow it again |
| `/wp trade <player>` | Hands the selected pet to another online player permanently |
| `/wp setfree` | Releases it back to the wild |

---

## Skills, items, and history

| Command | What it does |
|---|---|
| `/ss info` | Your skill levels. `/ss info <player>` shows someone else's |
| `/ss skill <name>` | One skill's level cap and what each level costs in experience |
| `/ss top` | The leaderboard, overall or per skill |
| `/pl add "<line>"` | Adds a line of lore to the item in your hand |
| `/pl edit <n> "<line>"` / `/pl remove <n>` | Changes or deletes line `n`, counting from 1 |
| `/title <title>` | Renames the book and quill in your hand, subject to the collision noted above |
| `/at info` | How long you have played and when you last logged in |
| `/at top` | The most active players on the server |

`/pl` writes onto an item, not onto your character. A named sword that carries the line of who it was taken from outlasts the telling of it.

---

## What is not here

Fighting has no command. PvP is ordinary Minecraft combat, bounded by [`rules.md`](rules.md) rather than by the server — with one exception:

| Command | What it does |
|---|---|
| `/duel challenge <player>` | Challenges someone to a duel |
| `/duel accept <player>` | Accepts a challenge |
| `/duel cancel <player>` | Turns one down, or calls off one you sent |

A duel is consent made explicit, which is what rule 6 asks for. It is not the only way to satisfy that rule, but it is the unambiguous one.

Anything not listed on this page is either a staff command or something the plugin help commands will tell you about.

---

*Read [`getting-started.md`](getting-started.md) first if you have not. This page assumes you already know what the server is.*
