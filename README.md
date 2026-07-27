# Tetris RPG: Time War

Небольшой браузерный Tetris с RPG-механиками: боссы, мана, способности,
перемотка времени, AI-режим, достижения и лидерборд.

## Возможности

- 7 классических тетромино, ghost piece, next piece и bag randomizer.
- Боссы с HP, таймером и атаками мусором.
- Навыки: Rewind, Bomb, Clear и Slow.
- Переключатель AI и скорость 1–10.
- RU/EN локализация с автоопределением языка через Yandex Games SDK.
- Достижения сохраняются локально и через `player.setData`.
- Рекорд отправляется в лидерборд `high_score`.
- Rewarded video за дополнительную ману и interstitial после явного перезапуска.
- Адаптивная вёрстка и управление свайпами/кнопками на мобильных.

## Управление

| Действие | Клавиша |
| --- | --- |
| Движение | `←` `→` |
| Мягкое падение | `↓` |
| Поворот | `↑` |
| Жёсткое падение | `Space` |
| Перемотка | `Z` |
| Бомба | `X` |
| Очистка ряда | `C` |
| Замедление | `V` |
| AI | `A` или кнопка `AI ON/OFF` |
| Скорость | Ползунок или `-` / `+` |
| Пауза | `P` / `Esc` |
| Достижения | Кнопка `🏆` |

## Локальный запуск

Игра не требует сборщика и зависимостей. Откройте `index.html` напрямую или
запустите любой статический сервер:

```powershell
python -m http.server 8080
```

Затем откройте <http://127.0.0.1:8080>.

## Сборка архива для Яндекс Игр

```powershell
.\scripts\build-yandex.ps1
```

Скрипт создаёт `dist/tetris-rpg-time-war.zip`. В корне архива находится
`index.html`, как требует форма загрузки Яндекс Игр.

Перед отправкой в модерацию:

1. Создайте в консоли Яндекс Игр лидерборд с техническим именем `high_score`.
2. Загрузите `dist/tetris-rpg-time-war.zip`.
3. Выберите платформы Desktop и Mobile, ориентацию «любая», языки Russian и English.
4. Отметьте облачные сохранения и монетизацию рекламой.
5. Загрузите `assets/yandex/icon.png` (512×512 PNG), `cover.png` (800×470 PNG)
   и скриншоты из `assets/yandex/screenshots`.
6. Проверьте `Game Ready`, паузу рекламы и rewarded-награду в debug-панели.

Текущие требования и поля черновика:

- [Требования к игре](https://yandex.ru/dev/games/doc/ru/concepts/requirements)
- [Подключение SDK](https://yandex.ru/dev/games/doc/ru/sdk/sdk-about)
- [Реклама](https://yandex.ru/dev/games/doc/ru/sdk/sdk-adv)
- [Загрузка игры и разметка геймплея](https://yandex.ru/dev/games/doc/ru/sdk/sdk-game-events)
- [Заполнение черновика](https://yandex.ru/dev/games/doc/ru/console/add-new-game/draft)

## English

Tetris RPG: Time War is a compact browser Tetris with bosses, mana skills,
rewind, AI mode, achievements, cloud saves and a Yandex Games leaderboard.
The game automatically selects Russian or English and includes a manual toggle.

The game is intentionally dependency-free: `index.html` is the complete runtime
and the Yandex archive can be built with `scripts/build-yandex.ps1`.
