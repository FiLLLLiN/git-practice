# Инструкция по работе с GIT

## Структура документа

Документ разбит на главы:

- Создание учетной записи в GitHub  
- Установка Git  
- Работа с локальным Git  
- Работа с удалённым Git и форками  

---

## 1. Создание учётной записи в GitHub

1. Перейдите на https://github.com  
2. Нажмите кнопку Sign up  
3. Введите email, пароль и имя пользователя  
4. Подтвердите email  
5. Аккаунт создан  

---

## 2. Установка Git

1. Перейдите: https://git-scm.com/download/win  
2. Скачайте Git  
3. Установите (везде Next)  
4. Проверьте:

git --version

---

## 3. Работа с локальным Git

### Настройка

git config --global user.name "YourName"  
git config --global user.email "your@email.com"  
git config --list  

### Основные команды

git init  
git status  
git add .  
git commit -m "сообщение"  
git commit --amend -m "новое сообщение"  
git log --oneline  
git diff  

### Работа с ветками

git branch  
git checkout -b new-branch  
git checkout main  
git merge new-branch  
git branch -d new-branch  