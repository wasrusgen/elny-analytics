# ELNY · Аналитика — публичные отчёты

Статический сайт, который GitHub Pages автоматически собирает из этого репо при каждом пуше в `master`.

**Живая ссылка:** https://wasrusgen.github.io/elny-analytics/

## Что внутри

| Файл | Что это |
|---|---|
| `index.html` | Главная — редирект на `status.html` |
| `status.html` | Дашборд статуса пайплайна парсинга (real-time состояние данных) |
| `dashboard.html` | Аналитический дашборд по 6 брендам (ELNY + 5 конкурентов) |
| `reports/*.pdf` | Сгенерированные отчёты (конкурентный анализ, brand voice, SEO, AI visibility) |
| `reports/*.xlsx` | Excel-выгрузки (master, brand_voice, Power Query template) |

## Источник данных

Файлы публикуются скриптом `scripts/publish_to_gh_pages.py` из основного проекта парсинга:
`D:\! Рабочий стол\ELNY\ПАРСИНГ\`

Скрипт копирует свежие `exports/*.html` и выбранные отчёты в этот репо, делает `git commit + push` —
GitHub Pages деплоит в течение 1–2 минут.

## Сырые данные (Parquet)

Parquet-файлы (master, matches, embeddings, и т.д.) **не** хранятся здесь — они опубликованы на
Yandex.Диске в `/ELNY-Аналитика/data/`. Публичные ссылки на каждый файл —
в `config/share_links.yaml` основного проекта.
