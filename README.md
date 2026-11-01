# AOU Mod — maintained fork

AOU Mod for Anarchy Online, based on [dracul89/aou_mod](https://github.com/dracul89/aou_mod).
This fork repairs local help links and voice filenames, retains upstream's
Skills-window fix, and updates AOU_CYT Preferences for the 18.8.62_EP2 new-engine
client.

**[Download this fork as a ZIP](https://github.com/zooraw/aou_mod/archive/refs/heads/main.zip)**

## Fixed bugs

- **Empty Skills categories:** retains dracul89's upstream fix; all 11 categories
  populate in game.
- **Broken local help pages:** corrects eight links in five files, including the
  Alien General and City Controller pages verified in game.
- **Two missing Line of Fire clips:** removes incorrect `male_` prefixes from
  `target_spotted` and `scratch_another_one` in both playback and macro menus.
- **Missing Basic voice files:** provides an installer that reconstructs 57
  WAV/caption pairs from shipped AO sounds. Line of Fire remains a separate pack;
  installation and required audio settings are in [the voice guide](docs/voice-packs.md).
- **Outdated AOU_CYT Video Settings:** replaces obsolete controls and bindings
  with the current new-engine panel, including working texture-resolution values.
- **Missing AOU_CYT mouse-cursor selector:** restores Detailed, Simple, and None
  under F10 → Controls → Mouse → Mouse cursor context hints.

The Preferences changes above apply to **AOU_CYT**. The two Slim variants have
not received these panel updates. See the verification scope below before
assuming that every setting or gameplay effect has been tested.

## Install or update the GUI

1. Exit Anarchy Online and extract the ZIP to a temporary folder.
2. Open `%LocalAppData%\Funcom\Anarchy Online` and find the data folder for the
   AO installation you use. It normally contains a folder named `Anarchy Online`.
   If you have several installations, select the matching folder rather than
   copying into every one.
3. Copy the extracted `Gui` folder into that `Anarchy Online` data folder.
   Merge folders and replace the AOU mod files when updating.
4. Copy the extracted `scripts` folder into the same data folder. Also copy its
   contents into the `Scripts` folder in the game installation (the folder that
   contains `Anarchy.exe` and `cd_image`).
5. Start AO, enter the world, and run:

   ```text
   /script aou_gui_default
   ```

6. Restart AO to load the AOU skin. If it is already selected, simply restart
   after updating. No character skill or equipment changes are needed.

The original `AOU_Mod_instructions.txt` is retained for historical reference;
use the installation paths above for the current client.

## Optional voice packs

Audio files are installed separately from the GUI and scripts. Follow
[the voice-pack instructions](docs/voice-packs.md) for Ariens' basic sounds and
Windguaerd's Line of Fire v4.0. The ZIP contains no audio binaries.
In **F10 → Audio**, enable **Voices On/Off**, raise **Voices volume**, and allow
the relevant channel under **Hear voices from** (including **Vicinity** for the
guide's test). Captions alone do not confirm audible playback.

## Verification and known limitations

Checked on the AO 18.8.62_EP2 new-engine client:

- AOU_CYT's 15 Preferences pages were compared with the installed stock panel.
  Restored the missing Mouse Cursor Mode selector under Controls → Mouse.
  All controls on 13 pages match stock, including option bindings and radio values;
  Control Center retains AOU's custom layout, and Behaviour retains three extra
  options. Fixed-key definitions also match stock. In game, the AOU Menu visibility
  checkbox hid and restored its button. After restart, Mouse cursor context hints
  displayed Detailed, Simple, and None; Detailed → Simple → Detailed responded,
  with the original Detailed selection restored. This comparison does not
  establish that every setting's gameplay effect has been individually tested.
- Video Settings uses the controls and bindings from this client's stock panel.
  The old texture-resolution, color-depth, compression, and ground-texture controls
  are replaced with current texture, filter, FXAA, brightness, and grass settings.
  Restart AO after updating. In game, texture resolution responded to
  Full → Medium → Full, with Full restored. Other controls were not individually
  exercised; compatibility with the old-engine client has not been verified.
- All 11 Skills categories populate. Save with no pending changes and Close work.
  Spending or resetting skill points has not been tested.
- All 363 literal local file links in `scripts` resolve to packaged files.
- The previously failing Alien General and City Controller help links open in game.
- All 208 distinct voice-pack menu commands have matching WAV/text pairs after
  installing the optional packs. Sample WAVs also play through Windows audio.
  See the voice guide for the scope of in-game verification.
- Daily Rewards returned the same nginx **502 Bad Gateway** with both AOU and
  the stock GUI during testing on October 31, 2026. This fork does not claim to
  repair the reward service or change its address.
- Distorted character shadows remain unresolved. The shadow investigation is
  paused; this fork does not modify rendering shaders or client binaries.
- The separate AriensGUI promotional sound (`/voice AriensGUI`) remains missing
  and is not included in the two optional voice packs.

This is not an exhaustive gameplay test. Bot responses, purchases, reward claims,
and playback on other players' clients have not been verified.

## Credits

Original AOU Mod by Scene and the AO-Universe contributors; AriensGUI and
VoicePack by ArienSky; Alien Database and Line of Fire VoicePack by Windguaerd.
Upstream compatibility fixes by dracul89. This fork adds the link and voice-name
corrections and installation documentation. Original license files are retained.

![AOU GUI](Screenshot_20221009_020157.png)
