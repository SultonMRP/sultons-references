# WoW Forever / Camelot

Client notes from live addon work on **Interface 16001**. Gameplay is mostly Classic. Lua is mostly modern `C_*` APIs.

These files are **client behavior**, not addon source. Copy the facts. Do not treat them as Blizzard docs.

## Core

| File | What’s here |
| --- | --- |
| [client.txt](client.txt) | Detect Forever, names, secrets, chat send, TOC, sound |
| [chat-frames.txt](chat-frames.txt) | `ChatFrameMixin` fade clock and restamp |
| [chat-extra.txt](chat-extra.txt) | Links, whisper-to-self, `CHAT_MSG_WHISPER` sender |
| [tooltips.txt](tooltips.txt) | `AddLine` only, no nested `Show`, talent tree vs bags |
| [recipes-vs-crafted.txt](recipes-vs-crafted.txt) | Recipe id vs crafted id on bag vs AH |
| [secure-clicks.txt](secure-clicks.txt) | Lockdown, `[mod:alt]` overlay, dead/ghost |
| [savedvariables.txt](savedvariables.txt) | No mid-session WTF flush |

## World / UI

| File | What’s here |
| --- | --- |
| [softtarget-game-objects.txt](softtarget-game-objects.txt) | Herb/ore glow, SoftTarget CVars, `UnitExists` |
| [bags.txt](bags.txt) | Combined bags, `GetSlotAndBagID`, overlays |
| [merchant.txt](merchant.txt) | `C_MerchantFrame.GetItemInfo`, listing vs sell |
| [minimap-buttons.txt](minimap-buttons.txt) | LibDBIcon vs `UIParent` buttons |

## Items / professions / AH

| File | What’s here |
| --- | --- |
| [items-bind.txt](items-bind.txt) | Quest *class* is not quest-bound; `bindType` |
| [auction-house.txt](auction-house.txt) | No `ReplicateItems`; `IsRetail` vs Camelot |
| [trainer.txt](trainer.txt) | Beast Training `C_Trainer`, do not Classic-filter |
| [professions-enchant.txt](professions-enchant.txt) | Replace-enchant popup, hardware stack |
| [item-id-corrections.txt](item-id-corrections.txt) | Ids that do not match wiki on this client |
| [waylaid-crates.txt](waylaid-crates.txt) | Waylaid crate contents (this client) |

Confirm new APIs on the client (`/api`, `C_EventUtils.IsEventValid`). Forever still changes anti-bot / secret rules; fail closed.

Wiki: [World of Warcraft API](https://warcraft.wiki.gg/wiki/World_of_Warcraft_API) lists Forever as **forever**.
Recipe tooltip mix: [tooltips-and-recipes](https://github.com/SultonMRP/tooltips-and-recipes).
