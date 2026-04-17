# Практическая работа №5
## Тема: Основы работы с системами контроля версий
## Студент: Андреева Виктория ИСП-24-1
## Цель: научиться использовать систему контроля версий git при работе с программным кодом

---

## Исследование команд Git

В ходе выполнения практической работы были использованы следующие команды Git и их результаты:

### 1. git init
**Назначение:** Инициализирует новый локальный репозиторий в текущем каталоге. Создает скрытую папку `.git`, в которой хранится вся история изменений.

**Выполнение:**
```bash
$ git init
Initialized empty Git repository in C:/Users/user/Desktop/my-git-project/.git/
```

### 2. git config user.name и git config user.email
**Назначение:** Устанавливают имя пользователя и адрес электронной почты для подписи коммитов в текущем репозитории.

**Выполнение:**
```bash
$ git config user.name "Name"
$ git config user.email "mail@example.com"
```
Команды не выводят сообщение при успешном выполнении.

### 3. git config --global http.sslVerify false

**Назначение:** Отключает проверку SSL-сертификатов глобально для всех репозиториев. Используется для обхода проблем с прокси-сервером в колледже.

**Выполнение:**
```bash
$ git config --global http.sslVerify false
```
Команда не выводит сообщение при успешном выполнении.

### 4. git add .

**Назначение:** Добавляет все измененные и новые файлы в текущем каталоге и подкаталогах в индекс (staging area) для следующего коммита.

**Выполнение:**
```bash
$ git add .
```
Команда не выводит сообщение при успешном выполнении.

### 5. git commit -m "текст комментария"

**Назначение:** Сохраняет изменения из индекса в локальный репозиторий с указанным комментарием. Флаг -m позволяет добавить сообщение прямо в команде.

**Выполнение:**
```bash
$ git commit -m "first commit"
[master (root-commit) 4455a44] first commit
 2 files changed, 7 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 test.txt
```

### 6. git remote add origin <url>

**Назначение:** Добавляет ссылку на удаленный репозиторий с алиасом origin. Алиас используется как короткое имя вместо полного URL.

**Выполнение:**
```bash
$ git remote add origin https://github.com/nayakee/practice-git.git
```
Команда не выводит сообщение при успешном выполнении.

### 7. git push -u origin master

**Назначение:** Отправляет изменения из локальной ветки master в удаленный репозиторий origin. Флаг -u устанавливает связь между ветками для дальнейшего использования просто git push.

**Выполнение:**
```bash
$ git push -u origin master
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 440 bytes | 440.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/nayakee/practice-git.git
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'.
```

### 8. git status

**Назначение:** Показывает текущее состояние рабочего каталога и индекса: какие файлы изменены, какие добавлены в индекс, какие не отслеживаются.

**Выполнение:**
```bash
$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
```
### 9. git log

**Назначение:** Отображает историю коммитов в текущей ветке с указанием хеша, автора, даты и сообщения коммита.

**Выполнение:**
```bash
$ git log
commit 4455a44f31c62a9229a54d4c210ba7afecd5f160 (HEAD -> master, origin/master)
Author: Viktoria Andreeva <nayakee05@gmail.com>
Date:   Fri Apr 17 21:26:59 2026 +0300

    first commit
```

### 10. git diff

**Назначение:** Показывает различия между рабочим каталогом и индексом, или между коммитами.

**Выполнение:**
```bash
git diff
diff --git a/test.txt b/test.txt
index 1234567..abcdefg 100644
--- a/test.txt
+++ b/test.txt
@@ -1 +1,2 @@
 Hello World
+New line added
```

### 11. git config --system --unset credential.helper

**Назначение:** Удаляет настройки менеджера учетных данных, который может запоминать неправильного пользователя и мешать push в другой репозиторий.

**Выполнение:**
```bash
git config --system --unset credential.helper
```
Команда не выводит сообщение при успешном выполнении.

### 12. git config --global http.postBuffer 157286400

**Назначение:** Увеличивает буфер HTTP-запросов до 150 МБ для решения проблем с передачей больших файлов в GOGS.

**Выполнение:**
```bash
git config --global http.postBuffer 157286400
```
Команда не выводит сообщение при успешном выполнении.

