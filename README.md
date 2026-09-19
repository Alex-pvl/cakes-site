# Десерты ручной работы

Статический одностраничный сайт кондитерской, свёрстанный по макету Figma. Чистый HTML/CSS, без сборки и зависимостей.

## Деплой на GitHub Pages

Деплой делает workflow [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml): на каждый пуш в `main` он публикует `index.html`, `style.css` и `assets/`. Запустить вручную можно во вкладке **Actions → Deploy to GitHub Pages → Run workflow**.

Первая настройка:

```bash
gh repo create cakes-site --public --source=. --remote=origin --push
gh api -X POST repos/{owner}/{repo}/pages -f build_type=workflow
gh workflow run deploy.yml
```

Вторую команду можно заменить настройкой в интерфейсе: **Settings → Pages → Source: GitHub Actions**.

Сайт появится на `https://<username>.github.io/cakes-site/`.

## Локальный просмотр

```bash
python3 -m http.server 4173
```

и открыть `http://localhost:4173`.
