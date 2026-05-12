# Comskip of ffmpeg 5 shared for Windows
comskip.exe of "ffmpeg version 5 shared" for windows


## comskip github commit 2ef8684 (first seven(7) characters of the commit hash.)

This is a placeholder of the windows comskip executable that no longer can be compiled because the ffmpeg 7 and later code has changed and corresponding reactionary changes need to be made to the comskip code (https://github.com/erikkaashoek/Comskip ).  These code changes have not been done yet. We are waiting patiently.

The current version of "ffmpeg in MSYS2" is ffmpeg 8, in May 2026.  No easy way exists to go back and get an earlier compiled binary ( means versions 5 or 6 ) of ffmpeg.  No easy way exists to compile comskip.exe without "ffmpeg version 5 in MSYS2."

# Commit 2ef8684 of https://github.com/erikkaashoek/Comskip

a.k.a comskip.exe
```
Commits on Jun 7, 2024
Merge pull request #169 from rboy1/patch-3
erikkaashoek
authored
on Jun 7, 2024
Verified
```
https://github.com/erikkaashoek/Comskip/commit/2ef86841cd84df66fe0e674f300ee49cef6e097a


# Needs an ffmpeg shared version 5

## Original ffmpeg shared version 5

Needs an ffmpeg shared version 5 (Must be "SHARED VERSION" not static). Get it here.
https://github.com/GyanD/codexffmpeg/releases/download/5.0.1/ffmpeg-5.0.1-full_build-shared.7z
( See https://ci.appveyor.com/project/erikkaashoek/comskip/builds/51910208 )

## Alternate ffmpeg shared version 5 
Optionally, get it here.
https://github.com/BtbN/FFmpeg-Builds/releases/download/autobuild-2025-01-31-12-58/ffmpeg-n5.1.6-16-g6e63e49496-win64-gpl-shared-5.1.zip

# Needs the MSYS2 runtime file msys-2.0.dll

The MSYS2 runtime file is needed. A omplaint will occur if the file is missing.
```
msys-2.0.dll
```

# Instructions

1. Extract https://github.com/GyanD/codexffmpeg/releases/download/5.0.1/ffmpeg-5.0.1-full_build-shared.7z to a directory.
2. Download msys-2.0.dll, comskip.exe, and I_Love_Lucy_20260511_12301300.ts, from the Releases: https://github.com/AndreMikulec/Comskip_of_ffmpeg_5_shared_for_Windows/releases
3. Put the `\lib` directory and the `\bin` directory in the PATH
4. Put msys-2.0.dll in the path
5. Put comskip.exe in the PATH
6. Run comskip --help
7. Run the first 20 seconds and THEN STOP of the file I_Love_Lucy_20260511_12301300.ts
8. Notice the commercial starts at zero(0) seconds and the show starts at eleven(11) seconds. Run again I_Love_Lucy_20260511_12301300.ts.
9. Run `comskip --zpcut --zpchapter --scf --videoredo --videoredo3 --csvout --quality --plist I_Love_Lucy_20260511_12301300.ts`
10. Look at the new output `.cut` file contents of `I_Love_Lucy_20260511_12301300.cut`. It reads `JumpSegment("From=0.0000","To=11.0110").`
    This means that the first eleven(11) seconds are identified as commercials
   (and 3rd party .cut-file-reading-software can skip this time range.)
