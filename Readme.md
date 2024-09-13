# Python
Как установить ?
```pip
pip install tg-bot-sender
```
## Импорты 
```python
from tg_bot_sender import Data, TelegramSender
```
## Начало работы
logs параметр указывает на сохранения логов в json формате
```python
tg = TelegramSender(telegramToken, logs = False)
```
## Варианты отправки сообщений
#### sendFromIds - отправка пользователям
```python
tg.sendFromIds([...telegramUserIds], Data(
    text = 'Hello',
    photo = 'Photo link',
    buttons = [{
        buttonTitle: 'Hello',
        buttonUrl: 'https://google.com'
    }]
))
```
#### sendFromId - отправка пользователю
```python
tg.sendFromIds(telegramUserId, Data(
    text = 'Hello',
    photo = 'Photo link',
    buttons = [{
        buttonTitle: 'Hello',
        buttonUrl: 'https://google.com'
    }]
))
```
