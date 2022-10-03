# [TAS] I Wanna Kill The Guy 100% in 34:18.27
This repository contains files required to playback this TAS. You would need to playback .gmtas file presented here to watch this TAS on your machine. Check https://github.com/OpenGMK/OpenGMK for instructions on running the playback.

Notes:
- You would need to download modified KTG, gm8emulator, gm8emulator-wow64 and library files from this repository to playback .gmtas file.
- KTG was compiled using GameMaker 8.0; GameMaker 8.1 doesn't support bitmap (.fon) fonts that were presented in original KTG.
- KTG was modified to make it work with gm8emulator's used version. Original KTG had several code issues, which were causing runtime errors. Runtime errors didn't show up while running because KTG's developer decided to disable showing of error messages. These errors weren't critical, so game was working fine. Emulator crashes at any runtime errors, no matter how critical they are, so these errors were needed to be removed.
- FMOD extension package's functions were replaced by identical imported scripts from GMFMODSimple.
- FMOD's library files were modified to make them work with imported scripts. It was also required to add an extra "fmodex.dll" to make the external sound system work.
- KTG was modified to be able to make press inputs without release inputs. See `theguy`'s Step Event code for reference.
- `geezer_timer` timeline now creates objects that control the cursor. See `geezer_timer` timeline for reference.
- Chapter 5 isn't required to be played for 100% category, hence chapter 5's code wasn't cleaned up from runtime errors, making it impossible to run it in emulator.
- Some of Haunted House rooms were modified to be brighter for better "watchability" (otherwise, you would see kid jumping and moving it totally dark room.) However, there is a video showing these rooms without that change for transparency.
- Mask sprite was slightly modified to make it more visible while TASing (red outline in boundaries of the sprite). This doesn't effect actual hitbox.
- There was added an extra timeline of kid's shooting at the beginning of Chapter 1. It is done purely for entertainment purposes. See `startgame`'s Create Event code and added `objMusicShoot` object for reference. However, this timeline desynchronizates when played too long.
- In order to open .gmk project properly, you would need to install following fonts (this isn't 100% accurate since fonts' name don't save when decompiling):

  - `font1: Tunga`
  - `exor_font: Gungsuh`
  - `transition_font: Vani`
  - `dialog_text: Verdana`
  - `dialog_text2: Ebrima`
  - `font2: Utsaah`
  - `ddr_font: Small Fonts`
  - `font10: Arial`
  - `crate_font: Small Fonts` (closest font)
  - `medium_size: Microsoft Sans Serif`
  - `computer_font: Arial`
  - `vfont: Arial`
  - `Terminal: Small Fonts` (closest font)
  - `menu_font: Upheaval Pro`
  - Link to all these fonts: <https://www.mediafire.com/file/ucrxdi146nnxvik/KTGFonts.rar/file>

- Make sure to open .gmk project in GameMaker 8.0 because 8.1 disabled support of bitmap fonts.
