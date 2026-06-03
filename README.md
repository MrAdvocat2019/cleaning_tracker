# Трекер уборки

Минималистичный веб-трекер на неделю. Один HTML-файл, прогресс хранится в `localStorage`.

## Файлы

- `index.html` — разметка, стили и логика.
- `tasks.js` — список задач. Можно открыть и редактировать вручную.
- `README.md` — этот файл.

## Локально

Открой `index.html` двойным кликом в Finder — откроется в браузере.

## Деплой на GitHub Pages (бесплатно)

1. На [github.com/new](https://github.com/new) создай публичный репозиторий `cleaning_tracker`. **Без** README, .gitignore и лицензии (всё уже есть локально).
2. Из этой папки залей файлы:
   ```sh
   git init
   git add index.html tasks.js README.md
   git commit -m "init cleaning tracker"
   git branch -M main
   git remote add origin https://github.com/<логин>/cleaning_tracker.git
   git push -u origin main
   ```
3. В репозитории: **Settings → Pages → Source: Deploy from a branch → Branch: main / root → Save**.
4. Через минуту приложение откроется по адресу `https://<логин>.github.io/cleaning_tracker/`.
5. Открой URL на телефоне в Safari → «Поделиться» → «На экран Домой». Иконка появится как у нативного приложения.

## Как редактировать задачи

Открой `tasks.js` в любом редакторе. Внутри две константы:

- `WEEKLY_TASKS` — задачи по дням недели (`Mon`–`Sun`).
- `MONTHLY_TASKS` — задачи раз в месяц.

Текст задач можно менять как угодно. После правок перезагрузи страницу.

## Сброс прогресса

- Дневные галочки сбрасываются автоматически в начале каждой ISO-недели (понедельник).
- Месячные — в начале каждого календарного месяца.
- Ручной сброс: в DevTools → Application → Local Storage → удали ключ `cleaning_tracker-v1`.
