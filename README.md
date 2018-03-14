# Шпаргалка по GitHub
---------------------
## Оглавление
[git status](#git_status)  
[Создание веток](#branch_create)   
[Посмотреть список веток](#branch_list)  
[Выбрать другую существующую ветку](#branch_change)  
[Запушить все ветки на сервер](#push_all)  
[Запушить одну ветку](#push_one)

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
`git push -all origin`    
#### Запушить одну ветку  
---------------------  
`git push name_branch origin` 


