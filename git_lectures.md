# GIT - лекция 1

## Установка и Регистрация в Git, начало работы.

***!!! Сначала устанавливаем GIT, затем VS code.***

1. **Проверим версию GIT:**  

> git version

2. **Задаем имя пользователя и e-mail:**
 
> git config --global user.name Alina

> git config --global user.email aax_74@mail.ru

3. **Проверим настройки:**

>git config user.name

>git config user.email

>git config --list

## Работа с папками и файлами

1. **После создания новой папки необходимо добавить ее в контроль версий:**

>git init

2. **После создания файла и для записи изменений, каждый раз необходимо:** *сначала сохранить - Ctrl + S*, **затем ввести команды (также и при изменении имени файла):**

>git add Git_lesson1.md

>git commit -m "Создан файл"

3. **Посмотреть статус папки:**

>git status

4. **Посмотсреть внесенные изменения после сохранения файла:**

>git diff

## Работа с версиями

1. **Посмотреть версии (сохраненные изменения):**

>git log *или* git log --graph

2. **Переход к определенной версии:**

>git checkout 2cb9 - *где 2cb9 - это первые 4 символа коммита.*

3. **возврат к текущей версии:**

>git checkout master


---
---
# GIT - лекция 2

>Clear - очистить окно терминала

## Работа с ветками

1. **Показать имеющиеся ветки:**

>git branch

2. **Создание новой ветки:**

>git branch name_of_new_branch

3. **Переход между ветками**
>git checkout имя_ветки

>git checkout master  -  вернуться к ветке мастер


3. **Слияние веток**
>git merge имя_добавляемой_ветки

*добавление происходит в ту ветку в которой сейчас находишься*

! Если в 2 версиях при слиянии будет разный контент, GIT попросит решить конфликт и выбрать что оставить

4. **Удаление ненужной ветки**
>git branch -d имя_удаляемой_ветки

>git branch -D имя_удаляемой_ветки 
*- удалит ветку даже если она не слита с другой*

## Markdown

Для того чтобы вставить картинку нужно написать
>![Инфо для отображения, если файл не доступен](имя_файлаю.jpg)

Чтобы GIT не отслеживал картинки нужно создать файл <**.gitignore**> и вписать туда имя картинки.

---
---
# Git - лекция 3

## Работа с GITHUB

1. Скачать любой репозитрий себе в VSCode. Ссылку берем из кнопки **Code** в Github/
>git clone https://github.com/AlinaSaitk/group_903.git

2. Загрузить созданный локально репозиторий на Github, нужно сначала создать новый репозиторий на Github, затем написать: 
>git remote add origin https://github.com/AlinaSaitk/test2.git
git branch -M main  
git push -u origin main

При этом при первом обращении Github попросит авторизоваться.

3. Чтобы синхронизировать изменения VSCode --> Github:
>git push

4. Чтобы синхронизировать изменения Github --> VSCode:
>git pull

5. Совместная работа над проектом и предложение по изменению:

* ***fork*** - копирует любой репозиторий к себе в аккаунт

* Затем в VSCode делаем изменения в отдельной ветке.

! *файл README.md всегда называют капсом.*

* Делаем **git push** для внесения измнений на репозиторий на Github.
* После этого в окне на Github появиться возможность отправить ***pull request*** с изменениями


