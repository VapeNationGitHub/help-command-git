### Основы работы с Git и GitHub

Git — это система контроля версий, которая помогает отслеживать изменения в проекте и работать в команде. Она позволяет сохранять разные версии кода, возвращаться к предыдущим, а также объединять изменения нескольких разработчиков.

#### 1. Основные команды для работы с файлами

**1.1 Команды навигации и управления файлами в терминале:**
- `pwd` — отображает текущую директорию.
- `ls` — показывает содержимое текущей директории.
- `cd <имя_папки>` — перемещает в указанную директорию.
- `mkdir <имя_папки>` — создаёт новую папку.
- `touch <имя_файла>` — создаёт новый файл.
- `rm <имя_файла>` — удаляет файл.
- `rmdir <имя_папки>` — удаляет пустую папку.
- `rm -r <имя_папки>` — удаляет папку вместе с её содержимым.

#### 2. Настройка Git

**2.1 Установка и проверка:**
- `git --version` — проверяет установленную версию Git.
- `xcode-select --install` (для macOS) — устанавливает инструменты командной строки, включая Git.

**2.2 Настройка пользователя:**
- `git config --global user.name "Ваше Имя"` — задаёт имя пользователя.
- `git config --global user.email "email@example.com"` — задаёт email.
- `git config --global core.ignorecase false` — делает Git чувствительным к регистру.
- `git config --list` — отображает текущие настройки.

#### 3. Работа с репозиториями

**3.1 Создание локального репозитория:**
- `git init` — инициализирует новый локальный репозиторий в текущей папке.

**3.2 Проверка состояния репозитория:**
- `git status` — показывает состояние файлов (отслеживаемые, изменённые, новые).

**3.3 Подготовка файлов к коммиту:**
- `git add <имя_файла>` — добавляет файл для отслеживания.
- `git add .` — добавляет все изменения в текущей директории.

**3.4 Фиксация изменений (коммит):**
- `git commit -m "Сообщение"` — сохраняет изменения с комментарием.

#### 4. Работа с удалёнными репозиториями

**4.1 Подключение удалённого репозитория:**
- `git remote add origin <адрес_репозитория>` — связывает локальный репозиторий с удалённым.

**4.2 Отправка изменений в удалённый репозиторий:**
- `git push -u origin main` — отправляет изменения из ветки `main` в удалённый репозиторий и устанавливает связь для последующих пушей.
- `git push` — отправляет изменения после первичной настройки.

**4.3 Получение изменений из удалённого репозитория:**
- `git pull` — загружает изменения из удалённого репозитория и объединяет их с локальной версией.
- `git fetch` — загружает изменения без автоматического слияния.
- `git merge <ветка>` — объединяет указанную ветку с текущей.

**4.4 Клонирование удалённого репозитория:**
- `git clone <адрес_репозитория>` — создаёт локальную копию удалённого репозитория.

#### 5. Работа с ветками

**5.1 Основные команды для работы с ветками:**
- `git branch` — показывает список веток.
- `git branch <название>` — создаёт новую ветку.
- `git checkout <название>` — переключается на указанную ветку.
- `git checkout -b <название>` — создаёт и сразу переключается на новую ветку.

**5.2 Слияние веток:**
- `git merge <ветка>` — объединяет изменения из указанной ветки в текущую.

#### 6. GitHub: регистрация и работа

**6.1 Регистрация и настройка GitHub:**
1. Зарегистрируйтесь на [GitHub](https://github.com).
2. Создайте SSH-ключ и добавьте его в GitHub для безопасного подключения:
   - `ssh-keygen -t ed25519 -C "email@example.com"`
   - `pbcopy < ~/.ssh/id_ed25519.pub` — копирует публичный ключ в буфер обмена.
   - Добавьте ключ в разделе Settings > SSH and GPG keys.

**6.2 Создание удалённого репозитория:**
1. На GitHub нажмите "+" > "New repository".
2. Укажите название и параметры репозитория (public/private).

**6.3 Отправка локального репозитория на GitHub:**
1. Подключите репозиторий с помощью `git remote add origin <адрес>`.
2. Отправьте изменения: `git push -u origin main`.

**6.4 Работа с Pull Requests:**
- Pull Request (PR) — это запрос на слияние изменений из одной ветки в другую через GitHub.
- Создайте PR через вкладку "Pull requests" на GitHub и обсудите изменения с коллегами перед слиянием.

#### 7. Полезные советы
- **Описательные коммиты:** пишите информативные сообщения, чтобы легко понять, что было сделано.
- **Работа с .gitignore:** используйте файл `.gitignore` для исключения ненужных файлов из репозитория.
- **Конфликты:** при возникновении конфликтов при слиянии веток, внимательно изучите изменения и разрешите конфликты вручную.

