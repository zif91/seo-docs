# 🌐 Настройка публичного сайта

Ваша база знаний может автоматически публиковаться как красивый сайт через GitHub Pages!

## ✅ Что уже настроено:

1. **GitHub Actions workflow** создан (`.github/workflows/deploy-quartz.yml`)
2. **Quartz** будет автоматически собирать сайт при каждом пуше в `main`
3. **Все ссылки Obsidian `[[]]`** будут работать на сайте
4. **Поиск, графы, темы** - всё включено

## 🚀 Шаги для активации:

### Шаг 1: Включите GitHub Pages

1. Перейдите в настройки репозитория: https://github.com/zif91/seo-docs/settings/pages
2. **Source:** Выберите **"GitHub Actions"** (не Branch!)
3. Сохраните

### Шаг 2: Запустите workflow

Workflow запустится автоматически при следующем пуше, или запустите вручную:

1. Перейдите в https://github.com/zif91/seo-docs/actions
2. Выберите "Deploy Quartz Documentation Site"
3. Нажмите "Run workflow" → "Run workflow"

### Шаг 3: Подождите 2-5 минут

GitHub соберёт и опубликует сайт.

## 📍 Адрес вашего сайта:

```
https://zif91.github.io/seo-docs/
```

## 🔄 Как обновлять сайт

Просто редактируйте `.md` файлы в Obsidian и делайте `git push`:

```bash
cd /Users/zif91/Downloads/SEO_Knowledge_Base_Obsidian/SEO_docs

# После редактирования в Obsidian:
git add .
git commit -m "Обновил контент"
git push
```

Сайт автоматически обновится через 2-3 минуты!

## 🎨 Возможности сайта:

- ✅ **Поиск** по всей базе знаний
- ✅ **Graph View** - визуализация связей между темами
- ✅ **Backlinks** - кто ссылается на эту страницу
- ✅ **Table of Contents** - навигация по разделам
- ✅ **Темная/светлая тема** - автоматическое переключение
- ✅ **Мобильная версия** - адаптивный дизайн
- ✅ **SPA** - быстрая навигация без перезагрузки
- ✅ **Popovers** - превью при наведении на ссылки
- ✅ **RSS** - подписка на обновления

## ⚙️ Кастомизация (опционально)

Если хотите изменить внешний вид, отредактируйте конфиг в workflow-файле:
`.github/workflows/deploy-quartz.yml`

Можно изменить:
- Название сайта (`pageTitle`)
- Цветовую схему (`colors`)
- Шрифты (`typography`)
- Включить Google Analytics

Документация Quartz: https://quartz.jzhao.xyz/

## 🌳 Структура репозитория:

```
seo-docs/
├── main (ветка)              ← Obsidian vault + исходники
│   ├── *.md                  ← Ваши заметки
│   ├── .obsidian/            ← Настройки Obsidian
│   └── .github/workflows/    ← Автоматическая публикация
│
└── quartz-site (ветка)       ← Резервная копия полного Quartz (не используется для публикации)
```

## 📝 Автоматизация через Obsidian Git

Для максимальной автоматизации установите плагин **Obsidian Git**:

1. В Obsidian: Settings → Community Plugins → Browse
2. Найдите **"Obsidian Git"**
3. Установите и активируйте
4. Настройте:
   - Auto-commit: каждые 10 минут
   - Auto-pull: каждые 10 минут
   - Auto-push: после каждого коммита

Теперь ваши изменения будут автоматически публиковаться на сайт!

---

**Вопросы?** Создайте Issue: https://github.com/zif91/seo-docs/issues
