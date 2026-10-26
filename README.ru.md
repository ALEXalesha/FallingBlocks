<div align="center">

# FallingBlocks - Блоки

**Блоки - головоломка с падающими фигурами на одной HTML-странице: собирай ряды, держи фигуру в запасе, крути фигуры в тесные щели. Работает в браузере без сервера и без интернета: откройте `index.html` или играйте онлайн.**

[**▶ Играть онлайн →**](https://alexalesha.github.io/FallingBlocks/) &nbsp;·&nbsp; [English version of this file](README.md)

[![Status](https://img.shields.io/badge/status-stable-brightgreen)](#) [![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE) [![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/docs/Web/HTML) [![Website](https://img.shields.io/badge/Website-open-0A84FF?logo=googlechrome&logoColor=white)](https://alexalesha.github.io/FallingBlocks/) [![Built with Claude Code](https://img.shields.io/badge/Built_with-Claude_Code-D97757?logo=claude&logoColor=white)](https://claude.com/claude-code)

Код, тесты и документация этого проекта написаны Claude (Anthropic) в Claude Code. Идеи, проверка и решения - Алексей.

</div>

> Фанатская игра, не связана с правообладателями похожих игр. Правила вращения - по открытому описанию системы SRS, очередь - «мешок» из семи фигур.

![Меню](docs/screens/menu.png)

![Идёт игра](docs/screens/play.png)

![Режимы игры](docs/screens/modes.png)

## Что есть в игре

- **Режимы:** Марафон (150 линий и 15 уровней, каждые 10 линий быстрее), Спринт (40 линий на время), Ультра (очки за 2 минуты), Дзен (без проигрыша).
- Очки: 100 / 300 / 500 / 800 за одну-четыре линии, умноженные на уровень, T-вращения 400-1600, серия сложных очисток ×1,5, комбо и бонус за чистое поле.
- Призрак фигуры, ожидание на земле до 15 сдвигов, запас раз за ход; DAS, ARR и скорость мягкого падения - в настройках.
- Достижения и рекорды по режимам, переназначение клавиш, геймпад; рисунки, музыка и звуки сделаны в коде.

## Управление

| Клавиша | Действие |
|---|---|
| ← → | сдвиг |
| ↓ | мягкое падение |
| Пробел | жёсткий сброс |
| ↑ или X / Z | поворот по часовой / против |
| C или Shift | в запас |
| Esc или P | пауза |

Где игра это позволяет, клавиши меняются в настройках.

## Запуск у себя

Откройте `index.html` в Chrome, Edge или Firefox. Всё лежит в репозитории, ничего не скачивается.

## Проверки

Законы - проверки Playwright в `tests/`. Они открывают страницу по файловому адресу в безголовом
Chromium, по одной за раз:

```
npm install
npx playwright install chromium
npm test
```

Захват мыши в проверках всегда поддельный: настоящий `requestPointerLock` в безголовом Chromium
на Windows может зажать курсор пользователя.
Кадры выше сняты в безголовом браузере скриптом кадров сборника Hub.

## История

Игра сделана в сборнике [Hub](https://github.com/ALEXalesha/ALEXalesha.github.io), там она же работает в Хабе ([играть там](https://alexalesha.github.io/)). Здесь игра лежит вместе с историей коммитов.

## Лицензия

MIT, см. [LICENSE](LICENSE).
