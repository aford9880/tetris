# Yandex Games publication sheet

Готовые значения для черновика находятся ниже. Название и тексты совпадают с
локализациями игры.

## Technical

- Version: `1.0.0`
- Platforms: Desktop, Mobile / Android, iOS
- Orientation: Any
- Cloud saves: Yes
- Leaderboard technical name: `high_score`
- Archive: `dist/tetris-rpg-time-war.zip`

## Russian

- Name: `Tetris RPG: Time War`
- SEO: `Tetris RPG с боссами, магией и перемоткой времени`
- Short description: `Собирайте линии, побеждайте боссов и переписывайте ход времени в неоновом RPG-тетрисе.`
- About:
  `Tetris RPG: Time War превращает классический тетрис в битву за время. Собирайте полные линии,
  повышайте уровень, копите ману и применяйте четыре способности. Каждые десять линий появляется
  босс со своей атакой и таймером. В игре есть AI-режим, достижения, облачные сохранения и таблица
  рекордов. Играйте на клавиатуре, свайпами или мобильными кнопками.`
- How to play:
  `Перемещайте фигуры стрелками, поворачивайте стрелкой вверх и сбрасывайте пробелом. Очищайте
  линии, чтобы получать очки, XP и ману. Z перематывает время, X взрывает блоки, C очищает
  неполный ряд, V замедляет падение. Кнопка A включает AI. Победите босса до истечения таймера.`
- Categories: Puzzle, RPG
- Tags: tetris, puzzle, rpg, bosses, ai, achievements, time, casual

## English

- Name: `Tetris RPG: Time War`
- SEO: `Tetris RPG with bosses, magic and time rewind`
- Short description: `Clear lines, defeat bosses and rewrite time in a neon RPG twist on classic Tetris.`
- About:
  `Tetris RPG: Time War turns classic Tetris into a battle for time. Clear lines, level up, charge
  mana and use four special abilities. A boss arrives every ten lines with its own attack and
  countdown. The game includes an AI mode, achievements, cloud saves and a leaderboard. Play with
  keyboard controls, swipes or mobile buttons.`
- How to play:
  `Move pieces with the arrow keys, rotate with Up and hard-drop with Space. Clear lines to gain
  score, XP and mana. Z rewinds time, X bombs blocks, C clears an incomplete row, and V slows the
  fall. Press A to toggle AI. Defeat each boss before its timer expires.`
- Categories: Puzzle, RPG
- Tags: tetris, puzzle, rpg, bosses, ai, achievements, time, casual

## Monetization and moderation notes

- Fullscreen ads are requested only after the player explicitly restarts a finished run.
- Rewarded ads are requested only from the `Ad: +40 MP` / `Реклама: +40 MP` button.
- The rewarded bonus is additional mana and is never required to continue.
- Gameplay pauses while any ad is shown.
- The SDK is loaded from `/sdk.js`; local `file://`, localhost and loopback runs use
  a no-SDK fallback so the game remains testable offline.
