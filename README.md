# LR6
Лабораторная работа №6

# Система контроля версий

## Цель работы
Изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.

## 1. Клон репозитория и добавление файла через интерфейс GitHub

Изначально был выполнен клон репозитория в локальное хранилище с помощью команды git clone. ![Клонирование репозитория](screenshots/1.png)

В интерфейсе GitHub с помощью add был добавлен файл fileFromGitHubInterface, и сделан pull для получения данного файла в личный репозиторий. ![Подтягивание изменений в локальный репозиторий командой Pull](screenshots/4.png)

## 2. Настройка клиента Git

Далее были добавлены имя пользователя и email. Эти данные будут использоваться при создании коммитов. ![Настройка имени и email](screenshots/2.png) ![Настройка имени и email](screenshots/3.png)

## 3 Получение истории операций для каждой из веток и последующее их слияние.

Для начала необходимо создать новую ветку с помощью команды git branch "название ветки", далее переходим в эту ветку командой checkout, изменяем файл mergefile.txt и коммитим изменения. Далее меняем тот же файл в ветке master и разрешаем merge conflict в файле и после этого удаляем новую ветку feature. 
![изменяем файл в ветке feature](screenshots/5.png)
![изменяем файл в ветке master](screenshots/6.png)
![просмотр истории операций](screenshots/7.png)
![слияние](screenshots/8.png)
![удаление ветки](screenshots/9.png)

## 4 Добавление изменений и откат коммита

Во-первых создаем файл changes.txt и коммитим его, после добавляем еще один файл newChanges.txt и так же его коммитим. После второго коммита делаем откат с помощью команжды git reset
![Добавление changes.txt](screenshots/10.png)
![Добавление newChanges.txt и откат коммита](screenshots/11.png)

## 5 Лог команд
```bash
git clone git@github.com:setgen-dot/LR6.git
cd LR6
git config user.name "4414 Филиппов Д.С."
git config user.email "den.filippov.m@gmail.com"
git pull
ls
git branch feature
git checkout feature
git status
git add .
git commit -m "change mergefile.txt from feature"
git checkout master
git status
git add .
git commit -m "change mergefile.txt from master"
git log --oneline
git checkout feature
git log --oneline
git checkout master
git merge feature
git add .
git status
git commit
git branch -d feature
git status
git add .
git commit -m "add changes.txt"
git status
git add .
git commit -m "add newChanges.txt"
git status
git reset --hard HEAD~1
```

##  6 История операций

```bash
74788cb | 2025-10-17 | 4414 Филиппов Д.С. | change README.md
49b72de | 2025-10-17 | 4414 Филиппов Д.С. | add screenshots and change README.me
0364673 | 2025-10-17 | 4414 Филиппов Д.С. | add changes.txt
c1ac104 | 2025-10-17 | 4414 Филиппов Д.С. | change mergefile.txt from master
872adb4 | 2025-10-17 | setgen-dot | Create fileFromGitHubInterface
921f53b | 2020-11-21 | Kurtyanik | Обновление информации
c08a654 | 2020-11-21 | Kurtyanik | Файл создан пустым
3c6e913 | 2020-11-21 | Kurtyanik | Initial commit
```

## 7 Выводы
В данной работе были изучены базовые команды для работы с личным и удалённым репозиторием в системе управления версиями. Работа проводилась в среде Git Bash, были использованы команды git pull, git clone, git add, git commit, git checkout, git merge и др.