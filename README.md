# Theory-Git



## Ветки

#### Создание ветки

Для создания своей ветки 

```
git branch [name-branch]
```

Для перехода в свою ветку

```
git cheсkout [name-branch]
```

Чтобы промотреть все ветки, которые есть в проекте и увидеть в какой ветке сейчас находишься

```
git branch -a
```

Вернуться в ветку master

```
git cheсkout master
```

Чтобы создать ветку и сразу в нее перейти 

```
git cheсkout -b [name-branch]
```


#### Слияние веток

1) Перейдем в ветку master

```
git checkout master 
```

2) Выбрать ветку с которой нужно произвести слияние

```
git marge [name-branch]
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
git chekout [git log id]
```

чтобы вернуться обратно

```
git chekout master
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