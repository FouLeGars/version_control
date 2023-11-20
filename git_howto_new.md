# Подсказка по GIT:

**GIT** - это консольная утилита, для отслеживания и ведения истории изменения файлов, в вашем проекте. Чаще всего его используют для кода, но можно и для других файлов. Например, для картинок - полезно для дизайнеров.

* С помощью Git-a вы можете откатить свой проект до более старой версии, сравнивать, анализировать или сливать свои изменения в репозиторий.
* Репозиторием называют хранилище вашего кода и историю его изменений. Git работает локально и все ваши репозитории хранятся в определенных папках на жестком диске.
* Так же ваши репозитории можно хранить и в интернете. Обычно для этого используют три сервиса: GitHub, Bitbucket, GitLab.

* Каждая точка сохранения вашего проекта носит название коммит (commit). У каждого commit-a есть hash (уникальный id) и комментарий. Из таких commit-ов собирается ветка. Ветка - это история изменений. У каждой ветки есть свое название. Репозиторий может содержать в себе несколько веток, которые создаются из других веток или вливаются в них.

* Для того, чтобы GIT игнорировал какой то файл, нужно создать новый файл с названием .gitignore и внутри этого файла написать название файла, который нужно игнорировать.


# Команды используемые в GIT:

## Создания репозитория:
```sh
git init
```

## Добавление файлов для отслеживания и работой с ними:
```sh
git add
```

## Операция по добавлению всех проиндексированных файлов в репозиторий:
```sh
git commit -M "Message"
```

## Журнал событий:
```sh
git log
```

## Журнал событий в более сжатом виде:
```sh
git log --oneline
```

## Команда для переключения между версиями файлов:
```sh
git checkout
```

## Команда возврата в исходное состояние к актуальной версии файла:
```sh
git checkout master
```

## Команда для перемещения по веткам:
```sh
git checkout name
name - имя ветки, на которую хотим переключиться.
```

## Проверка статуса:
```sh
git status
```

## Команда отмены текущих изменений:
```sh
git restore <file>
```

## Команда ввода номера для просмотра различий между сохранениями:
```sh
git diff
```

## Команда присвоения имени автора для всех коммитов выполненных текущим пользователем:
```sh
git config --global user.name <name>
```

## Команда задает адрес электронной почты автора, который будет использоваться для всех коммитов, выполненных текущим пользователем:
```sh
git config --local user.email <email>
```


## Проверка имени пользователя автора текущих коммитов:
```sh
git config user.name
```


## Проверка почтового ящика пользователя автора текущих коммитов:
```sh
git config user.email
```

## Команда для просмотра на какой именно ветке в списке вы находитесь:
```sh
git branch
```

## Создание новой ветки в GIT:
```sh
git branch name
name - имя новой ветки
```

## Команда для удаления ненужной ветки:
```sh
git branch -d name
name - имя удаляемой ветки
```

## Переименование основной ветки Master в Main:
```sh
git branch -M main
```

## Команда для очистки терминала, чтобы удобнее было работать:
```sh
clear
```

## Команда для слияния веток:
```sh
git merge name
name - имя ветки, которую нужно объеденить с текущей.
```

## Журнал событий в виде красивого графа/древа:
```sh
git log --graph
```

## Клонирование репозитория из другого источника:
```sh
git clone address
address - адрес http:// с которого клонируем репозиторий
```

## Отправка локальных изменения на сервер:
```sh
git push
```

## Команда для удаления ветки из браузера с помощью терминала:
```sh
git push origin --delete name
где name - это имя ветки
```

## Забор изменений с сервера на локальный репозиторий: 
```sh
git pull
```

## Выкачка и слияние текущих изменений из удаленного репозитория:
```sh
git pull --rebase
```

## Переименование ветки Master в Main:
```sh
git branch -M main
```

## Команда показывает какая именно локальная ветка будет отправлена на удалённый сервер:
```sh
git remote show
```

## Более подробный показ какая ветка будет отправлена на удаленный сервер:
```sh
git remote show -v
```

## Перебазирование для придания линейности истории ветки, чтобы удобно отслеживать изменения, или для обновления ветки разработки последними изменениями из основной ветки:
```sh
git rabase
```

## Продолжение перебазирования линейности истории ветки:
```sh
git rebase --continue
```

## Отмена изменений и возврат в состояние до использования команды rebase:
```sh
git rebase --abort
```

## Перезапуск преобразования:
```sh
git rebase --skip
Важно! skip - пропустит (удалит) конфликтный коммит.
```