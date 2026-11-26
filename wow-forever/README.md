# WoW Forever / Camelot

Client notes from live addon work on **Interface 16001**. Gameplay is mostly Classic. Lua is mostly modern `C_*` APIs.

These files are **client behavior**, not addon source. Copy the facts. Do not treat them as Blizzard docs.

| File | What’s here |
| --- | --- |
| [client.txt](client.txt) | Detect Forever, names, secrets, chat send, TOC, sound |
| [softtarget-game-objects.txt](softtarget-game-objects.txt) | Herb/ore glow, SoftTarget CVars, `UnitExists` vs `UnitIsGameObject` |
| [chat-frames.txt](chat-frames.txt) | `ChatFrameMixin` fade clock and restamp |

Confirm new APIs on the client (`/api`, `C_EventUtils.IsEventValid`). Forever still changes anti-bot / secret rules; fail closed.

Wiki: [World of Warcraft API](https://warcraft.wiki.gg/wiki/World_of_Warcraft_API) lists Forever as **forever**.
