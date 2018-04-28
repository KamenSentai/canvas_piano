# Canvas piano

## Description

- A piano game featuring `One More Light` by `Linkin Park`

## Features
- Piano drawn with `<canvas>` tag
- Score of the player shown in the middle
- Maluses and bonuses editable in JS
- Activate or deactivate autoplay
- Instrumental version of `One More Light` played in background
- Played vocals as option
- Relay in the menu
- Number of keys `keyMax` adjustable in JS but need to download more sounds if the default value is increased
- Starfield in background to remind the song title and movable according to mouse position of devien orientation
- Stars speed up on bridge of the song
- Menu draggable
- Available on touch screen devices
- AZERTY keyboard required
  - Black keys : ZETYUOP
  - White keys : QSDFGHJKLM

## Technologies
- HTML
- CSS
- JS

## Issues
- Cannot deal with multiple simultaneous keypresses
- Get delay and key for each bar manually
- Do not mistake white keys indexes and black keys indexes
  - Black keys :
    - from `1` to `keyMax-1` for `bars[n].r` for all `n` natural number
    - every key with an index `n%7==0` or `n%7==3` is deleted
  - White keys :
    - from `0` to `keyMax-1` for `bars[n].r` for all `n` natural number
    - two keys are overflowed from the screen in order to create shadows to `whiteKeys[1]` and `whiteKeys[keyMax]`
- Edit `keyMax` implies editing CSS for menu
- Edit keyboard height implies editing CSS for some heights
- Vocals might be shifted if not activated ate the beginning even if the current times of instrumental and vocals are the same when logged in console
- Do not work well on devices if hosted in GitHub
  - sounds might need to be converted to `.mp3`
  - musics are not played or are shifted very late
  - need to add `user-scalable:no` to work when test on `Google Chrome` in order to prevent from rotation resizing but doens't work anymore when hosted

## Coding
- HTML
  - no W3C error
- CSS
  - `::selection` and property `user-select` not recognized by W3C
- JS
  - Modernizr check

## Todo
- Clean CSS file and JS file
  - Use classes for the keys
- Use Gulp template to seperate files
- Redesign the game

## Credits
- Author : Alain Cao Van Truong
- Band : [Linkin Park](https://www.linkinpark.com)
- Music : [One More Light](https://www.youtube.com/watch?v=Tm8LGxTLtQk)
- Piano version : https://www.youtube.com/watch?v=v8fWtZTWHEg
- Piano sounds : https://freesound.org/people/jobro/packs/2489/
- Teacher : [Bruno Simon](https://github.com/brunosimon)
