# Mixolas HasKill — WoW Keybinding Family Cheat Sheet

**Profile:** `Steam Controller WoW`  |  **Source:** `KeyBindProfiles.lua`  |  **Game used for this export:** WoW Classic Hardcore

This reference is grouped into **families** so you can find an entire set of related controls at once. Every keyboard/mouse binding below comes from the named saved profile in the accompanying Lua file. The file includes **102 WoW commands / 104 key assignments**.

> **Read this first:** This is a **WoW keybinding** cheat sheet, not an export of Steam Input button mappings. Steam Input decides which physical controller button sends each key. The exact abilities inside action-bar slots depend on your class, stance, and bar setup. The Always On right-mouse camera and Steam-button free-cursor behavior are configured in **Steam Input**, not in this Lua file.

## Modifier legend (Steam Controller layout)

| Physical control | Modifier sent | Design idea |
|---|---|---|
| L4 | `SHIFT` | Inward / defensive |
| R4 | `CTRL` | Outward / offensive |
| LB | `ALT` | Utility |
| R5 | `SHIFT` + `CTRL` + `ALT` | Full modifier chord |

These physical modifier labels describe the Mixolas Steam Input layout; they are **not** stored by KeyBindProfiles.

## At a glance — most-used families

| Family | Key / chord | What it does |
|---|---|---|
| Targeting | `` ` `` | Nearest enemy |
| Targeting | `` SHIFT-` `` | Nearest friendly player |
| Targeting | `` CTRL-` `` | Nearest enemy player |
| Targeting | `` ALT-` `` | Assist target |
| Targeting | `` ALT-CTRL-` `` | Last target |
| Interaction | `=` | Interact |
| Party | `F7` | Self |
| Party | `F9 / F10 / F11 / F12` | Party members 1–4 |
| Party | `SHIFT-F9 … SHIFT-F12` | Party pets 1–4 |
| Raid markers | `BUTTON3` | Skull |
| Raid markers | `CTRL-BUTTON3` | Cross (X) |
| Raid markers | `ALT-CTRL-SHIFT-BUTTON3` | Moon |
| Movement | `SPACE / NUMPAD0` | Jump |
| Movement | `ALT-SPACE` | Autorun |
| UI | `M` | World map |
| UI | `DOWN` | All bags |
| Chat | `ENTER` | Chat |
| Chat | `CTRL-ENTER` | Slash chat |

## Complete binding list, by family

### Targeting family

The backtick / grave-accent key is the base for your targeting set. **Note:** in this Lua export, `` ALT-` `` is **Assist**, while `` ALT-CTRL-` `` is **Last Target**.

| WoW action | Keyboard / mouse input | Internal command |
|---|---|---|
| Nearest enemy | `` ` `` | `TARGETNEARESTENEMY` |
| Nearest friendly player | `` SHIFT-` `` | `TARGETNEARESTFRIENDPLAYER` |
| Nearest enemy player | `` CTRL-` `` | `TARGETNEARESTENEMYPLAYER` |
| Nearest friendly unit | `` ALT-SHIFT-` `` | `TARGETNEARESTFRIEND` |
| Assist target | `` ALT-` `` | `ASSISTTARGET` |
| Previous / last target | `` ALT-CTRL-` `` | `TARGETLASTTARGET` |

### Party, self & pet targeting family

Self uses `F7`; party slots follow the `F9`–`F12` sequence. Adding Shift targets their pets.

| WoW action | Keyboard / mouse input | Internal command |
|---|---|---|
| Target self | `F7` | `TARGETSELF` |
| Target your pet | `SHIFT-F7` | `TARGETPET` |
| Target party member 1 | `F9` | `TARGETPARTYMEMBER1` |
| Target party member 2 | `F10` | `TARGETPARTYMEMBER2` |
| Target party member 3 | `F11` | `TARGETPARTYMEMBER3` |
| Target party member 4 | `F12` | `TARGETPARTYMEMBER4` |
| Target party member 1 pet | `SHIFT-F9` | `TARGETPARTYPET1` |
| Target party member 2 pet | `SHIFT-F10` | `TARGETPARTYPET2` |
| Target party member 3 pet | `SHIFT-F11` | `TARGETPARTYPET3` |
| Target party member 4 pet | `SHIFT-F12` | `TARGETPARTYPET4` |

### Interact & nameplates family

These are different WoW actions sharing the `=` key family.

| WoW action | Keyboard / mouse input | Internal command |
|---|---|---|
| Interact with target | `=` | `INTERACTTARGET` |
| Sit / stand | `SHIFT-=` | `SITORSTAND` |
| Sheathe / unsheathe weapons | `CTRL-=` | `TOGGLESHEATH` |
| Toggle enemy nameplates | `ALT-CTRL-=` | `NAMEPLATES` |
| Toggle friendly nameplates | `ALT-SHIFT-=` | `FRIENDNAMEPLATES` |

### Raid marker family

`BUTTON3` is the middle-mouse-button event used for the raid-marker family (right-stick North in the Mixolas Steam layout).

| WoW action | Keyboard / mouse input | Internal command |
|---|---|---|
| Raid marker: Skull | `BUTTON3` | `RAIDTARGET8` |
| Raid marker: Cross (X) | `CTRL-BUTTON3` | `RAIDTARGET7` |
| Raid marker: Moon | `ALT-CTRL-SHIFT-BUTTON3` | `RAIDTARGET5` |
| Raid marker: Triangle | `ALT-SHIFT-BUTTON3` | `RAIDTARGET4` |
| Raid marker: Square | `SHIFT-BUTTON3` | `RAIDTARGET6` |
| Raid marker: Diamond | `CTRL-SHIFT-BUTTON3` | `RAIDTARGET3` |
| Raid marker: Circle | `ALT-CTRL-BUTTON3` | `RAIDTARGET2` |
| Raid marker: Star | `ALT-BUTTON3` | `RAIDTARGET1` |

### Movement & camera family

The permanent camera hold and temporary free-mouse mode are configured separately in Steam Input.

| WoW action | Keyboard / mouse input | Internal command |
|---|---|---|
| Move forward | `W` | `MOVEFORWARD` |
| Move backward | `S` | `MOVEBACKWARD` |
| Strafe left | `Q` | `STRAFELEFT` |
| Strafe right | `E` | `STRAFERIGHT` |
| Turn left | `A` | `TURNLEFT` |
| Turn right | `D`, `RIGHT` | `TURNRIGHT` |
| Jump | `SPACE`, `NUMPAD0` | `JUMP` |
| Follow target | `ALT-SHIFT-SPACE` | `FOLLOWTARGET` |
| Toggle autorun | `ALT-SPACE` | `TOGGLEAUTORUN` |
| Toggle walk / run | `NUMPADDIVIDE` | `TOGGLERUN` |
| Camera zoom in | `MOUSEWHEELUP` | `CAMERAZOOMIN` |
| Camera zoom out | `MOUSEWHEELDOWN` | `CAMERAZOOMOUT` |
| Camera pitch up | `INSERT` | `PITCHUP` |
| Camera pitch down | `DELETE` | `PITCHDOWN` |
| Flip camera direction | `ALT-CTRL-SHIFT-9` | `FLIPCAMERAYAW` |

### Action-bar & stance-button family

These actions select **WoW action-bar positions**, not specific spells. A bar position might hold different abilities for different classes or stances. The table is intentionally organized by the **underlying key** (`9`, `3`, `1`, `R`, `F`, mouse button, then `CTRL-F` stance keys), rather than by bar slot number.

| WoW action | Keyboard / mouse input | Internal command |
|---|---|---|
| Bonus action slot 5 | `9` | `BONUSACTIONBUTTON5` |
| Bonus action slot 6 | `ALT-9` | `BONUSACTIONBUTTON6` |
| Bonus action slot 9 | `CTRL-9` | `BONUSACTIONBUTTON9` |
| Bonus action slot 1 | `SHIFT-9` | `BONUSACTIONBUTTON1` |
| Bonus action slot 10 | `ALT-CTRL-9` | `BONUSACTIONBUTTON10` |
| Bonus action slot 2 | `ALT-SHIFT-9` | `BONUSACTIONBUTTON2` |
| Multi-action bar 4, slot 8 | `3` | `MULTIACTIONBAR4BUTTON8` |
| Multi-action bar 1, slot 3 | `ALT-3` | `MULTIACTIONBAR1BUTTON3` |
| Multi-action bar 4, slot 10 | `CTRL-3` | `MULTIACTIONBAR4BUTTON10` |
| Multi-action bar 4, slot 6 | `SHIFT-3` | `MULTIACTIONBAR4BUTTON6` |
| Multi-action bar 1, slot 5 | `ALT-CTRL-3` | `MULTIACTIONBAR1BUTTON5` |
| Multi-action bar 1, slot 1 | `ALT-SHIFT-3` | `MULTIACTIONBAR1BUTTON1` |
| Multi-action bar 4, slot 3 | `ALT-1` | `MULTIACTIONBAR4BUTTON3` |
| Multi-action bar 4, slot 5 | `ALT-CTRL-1` | `MULTIACTIONBAR4BUTTON5` |
| Multi-action bar 4, slot 1 | `ALT-SHIFT-1` | `MULTIACTIONBAR4BUTTON1` |
| Multi-action bar 1, slot 6 | `R` | `MULTIACTIONBAR1BUTTON6` |
| Multi-action bar 1, slot 7 | `SHIFT-R` | `MULTIACTIONBAR1BUTTON7` |
| Multi-action bar 1, slot 8 | `F` | `MULTIACTIONBAR1BUTTON8` |
| Multi-action bar 1, slot 9 | `SHIFT-F` | `MULTIACTIONBAR1BUTTON9` |
| Multi-action bar 1, slot 12 | `BUTTON4` | `MULTIACTIONBAR1BUTTON12` |
| Stance/form button 1 | `CTRL-F1` | `SHAPESHIFTBUTTON1` |
| Stance/form button 2 | `CTRL-F2` | `SHAPESHIFTBUTTON2` |
| Stance/form button 3 | `CTRL-F3` | `SHAPESHIFTBUTTON3` |
| Stance/form button 4 | `CTRL-F4` | `SHAPESHIFTBUTTON4` |
| Stance/form button 5 | `CTRL-F5` | `SHAPESHIFTBUTTON5` |
| Stance/form button 6 | `CTRL-F6` | `SHAPESHIFTBUTTON6` |
| Stance/form button 7 | `CTRL-F7` | `SHAPESHIFTBUTTON7` |
| Stance/form button 8 | `CTRL-F8` | `SHAPESHIFTBUTTON8` |
| Stance/form button 9 | `CTRL-F9` | `SHAPESHIFTBUTTON9` |
| Stance/form button 10 | `CTRL-F10` | `SHAPESHIFTBUTTON10` |

### Saved camera-view family

View switching and view saving are distinct actions.

| WoW action | Keyboard / mouse input | Internal command |
|---|---|---|
| Switch to camera view 1 | `HOME` | `SETVIEW1` |
| Switch to camera view 2 | `SHIFT-HOME` | `SETVIEW2` |
| Switch to camera view 3 | `CTRL-HOME` | `SETVIEW3` |
| Switch to camera view 4 | `ALT-HOME` | `SETVIEW4` |
| Save camera view 1 | `CTRL-SHIFT-HOME` | `SAVEVIEW1` |
| Save camera view 2 | `ALT-SHIFT-HOME` | `SAVEVIEW2` |
| Save camera view 3 | `ALT-CTRL-HOME` | `SAVEVIEW3` |

### Interface & menu family

Panel shortcuts are grouped here regardless of which direction/button your Steam layout uses.

| WoW action | Keyboard / mouse input | Internal command |
|---|---|---|
| Open all bags | `DOWN` | `OPENALLBAGS` |
| World map | `M` | `TOGGLEWORLDMAP` |
| Quest log | `SHIFT-M` | `TOGGLEQUESTLOG` |
| Game menu / Escape | `ESCAPE` | `TOGGLEGAMEMENU` |
| Spellbook | `LEFT` | `TOGGLESPELLBOOK` |
| Talents | `SHIFT-LEFT` | `TOGGLETALENTS` |
| Pet spellbook | `ALT-LEFT` | `TOGGLEPETBOOK` |
| Character panel tab 0 | `UP` | `TOGGLECHARACTER0` |
| Character panel tab 1 | `ALT-UP` | `TOGGLECHARACTER1` |
| Character panel tab 2 | `SHIFT-UP` | `TOGGLECHARACTER2` |
| Character panel tab 3 | `ALT-CTRL-SHIFT-UP` | `TOGGLECHARACTER3` |
| Character panel tab 4 | `CTRL-UP` | `TOGGLECHARACTER4` |
| Guild tab | `ALT-DOWN` | `TOGGLEGUILDTAB` |
| Friends tab | `SHIFT-DOWN` | `TOGGLEFRIENDSTAB` |
| Raid tab | `CTRL-DOWN` | `TOGGLERAIDTAB` |
| Group Finder | `I` | `TOGGLEGROUPFINDER` |
| PvP score screen | `CTRL-SHIFT-M` | `TOGGLEWORLDSTATESCORES` |

### Chat & addon family

The Questie shortcut requires the corresponding addon.

| WoW action | Keyboard / mouse input | Internal command |
|---|---|---|
| Open chat | `ENTER` | `OPENCHAT` |
| Open chat with slash | `CTRL-ENTER` | `OPENCHATSLASH` |
| Reply to whisper (alternate) | `ALT-ENTER` | `REPLY2` |
| Questie: Journey | `;` | `QUESTIE_TOGGLE_JOURNEY` |

## Before you publish or install

1. Install the **KeyBindProfiles** addon in the correct WoW installation.
2. **Back up** your current `WTF/Account/<account>/SavedVariables/KeyBindProfiles.lua` before replacing anything.
3. If you already have saved profiles, **do not overwrite your file**: the provided Lua replaces the saved-variable database. Merge profiles instead or start with a clean installation.
4. Exit WoW completely before copying the Lua file; restart WoW, choose **Steam Controller WoW** in KeyBindProfiles, and apply it.
5. Test the configuration in a safe area first. This export was taken from the Hardcore setup; it has **not** been verified against the final WoW Forever client.

**No abilities are hardcoded into this file.** You will still need to place your abilities in the corresponding action-bar slots or use the matching action-bar setup.
