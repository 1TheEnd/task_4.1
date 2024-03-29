# Команда - ***git fetch***.

## Команда ``git fetch`` используется для получения изменений из удаленного репозитория Git, но не вносит изменения в локальную ветку. Эта команда позволяет вам получить информацию о ветках и коммитах, которых еще нет в локальном репозитории.

## Синтаксис команды ``git fetch``:

```bash=
git fetch [<remote>] [<refspec>...]
```
### Основные флаги:

### ``<remote>``: имя удаленного репозитория Git (например, origin). Если не указан, Git использует имя origin по умолчанию.
### ``<refspec>``: имена веток и тегов, которые вы хотите получить из удаленного репозитория. Если не указан, Git получает все ветки и теги.

## Пример использования команды ``git fetch``:

```bash=
git fetch
```
### *Эта команда получает все изменения из удаленного репозитория Git, который связан с вашим локальным репозиторием. После выполнения этой команды вы можете выполнить команду ``git log origin/master`` для просмотра истории изменений в удаленной ветке master.*
---

```bash=
git fetch origin feature-branch
```
### *Эта команда получает все изменения из удаленной ветки ``feature-branch`` в удаленном репозитории Git, связанном с вашим локальным репозиторием. После выполнения этой команды вы можете выполнить команду ``git log origin/feature-branch`` для просмотра истории изменений в удаленной ветке ``feature-branch``.*
---
### [< назад](./readme.md)
---