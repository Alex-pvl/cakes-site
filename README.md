# Десерты ручной работы

Статический одностраничный сайт кондитерской, свёрстанный по макету Figma. Чистый HTML/CSS, без сборки и зависимостей — можно открыть `index.html` напрямую или задеплоить на GitHub Pages.

## Деплой на GitHub Pages

```bash
gh repo create cakes-site --public --source=. --remote=origin --push
```

Затем в настройках репозитория: **Settings → Pages → Source: Deploy from a branch → Branch: main / (root)**.

Либо вручную, без `gh`:

```bash
git remote add origin https://github.com/<username>/<repo>.git
git branch -M main
git push -u origin main
```

Сайт появится на `https://<username>.github.io/<repo>/`.

## Локальный просмотр

```bash
python3 -m http.server 4173
```

и открыть `http://localhost:4173`.
