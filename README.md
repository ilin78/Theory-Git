# Theory-Git

Рекомендуемые ресурсы для изучения:

1) [Как научить людей использовать Git](https://habr.com/ru/post/437000/)

2) [Основные GIT Команды](https://www.hostinger.ru/rukovodstva/osnovnie-git-komandy)

3) [Git.Bitbucket tutorials](https://www.atlassian.com/git/tutorials/comparing-workflows)

## Частые вопросы

#### Как доставить все не достающие объекты?

Позволяет пользователю доставить все объекты из удаленного репозитория, которые не присутствуют в локальном рабочем каталоге. Пример применения:

```
git fetch --all
```
Если вдруг Вы ввели 
1. add .
2. git commit -m ''
3. git push - выдал ошибку из-за несоответствия данных на github(например, кто-то внес изменения в удаленный репозиторий, пока вы работали над проектом)
4. то ввести git fetch --all
5. Команда ниже сохранит данные из репо, не ломая свежие изменения (просто обновит текущий). Можно также временно скрыть изменения, сделать git pull, и затем вернуть изменения. Таким образом в проект сохранит историю и Ваши последние изменения.
```
git merge
```

#### Как временно скрыть и вернуть изменения?

Чтобы временно скрыть изменения
```
git stash 
```

Чтобы вернуть изменения 
```
git stash pop
```

#### gitk - графическое представление

#### 

## Ветки

#### Создание ветки

Для создания своей ветки 

```
git branch [имя_ветки]
```

Для перехода в свою ветку

```
git checkout [имя_ветки]
```

Чтобы промотреть все ветки, которые есть в проекте и увидеть в какой ветке сейчас находишься

```
git branch -a
```

Вернуться в ветку master

```
git checkout master
```

Чтобы создать ветку и сразу в нее перейти 

```
git checkout -b [имя_ветки]
```


Переименовать ветку
```
git branch -m [имя_старое] [имя_новое]
```


#### Слияние веток

1) Перейдем в ветку master

```
git checkout master 
```

2) Выбрать ветку с которой нужно произвести слияние

```
git marge [имя_ветки]
```
3) Удалить ветку после слияния 

```
git push origin --delete [имя_ветки]
```

## Коммиты

#### Удаление нескольких коммитов git reset

Нужно выбрать коммит который хотим удалить 
```
git reset [git log --oneline] --hard
```
после этого удаляются измения вместе с коммитом


#### Отмена коммита по одному git revert

```
git revert [git log --oneline]
```
попадаем в редактор Vim и выходим из него

```
:wq
```

#### git chekout [Машина времени]

Чтобы посмотреть интересующий коммит 

```
git checkout [git log --oneline]
```

чтобы вернуться обратно

```
git checkout master
```

#### log --oneline

Промотр логов

```
git log --oneline
```


#### .gitignore

ингнорирование
```
index.html   файла
css/         директории css/
js/*.js      всех .js файлов            
``` 


#### git add
Добавление всех файлов из папки css с расширением .html

```
git add css/*.html
```
или поиск по дочерним папким

```
git add css/**/*.html
```

Не добавлять style.css из папки css / кроме

```
git add !css/style.css
```
или 
```
git add !*.html
```

#### Просмотр изменений 

```
git diff
```


### …or create a new repository on the command line
```git
echo "# tvProfittBackEnd" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/dedmosay/tvProfittBackEnd.git
git push -u origin main
```

### …or push an existing repository from the command line
```git
git remote add origin https://github.com/dedmosay/tvProfittBackEnd.git
git branch -M main
git push -u origin main
```

Author: Ilin Oleg
