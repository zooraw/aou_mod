# AOU Mod — maintained fork

AOU Mod for Anarchy Online, based on [dracul89/aou_mod](https://github.com/dracul89/aou_mod).
This fork repairs eight local help links and two Line of Fire voice filenames.
It retains upstream's Skills-window fix.

**[Download this fork as a ZIP](https://github.com/zooraw/aou_mod/archive/refs/heads/main.zip)**

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

This is not an exhaustive gameplay test. Bot responses, purchases, reward claims,
and playback on other players' clients have not been verified.

## Credits

Original AOU Mod by Scene and the AO-Universe contributors; AriensGUI and
VoicePack by ArienSky; Alien Database and Line of Fire VoicePack by Windguaerd.
Upstream compatibility fixes by dracul89. This fork adds the link and voice-name
corrections and installation documentation. Original license files are retained.

![AOU GUI](Screenshot_20221009_020157.png)
