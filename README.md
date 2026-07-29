# Tetris RPG: Time War

Браузерный Tetris с RPG-механиками: боссы, мана, навыки, перемотка времени,
AI-режим, бонусы, перегрузка (overload), контракты, достижения, облачные
сохранения и лидерборд Яндекс Игр.

Игра не требует сборщика и зависимостей — всё в одном `index.html`.

## Возможности

- 7 классических тетромино, ghost piece, next piece и bag randomizer.
- **Система уровней и XP** — рост сложности, увеличение скорости.
- **Мана (MP)** — ресурс для навыков. Пополняется за очистку линий, level up,
  победу над боссом, бонусы и рекламу.
- **4 активных навыка:** Rewind (Z), Bomb (X), Clear (C), Slow (V).
- **Боссы** — 5 видов с HP, таймером и мусорными атаками.
- **Перемотка времени** — откат поля на ~15 шагов (60 MP).
- **Бонусы** — 6 эффектов: молния, заморозка, щит, мана, перегрузка,
  предвидение. Выдаются за серию из 4 очисток.
- **Контракты** — временные задания при появлении босса.
- **Шкала перегрузки (Overload)** — при ≥70% даёт ×1.5 очков за линии.
- **AI-режим** — компьютер играет сам (клавиша A).
- **Ползунок скорости 1–16** (клавиши `-` / `+`).
- **RU/EN локализация** с автоопределением языка.
- **6 достижений** — сохраняются локально и в облаке.
- **Лидерборд** `high_score` через Yandex Games SDK.
- **Облачные сохранения** профиля через `player.setData`.
- **Монетизация:** rewarded video (бонус-реролл) и interstitial (при рестарте).
- **Адаптивная вёрстка** и управление свайпами/кнопками на мобильных.

## Управление

| Действие | Клавиша |
| --- | --- |
| Движение | `←` `→` |
| Мягкое падение | `↓` |
| Поворот | `↑` |
| Жёсткое падение | `Space` |
| Перемотка (Rewind) | `Z` |
| Бомба (Bomb) | `X` |
| Очистка ряда (Clear) | `C` |
| Замедление (Slow) | `V` |
| AI вкл/выкл | `A` или кнопка в панели |
| Скорость | Ползунок или `-` / `+` |
| Пауза | `P` / `Esc` |

На мобильных: касание — поворот, свайпы — движение; кнопки `←` `↻` `↓` `→` `⤓`.

## Локальный запуск

Откройте `index.html` напрямую или запустите статический сервер:

```powershell
python -m http.server 8080
```

Затем откройте <http://127.0.0.1:8080>.

## Сборка архива для Яндекс Игр

```powershell
.\scripts\build-yandex.ps1
```

Скрипт создаёт `dist/tetris-rpg-time-war.zip`. В корне архива — только
`index.html`, как требует форма загрузки.

Перед отправкой в модерацию:

1. Создайте в консоли Яндекс Игр лидерборд с техническим именем `high_score`.
2. Загрузите `dist/tetris-rpg-time-war.zip`.
3. Выберите платформы Desktop и Mobile, ориентацию «любая», языки Russian и English.
4. Отметьте облачные сохранения и монетизацию рекламой.
5. Загрузите `assets/yandex/icon.png` (512×512 PNG), `cover.png` (800×470 PNG)
   и скриншоты из `assets/yandex/screenshots`.
6. Проверьте `Game Ready`, паузу рекламы и rewarded-награду в debug-панели.

Подробнее — в [`yandex-publishing.md`](yandex-publishing.md).

## English

Tetris RPG: Time War is a compact browser Tetris with RPG mechanics — bosses,
mana skills, time rewind, AI mode, 6 power-ups, overload, contracts,
achievements, cloud saves and a Yandex Games leaderboard. The game auto-detects
Russian or English with a manual toggle.

The game is intentionally dependency-free: `index.html` is the complete runtime.
Build the Yandex archive with `scripts/build-yandex.ps1`.
