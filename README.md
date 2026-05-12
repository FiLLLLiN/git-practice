## 8. Работа с удаленным репозиторием

Удаленный репозиторий — это репозиторий, который хранится на сервере, например на GitHub.

Удаленный репозиторий нужен для того, чтобы хранить проект в интернете, загружать изменения, получать изменения с других устройств и организовывать совместную работу.

### Добавление удаленного репозитория

```bash
git remote add origin https://github.com/username/git-instruction.git
```

Пример:

```bash
git remote add origin https://github.com/student/git-instruction.git
```

Здесь:

- `origin` — стандартное имя удаленного репозитория;
- ссылка — адрес репозитория на GitHub.

### Проверка подключенного удаленного репозитория

```bash
git remote -v
```

Пример результата:

```bash
origin  https://github.com/student/git-instruction.git (fetch)
origin  https://github.com/student/git-instruction.git (push)
```

Команда показывает список удаленных репозиториев.

### Отправка основной ветки на GitHub

```bash
git push -u origin main
```

Пример:

```bash
git push -u origin main
```

Параметр `-u` связывает локальную ветку с удаленной. После этого для следующих отправок можно использовать просто:

```bash
git push
```

Если основная ветка называется `master`, используется команда:

```bash
git push -u origin master
```

### Отправка ветки local

```bash
git checkout local
git push -u origin local
```

Пример:

```bash
git checkout local
git push -u origin local
```

### Отправка ветки global

```bash
git checkout global
git push -u origin global
```

Пример:

```bash
git checkout global
git push -u origin global
```

### Получение изменений из удаленного репозитория

```bash
git pull
```

Пример:

```bash
git pull origin main
```

Команда `git pull` загружает изменения из удаленного репозитория и объединяет их с текущей веткой.

### Загрузка изменений без автоматического слияния

```bash
git fetch
```

Пример:

```bash
git fetch origin
```

Команда `git fetch` загружает информацию об изменениях из удаленного репозитория, но не объединяет их автоматически с текущими файлами.

### Клонирование репозитория

```bash
git clone https://github.com/username/git-instruction.git
```

Пример:

```bash
git clone https://github.com/student/git-instruction.git
```

Команда `git clone` скачивает удаленный репозиторий на компьютер.

---

## 9. Работа с форками

Форк — это копия чужого репозитория, созданная в своем аккаунте GitHub. Форки используются для внесения изменений в чужой проект без прямого доступа к оригинальному репозиторию.

### Для чего нужен форк

Форк позволяет:

- скопировать чужой проект в свой аккаунт;
- внести изменения в своей копии;
- отправить предложение изменений автору оригинального проекта;
- безопасно работать с проектом, не изменяя исходный репозиторий.

### Создание форка

Для создания форка необходимо:

1. Открыть чужой репозиторий на GitHub.
2. Нажать кнопку **Fork**.
3. Выбрать свой аккаунт.
4. Дождаться создания копии репозитория.

После этого в аккаунте появится копия проекта.

### Клонирование форка

```bash
git clone https://github.com/username/project.git
```

Пример:

```bash
git clone https://github.com/student/example-project.git
```

### Переход в папку проекта

```bash
cd example-project
```

Пример:

```bash
cd example-project
```

### Добавление оригинального репозитория

Оригинальный репозиторий обычно добавляют под именем `upstream`.

```bash
git remote add upstream https://github.com/original-author/project.git
```

Пример:

```bash
git remote add upstream https://github.com/original/example-project.git
```

### Проверка удаленных репозиториев

```bash
git remote -v
```

Пример результата:

```bash
origin    https://github.com/student/example-project.git (fetch)
origin    https://github.com/student/example-project.git (push)
upstream  https://github.com/original/example-project.git (fetch)
upstream  https://github.com/original/example-project.git (push)
```

Здесь:

- `origin` — личная копия репозитория;
- `upstream` — оригинальный репозиторий.

### Получение изменений из оригинального репозитория

```bash
git fetch upstream
```

Пример:

```bash
git fetch upstream
```

### Обновление своей ветки main

```bash
git checkout main
git merge upstream/main
```

Пример:

```bash
git checkout main
git merge upstream/main
```

Эти команды позволяют обновить свою копию проекта изменениями из оригинального репозитория.

### Создание Pull Request

После внесения изменений в форк их можно предложить автору оригинального проекта.

Общий порядок:

1. Внести изменения в своей копии проекта.
2. Создать коммит.
3. Отправить изменения в свой репозиторий.
4. Открыть GitHub.
5. Нажать кнопку **Compare & pull request**.
6. Описать изменения.
7. Отправить Pull Request.

Пример команд:

```bash
git add .
git commit -m "Исправлена документация"
git push origin main
```

После этого изменения будут доступны в форке на GitHub.

---
