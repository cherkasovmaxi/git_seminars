![Занятная мысль (на самом деле - нет)!](original.jpg)

> **Интерсная мысль (но на самом деле нет). Поэтому делай инструкции!**

# Cистема контроля версий Git 

# [Основные команды Git](https://gb.ru/lessons/280500) 

## 1. "Представиться" Git 
Для начала необходимо "представиться" программе Git: ввести своё имя и электронную почту
* **git config --global user.name "user.name"**
* **git config --global user.email "e-mail"**

## 2. Инициализация репозитория 
Создать репозиторий Git. При инициализации он создаст скрытую папку. В ней содержатся все объекты и ссылки, которые Git использует и создаёт в истории работы над проектом.
* **git init**

## 3. Добавление файла в отслеживаемые 
Подготовка файла или файлов к коммиту (сохранению версии файла или файлов)
* **git add "file_name"**

## 4. "Закоммичивание" файлов 
Подготовленные в предыдущем пункте файлы (а точнее сказать - изменение в файлах) необходимо сохранить командой и оставить комментарий по внесенным изменениям:
* **git commit -m "comment"**

## 5. Просмотр статуса репозитория 
Просмотр статуса файлов и несохранненых изменений в репозитории
* **git status**

Убрать файл из отслеживаемых командой git status можно следующим образом
* **git ignore**

## 6. Список коммитов в репозитрии
В любой момент можно просмтотреть список всех коммитов с комменатариями 
* **git log** 

*Так же можно посмотреть список всех коммитов с привязкой к веткам
* **git log --graph**


## 7. Переход к другому коммиту (ветке) 
В любой момент можно перейти к другому коммиту или другой ветке (важно: не забудь перед этим "закоммитить" текущие сохранения)
* **git checkout** 

## 8. Просмотр веток в репозитории 
Чтобы работать более эффективно, важно всегда помнить - в какой ветке сейчас работаете
* **git branch** 

## 9. Создание новой ветки в репозитории 
Чтобы работать более эффективно, важно всегда помнить - в какой ветке сейчас работаете
* **git branch branch_name**

>*чтобы ускорить процесс - же можно одновременно создать ветку и сразу перейти в неё одной коммандой*
* **git checkout -b branch_name**

## 10. Слияние и удаление веток 
Слияние - это обьединение веток. Сляиние происходит из той ветки, в которую вы собираетесь сливать (branch_name - название ветки, которую вы присоединяете)
* **git merge branch_name**

*Если ветека больше не нужна - ее можно удалить*
* **git branch -d branch_name**

 ## 11. Разница данных и конфликт 
Полезно перед закоммичиванием изменений посмотреть разницу между измененной версией файла (но еще не закоммиченой) и закоммиченой:
* **git diff**

*При слиянии одного и того же файла из разных веток может получиться конфликт версий, поэтому имеет смысл перед слиянием посмотреть различия*
* **git diff branch_name1..brnach_name2**

# Работа с удаленным репозиторием

## 12. Перенос данных (одной ветки) из локального репозитория в удалённый 

Это делается после создания на GitHub в своем профиле нового репозитория *rep_name*

* **git remote** add *rep_name* https://github.com/account_name/rep_name.git*

* **git branch -M** *branch_name*

* **git push** -u *rep_name* *branch_name*

## 13. Обмен данными с удаленным репозиторием, с которым настроена связь через **git remote**

* **git push** - передать коммит (данные) в удаленный репозиторий

* **git pull** - "притянуть" коммит
 

## 14. "Клонирование" удаленного репозитория 

При этом копируется все содержимое удаленного репозитория (все файлы с версиями) вместе с его историей, устанавливаются удаленные устройства для каждой из вызываемых его ветвей *rep_name*. Затем вы можете использовать git pull для обновления главной ветки.

* **git clone**



# "Интересные" команды Git (которых не было на лекции)

## 15. ["Отложить" в архив](https://www.atlassian.com/ru/git/tutorials/saving-changes/git-stash)

Команда git stash позволяет на время «сдать в архив» (или отложить) изменения, сделанные в рабочей копии, чтобы вы могли применить их позже. 

* **git stash**

Затем происходит откат до исходной рабочей копии. Затем, чтобы вернуть данные из временного архива:

* **git stash pop**

При извлечении отложенных изменений они удаляются из "архива" и применяются к рабочей копии. Также можно применить изменения к рабочей копии, не удаляя их из набора отложенных изменений. Для этого воспользуйтесь командой:
* **git stash apply**

Откладывание изменений полезно, если вам необходимо переключить контекст и вы пока не готовы к созданию коммита.

 Команду git stash можно выполнить несколько раз, после чего можно будет просмотреть список созданных наборов с помощью команды:
 
 * **git stash list**



# Дополнительно по Git

## Интерактивный тренажёр Git. На нём можно улучшить свои навыки работы с данной программой и получить новые.


# Заключение

**Git необходимая и очень удобная программа для работы над проектами. Может применяться не только в IT, но и в любой проектной совместной работе с файлами.**

