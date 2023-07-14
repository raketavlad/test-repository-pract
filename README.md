# Шпаркагла по Git

Git — это система контроля версий, которая помогает отслеживать изменения в проекте. Этот инструмент можно использовать как для индивидуальной, так и для командной работы.  
Git позволяет сохранять изменения локально и при необходимости возвращаться к предыдущим версиям проекта. Также можно создать удалённую копию на хостинг-платформе, которая работает с Git, и поделиться результатом с другими.

## Работа с файлом настройки .gitconfig

Глобальные настройки Git хранятся в файле **.gitconfig** в домашней директории.  
Прочитать этот файл: **cat ~/.gitconfig** или **git config --list**.  
Указать имя пользователя: **git config --global user.name [имя или ник на латинице в кавычках]**.  
Указать E-mail пользователя: **git config --global user.email [электронная почта без кавычек]**.  

## Инициализируем репозиторий

### Сделать папку репозиториев - **git init**  
Необходимо зайти в папку и ввести команду: **git init** (initialize - инициализировать).

### "Разгитить" папку, если что-то пошло не так - **rm -rf .git**  
Чтобы "разгитить" папку, нужно удалить скрытую подпапку .git командной **rm -rf .git**

## Проверить состояние репозитория

### Добавляем файлы к сохранению - **git add**  
Подготовить файл: **git add [name]**. Подготовить все файлы: **git add --all**.

### Делаем первый коммит  
Коммит (совершать, фиксировать) — это одна из основных сущностей в Git (и в других системах контроля версий). Коммит гарантирует, что изменения будут сохранены в истории и при необходимости к ним можно будет «откатиться». Это, как если бы вы могли выполнить операцию Ctrl+Z для целой папки (репозитория).  
#### Выполнить коммит - **git commit -m [комментарий в кавычках]  
#### Посмотреть историю коммитов - **git log**.  
#### Привязать удаленный репозиторий к локальному - **git remote add**.  
Команда **git remote add [имя удалённого репозитория (origin)] [URL репозитория]**  
#### Убедиться, что репозитории связаны - **git remote -v** (-v (verbose - подробный)).  
#### Отправить изменения на удалённый репозиторий - **git push**  
При первом вызове команда: **git push -u origin main(или master)**.  
При последующих просто: **git push**.

### Синзронизация репозиториев (удалённого и локального)