## 4. Работа с удалённым Git

### Основные команды

git clone <url> - клонировать  
пример: git clone https://github.com/user/repo.git  

git remote add origin <url> - подключить  
пример: git remote add origin https://github.com/user/repo.git  

git push -u origin main - отправить  
пример: git push -u origin main  

git push - отправить изменения  
пример: git push  

git pull - получить изменения  
пример: git pull  

git fetch - скачать без merge  
пример: git fetch  

git remote -v - список репозиториев  
пример: git remote -v  

---

## Работа с форками

1. Нажмите Fork на GitHub  
2. Клонируйте форк  

пример:  
git clone https://github.com/your/repo.git  

3. Добавьте upstream  

пример:  
git remote add upstream https://github.com/original/repo.git  

4. Создайте ветку  

пример:  
git checkout -b fix  

5. Сделайте изменения  

git add .  
git commit -m "fix"  

6. Отправьте  

git push origin fix  

7. Создайте Pull Request  
