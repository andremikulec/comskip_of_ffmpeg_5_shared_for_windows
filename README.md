# Comskip of ffmpeg 5 shared for Windows
comskip.exe of "ffmpeg version 5 shared" for windows


## comskip github commit 2ef8684 (first seven(7) characters of the commit hash.)

This is a placeholder of the windows comskip executable that no longer can be compiled 
because the ffmpeg 7 and later code has changed and corresponding reactionary changes need
to be made to the comskip code (https://github.com/erikkaashoek/Comskip ).  
These code changes have not been done yet. We are waiting patiently.

The current version of ffmpeg in MSYS2 is ffmpeg 8 in May 2026.
No easy way exists to go back and get an earlier compiled binaries ( means versions5 and 6 ) of ffmpeg.
No easy way exists to compile comskip.exe without "ffmpeg version 5 in MSYS2."

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

# Need an ffmpeg shared version 5

Needs ffmpeg shared version 5 (Must be "SHARED VERSION" not static)
https://github.com/GyanD/codexffmpeg/releases/download/5.0.1/ffmpeg-5.0.1-full_build-shared.7z
( See https://ci.appveyor.com/project/erikkaashoek/comskip/builds/51910208 )

Alternate ffmpeg shared version 5 
https://github.com/BtbN/FFmpeg-Builds/releases/download/autobuild-2025-01-31-12-58/ffmpeg-n5.1.6-16-g6e63e49496-win64-gpl-shared-5.1.zip

# Needs the MSYS2 runtime file msys-2.0.dll

Direct MSYS2 runtime requirement needed. complaints if missing ...
```
msys-2.0.dll
```

# Instructions

1. Extract https://github.com/GyanD/codexffmpeg/releases/download/5.0.1/ffmpeg-5.0.1-full_build-shared.7z
2. Put the `\lib` directory and `\bin` directory in the PATH
3. Put  msys-2.0.dll in the path
4. Put  comskip.exe in the PATH
5. Run  comskip  --help
6. Run  The first 20 seconds ONLY THEN STOP!- I_Love_Lucy_20260511_12301300.ts
7. Notice the commercial starts at zero(0) seconds and the show starts at eleven(11) seconds. Run again I_Love_Lucy_20260511_12301300.ts
8. Run  comskip --zpcut --zpchapter --scf --videoredo --videoredo3 --csvout --quality --plist I_Love_Lucy_20260511_12301300.ts
9. Look at the NEW output file I_Love_Lucy_20260511_12301300.cut  Notice that the first 11 seconds of commercials have been SKIPPED
