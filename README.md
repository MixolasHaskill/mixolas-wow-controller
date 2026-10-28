# Mixolas HasKill — Steam Controller 2 WoW Keybindings

This repository contains the **Steam Controller WoW** saved keybinding profile for the **KeyBindProfiles** World of Warcraft addon. It is based on the configuration currently used for **Classic Hardcore**; **WoW Forever has not yet been tested against this release**.

## Quick reference

See [KEYBIND-CHEATSHEET.md](KEYBIND-CHEATSHEET.md) for all **102 commands**, organized into controller-use families: targeting, party and pets, interaction, raid markers, movement, combat, camera, interface, and chat. The cheat sheet describes WoW keybindings, not the full physical Steam Input configuration.

## Requirements

- The Steam Controller layout demonstrated in the Mixolas HasKill setup tutorial (a **separate** Steam Input download).
- [KeyBindProfiles](https://www.curseforge.com/wow/addons/keybindprofiles) installed in your WoW version.

## Fresh setup (no existing KeyBindProfiles profiles)

1. Install KeyBindProfiles, then fully exit World of Warcraft.
2. Open your World of Warcraft installation for the version you are playing, and navigate to `WTF/Account/<your-account>/SavedVariables/`.
3. Make a backup of any `KeyBindProfiles.lua` already in that folder.
4. Copy the downloaded `KeyBindProfiles.lua` into that `SavedVariables` folder.
5. Start WoW. Open KeyBindProfiles, select **Steam Controller WoW**, and load/apply that profile.
6. Test targeting, movement, interactions, and ability bindings before combat.

**Already have KeyBindProfiles profiles?** Do **not** simply replace your `KeyBindProfiles.lua` file: doing so will replace access to those saved profiles. Keep your backup and merge the profile with your existing saved variables instead. This download is not a built-in import code.

## Notes

- This package contains the named **Steam Controller WoW** profile only. Personal character data and unrelated profiles were intentionally excluded.
- Keybindings were **not** adjusted or reconciled with `bindings-cache.wtf` or other add-ons.
- Some actions may depend on your installed action-bar or other add-ons, and different WoW versions may behave differently.
- Share freely; no purchase required.