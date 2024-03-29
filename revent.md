# Команда - ***git revent***

## Команда ``git revert`` используется для отмены определенного коммита и создания нового коммита, который отменяет изменения предыдущего коммита. Это делает команду безопасной для использования в общем репозитории, поскольку она не изменяет историю коммитов.

## Синтаксис команды ``git revert``:

```bash=
git revert <commit>
```
### *где ``<commit>`` - это хэш-идентификатор коммита, который нужно отменить.*
---
## Пример использования команды ``git revert``:

```bash=
$ git log --oneline
d3b3d43 Commit C
786f7f8 Commit B
12556fa Commit A

$ git revert d3b3d43
```
### *Эта команда создаст новый коммит, который отменяет изменения, внесенные коммитом с хэш-идентификатором ``d3b3d43``.*
---
## Флаги:

### ``--no-commit``: применить изменения, но не создавать новый коммит. Это позволяет вам проверить изменения перед тем, как закоммитить их.
### ``-m parent-number``: используется, если коммит имеет несколько родительских коммитов (как в случае с объединением веток). Он указывает, какой из родительских коммитов следует использовать при выполнении операции отмены.

## Пример использования команды ``git revert`` с флагом ``--no-commit``:

```bash=
$ git revert --no-commit d3b3d43
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)
        modified:   file.txt
```
### *Эта команда отменяет изменения, внесенные коммитом с хэш-идентификатором ``d3b3d43``, и добавляет их в индекс. Но новый коммит не создается, пока не будет выполнена команда ``git commit``.*

---
### [< назад](./readme.md)
---