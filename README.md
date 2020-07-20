# Theory-Git

Рекомендуемые ресурсы для изучения:

1) [Как научить людей использовать Git](https://habr.com/ru/post/437000/)

2) [Основные GIT Команды](https://www.hostinger.ru/rukovodstva/osnovnie-git-komandy)

3) [Git для тех кто в теме](https://www.atlassian.com/git/tutorials/comparing-workflows)

## Частые вопросы

#### Как доставить все не достающие объекты?

Позволяет пользователю доставить все объекты из удаленного репозитория, которые не присутствуют в локальном рабочем каталоге. Пример применения:

```
git fetch
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
