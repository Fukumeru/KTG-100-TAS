# [TAS] I Wanna Kill The Guy 100% in 34:18.27
This repository contains files that can be used to playback this TAS. You can check https://github.com/OpenGMK/OpenGMK for playback instructions.

Notes:
- In order to be able to playback this TAS, you would need to download modified KTG, gm8emulator, gm8emulator-wow64 and library files exactly from this repository.
- KTG was compiled using GameMaker 8.0. Can't use newer GM; 8.1 doesn't support bitmap (.fon) fonts that were used in the original game.
- Original KTG's code causes runtime errors. Since gm8emulator can't just simply ignore these errors as original GM8 runner can do, these errors were needed to be removed.
- Some audio inaccuracies could be noticed. Because FMOD's internal functions were replaced by GMFMODSimple's scripts. It was done to cut the dependency on FMOD extension package.
- FMOD's library files were modified to make them work with imported scripts. It was also required to add an extra "fmodex.dll" to make the external sound system work.
- To be able to make a Press input without making a Release input on the same frame, KTG's code was modified. For reference, see `theguy`'s Step Event code.
- To make the last bossfight more entertaining, I have made some objects that control the cursor. It doesn't affect the playback in any way; you can remove these objects and you'd still be able to playback the TAS.
- There's now an extra timeline that makes the player shoot to the music at the beginning of Chapter 1. For reference, see `startgame`'s Create Event code and the new `objMusicShoot` object. It doesn't affect the playback too.
- `geezer_timer` timeline now creates objects that control the cursor. See `geezer_timer` timeline for reference.
- Although Chapter 5 isn't required to be played for 100% category nor it is used in TAS' playback, Chapter 5's code wasn't cleaned up from runtime errors, rendering it impossible to run it in emulator.
- Some of Chapter 5's rooms were modified to have a better visiblity on playback. Otherwise, you would see the player jumping and moving in a totally dark room.
- Mask sprite was slightly modified to make it more visible while TASing (red outline in boundaries of the sprite). This doesn't effect actual hitbox.
- In order to be able to open .gmk project without any errors, you would need to install following fonts:

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

- Make sure to open .gmk project in GameMaker 8.0 because GameMaker 8.1 doesn't support bitmap fonts.
