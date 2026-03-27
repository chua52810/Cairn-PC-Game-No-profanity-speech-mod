# No-profanity speech mod
Cairn is an exceptional climbing simulator, boasting beautiful graphics, captivating soundscapes, and innovative gameplay. There is just 1 problem - the game has no built-in remove profanity speech toggle. As of Mar 2026, official support for this feature remains unavailable. With this mod, players can transform the game experience, effectively shifting the game's rating from Mature to Family-friendly.

# Usage
1. Go to the game sound directory at
   "..\Cairn\Cairn_Data\StreamingAssets\Audio\GeneratedSoundBanks\Windows\English(US)".
   
2. Rename the original "character.bnk", "dialogue.bnk" as "character1.bnk", "dialogue1.bnk".
 
3. Download both "character.bnk" and "dialogue.bnk" and copy both files to the sound directory.

# Full mod creation guide
Cairn uses Audiokinetic Wwise software for all sound and music. Individual sound files use WEM file extension, while multiple sound files are packaged together as a BNK file. TXT files, which map logical names (e.g., cs_34010_aava_slurps) to physical WEM files, are provided for each BNK file.

To create the mod, AI (Claude/Chatgpt/Gemini)  + vibe coding utilised as below:

1. Use AI to read all TXT files to identify which BNK packages likely contain profanities.
   -> "character.bnk" and "dialogue.bnk" tagged as most likely packages.

2. Run Wwise Unpacker to unpack "character.bnk" and "dialogue.bnk" to get both WEM and WAV files.
   
3. Install python (v3.11 or below) + whisper (Use medium model) to transcribe the WAV files into TXT files.

4. Run a script to compare all the transcribed TXT files against a profanity list and flag those that contain profanities.
   
5. Run FFmpeg on th
   
