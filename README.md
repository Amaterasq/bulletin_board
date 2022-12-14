![](https://img.shields.io/badge/Python-3.11.1-blue) 
![](https://img.shields.io/badge/Django-4.1.4-green)
![](https://img.shields.io/badge/Bootstrap-4-purple)


# Bboard! - размещение объявлений
## pet-project
## Описание
Сайт для публикации и поиска объявлений.
### Пользователи
- Регистрация через эл. почту / удаление аккаунта
- Вход и выход
- Смена пароля
- Изменение личной информации
- Оповещения о комментариях к их объявлениям на эл. почту
- Возможность отключить уведомления о комментариях
- Личный кабинет со всеми выложенными объявлениями
### Объявления
- Рубрики и суперрубрики создаются через админку
- Автор объявления может выбрать суперрубрику и рубрику объявления, название, описание и цену товара, основную и дополнительные картинки
- У объявления есть страница детальной информации (в ней вся информация объявления и автоматическая карусель с картинками если пользователь их добавил, если нет - стандартная)
- Возможность изменять и удалять свои объявления
### Комментарии
- Пользователи и анонимы могут оставлять комментарии к объявлениям (Аноним сам выбирает свой ник и к нему автоматически добавляется 'Anonimous')
- Возможность включить оповещения для автора объявления о комментариях (на почту)
### Лайки
- Авторизованные пользователи могут ставить и отменять   лайки объявлениям (реализовано через javascript, без обновления страницы)

## Инструкции по запуску
1. Склонировать проект
2. Установить зависимости
```sh
pip install -r requirements.txt
```
3. В отдельном терминале с активными виртуальным окружением запустить потчовый сервер (на него будут приходить все эл. письма)
```sh
python3 -m aiosmtpd -n -l localhost:1025
```
4. Создать суперюзера
5. Запустить сайт на localhost
```sh
python3 manage.py runserver
```
6. Создать несколько рубрик

## Как это выглядит
- Главная страница
![index](https://github.com/Amaterasq/bulletin_board/raw/main/project_images/index.png)
- Выпадающее меню профиля

![menu](https://github.com/Amaterasq/bulletin_board/raw/main/project_images/profile_settings.png)
- Выпадающий список рубрик из надрубрик

![rubrics](https://github.com/Amaterasq/bulletin_board/raw/main/project_images/rubrics.png)
- Страница деталей объявления
![bb_detail](https://github.com/Amaterasq/bulletin_board/raw/main/project_images/bb_detail.png)
- Профиль пользователя
![bb_detail](https://github.com/Amaterasq/bulletin_board/raw/main/project_images/profile.png)

P.S. Фронт оставляет желать лучшего, в планах переделать
## Code Style
* [PEP8](https://www.python.org/dev/peps/pep-0008/)