# Шпаргалка по GitHub
---------------------
## Оглавление
[git status](#git_status)  
[Создание веток](#branch_create)   
[Посмотреть список веток](#branch_list)  
[Выбрать другую существующую ветку](#branch_change)  
[Запушить все ветки на сервер](#push_all)  
[Запушить одну ветку](#push_one)  
[Слияние веток](#merge)    
[Удаление ветки(локально)](#branch-del)   
[Удаление ветки(на сервере)](#branch-del-remote)    
[Посмотреть лог изменений](#log)    
[Откат к коммиту](#revert)    
[Отмена последнего коммита(не запушен)](#reset-soft)    
[Удаление последнего коммита(не запушен)](#reset-hard)    

Можно вести разработку проекта на локальном устройстве. Доступно индексирование, коммит.
Для начала необходимо в папке проэкта сделать инициализацию

`git init`

Далее добавляем необходимые файлы, редактируем их и т.д
Командой `git status` проверяем статус файлов репа. Так же можно залить проэкт на GitHub.
Для этого необходимо создать на GitHub новый репозиторий и с помощью пары команд, находясь в
папке локального репозитария(все необходимые файлы проиндексированы и закомичены) 
залить туда ваш локальный проэкт
 
`git remote add origin https://github.com/webabrakadabra/X.git`  
`git push -u origin master`
 
 ### Примеры
-------------------
<a name="git_status"><b><em>git status</em></b></a>

`git status` - проверка статуса локального репозитария.
Допустим в локальный реп. был добавлен новый файл  **new.txt** и также был изменен файл **read.txt**
Делаем команду **git status** 
  
````
git status
 
On branch new2 <-------------Ветка new2
Changes not staged for commit: 
 
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)
 
        modified:   read.txt <------Проиндексированый файл модифицирован (git add .)
 
Untracked files:
  (use "git add <file>..." to include in what will be committed)
 
        new.txt <------------файл еще не проиндексирован (git add .)
 
no changes added to commit (use "git add" and/or "git commit -a") 
````

#### Создание веток  
-------------------  
<a name="branch_create"></a>    
Создание и автоматический переход в новую ветку    
`git chechout -b new_branch`    
Создание без перехода в новую ветку  
`git branch new_branch2`  

#### Посмотреть список веток  
---------------------  
<a name="branch_list"></a>   
`git branch`  
`git branch -v` - подробный вывод  

#### Выбрать другую существующую ветку  
--------------------  
<a name="branch_chahge"></a>  
`git checkout new_branch2`    
#### Запушить все ветки на сервер  
---------------------  
<a name="push_all"></a>    
`git push -all origin`    
#### Запушить одну ветку  
---------------------  
<a name="push_one"></a>  
`git push name_branch origin`   
#### Слияние веток  
--------------------  
<a name="merge"></a>  
`git merge new_branch2`    
#### Удаление ветки(локально)    
---------------------  
<a name="branch-del"></a>  
`git branch -D new_branch2`  
#### Удаление ветки(на сервере)  
-----------------------  
<a name="branch-del-remote"></a>  
`git push origin --delete new_branch2`  
#### Посмотреть лог изменений  
---------------------  
<a name="log"></a>  
`git log`    
#### Откат к коммиту  
----------------------  
<a name="revert"></a>  
`git revert 3f91a9aa4ecae0396c37bc1612e6c1bfdf77e9b5`  
#### Отмена последнего коммита  
----------------------
<a name="reset-soft"></a>  
`git reset --soft HEAD^`    
Эта команда отменит последний коммит (но не изменения, которые вы внесли, они сохранятся).   
#### Удаление последнего коммита(не запушен)  
----------------------------------------  
<a name="reset-hard"></a>  
`git reset --hard HEAD^`  








