####################
Rocket |beta badge|
####################
==========================================

Welcome to the documentation for My project! 

language: Russian

.. toctree::
   :maxdepth: 2

   introduction
   translations
   installation
   api_reference
   contributing
   changelog

Introduction
------------------------------------------

Наш проект решает многие проблемы, вот например

.. table:: таблица

   +---------------++---------------+
   |    пример     |    пример      |
   +===============++===============+
   |простые функции|     None       |
   +---------------++---------------+
   | быстрый доступ|настройка       |
   +---------------++---------------+
   |легко изучаемый| None           |
   +---------------++---------------+
   
Наш проект создан просто так, и выпущен в общий доступ для всеобщего обзора и использувания



Installation
------------------------------------------

чтобы скачать

.. code-block:: bash

   pip install api-Rocket
   
потом проверяем маленьким скриптом

.. code-block:: python

   import api_Rocket as api
   app = api.Client(token="Your Token")
   ver = app.api_version()
   print(ver)

готово

API Reference
------------------------------------------

Мы используем официальное API TonRocket'a
   
создатель официального API: `RocketMan <https://t.me/RocketBotCEO>`_

официальное `API <https://pay.ton-rocket.com/api/>`_

Contributing
------------------------------------------

Мы будем очень благодарны если вы захотите нам помочь

чем моежете нам помочь? та все просто

1. находите баги или глюки - сообщаете `нам <https://t.me/Redpiar>`_
2. есть идея как улучшить производительность - сообщаете `нам <https://t.me/Redpiar>`_
3. если есть совершенно любые идеи - сообщаете `нам <https://t.me/Redpiar>`_

Changelog
------------------------------------------

в этом обновлении произошло следующие:

1. добавлено proxies
2. добавлено exceptions
3. добавлена одна функция в async client


Usage
==========================================

.. toctree::
   :maxdepth: 2

   api version
   info
   transfer
   create multi Cheques
   check multi Cheques
   info multi Cheques
   edit multi Cheques
   
 
api version
------------------------------------------

Эта функция дает возможность узнать версию используваемого API

внимание на код

.. code-block:: python

   import api_Rocket as api
   app = api.Client(token="Your Token")
   ver = app.api_version()
   print(ver)


info
------------------------------------------

Эта функция дает информацию про ваш кошелек

внимание на код

.. code-block:: python

   import api_Rocket as api
   app = api.Client(token="Your Token")
   info = app.info()
   print(info)

transfer
------------------------------------------

Эта функция дает возможность отправлять кому-то валюту

внимание на код

.. code-block:: python

   import api_Rocket as api
   
   data = {
      "userid": 0, #int, телеграмм айди пользователя
      "currency": "TONCOIN", #str, валюта
      "amount": 0, #int, кол-во валюты для передачи
      "comment": None #комментарий
   }
   
   app = api.Client(token="Your Token")
   tr = app.transfer(data=data)
   print(tr)
   

create multi Cheques
------------------------------------------

Эта функция создает мульти чек

внимание на код

.. code-block:: python

   import api_Rocket as api
   data = {
      "currency": "TONCOIN", #str, валюта
      "PerUser": 0.1, #int, float, за пользователя
      "usersNumber": 5, #int, кол-во активаций
      "refProgram": 2, #int, реф программа для пользователя
      "password": "RdGd234", #пароль на чек
      "telegramResurce": "https://t.me/channel" #ссылка на ваш тг канал
   }
   app = api.Client(token="Your Token")
   multi = app.create_multi_Cheques(data=data)
   print(multi)
   
check multi Cheques
------------------------------------------

Эта функция показывает все ваши мульти чеки

внимание на код

.. code-block:: python

   import api_Rocket as api
   app = api.Client(token="Your Token")
   info = app.check_multi_Cheques()
   print(info)
   
либо же 

.. code-block:: python

   import api_Rocket as api
   app = api.Client(token="Your Token")
   info = app.check_multi_Cheques(limit=100, offset=0) #по умолчания limit=100, offset=0
   print(info)
   
info multi Cheques
------------------------------------------

Эта функция показывает полную информацию про ваш чек

внимание на код

.. code-block:: python

   import api_Rocket as api
   app = api.Client(token="Your Token")
   info = app.info_multi_Cheques(id=0) #находим ваш чек по айди
   print(info)


edit multi Cheques
------------------------------------------

Эта функция дает возможность редактировать чеки

внимание на код

.. code-block:: python

   import api_Rocket as api
   data = {
      "password": "hhfggs086",
      "telegramResurce": None,
   }
   app = api.Client(token="Your Token")
   info = app.info_multi_Cheques(id=0) #находим ваш чек по айди
   print(info)
   
.. |beta badge| image:: https://img.shields.io/badge/-beta-orange
  :alt: Beta badge
