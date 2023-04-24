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

==========================================
Usage
==========================================

Welcome to the documentation for My project! 

.. toctree::
   :maxdepth: 2

   api version
   info
   transfer
   create multi Cheques
   check multi Cheques
   info multi Cheques
   edit multi Cheques
   delete multi Cheques
   check currency
   create invoice
   check invoices
   get invoice
   delete invoice
   
 
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
   info = app.info_multi_Cheques(id=0, data=data) #находим ваш чек по айди
   print(info)
   
delete multi Cheques
------------------------------------------

Эта функция удаляет чек по айди

внимание на код

.. code-block:: python

   import api_Rocket as api
   app = api.Client(token="Your Token")
   info = app.delete_multi_Cheques(id=0) #находим ваш чек по айди и удаляем его
   print(info)
   
check currency
------------------------------------------

Эта функция проверяет доступную валюту

внимание на код

.. code-block:: python

   import api_Rocket as api
   app = api.Client(token="Your Token")
   info = app.check_currency()
   print(info)
   
create invoice
------------------------------------------

Эта функция создает счет

внимание на код

.. code-block:: python

   import api_Rocket as api
   data = {
      "amount": 5, #колво за одну активацию счета
      "numPayments" 1, #колво платижей
      "currency": "TONCOIN", #валюта
      "description": "это описание чека",
      "message": "сообщение которое будет доступно после оплаты счета",
      "url": "ссылка которая будет доступна после оплаты счета",
      "expired": 0, #срок действия счета, 0 - навсегда
   }
   app = api.Client(token="Your Token")
   info = app.create_invoice(data=data)
   print(info)

check invoices
------------------------------------------

Эта функция дает возможность проверять ваши счета

внимание на код

.. code-block:: python

   import api_Rocket as api
   app = api.Client(token="Your Token")
   info = app.check_invoices(limit=100, offset=0) #по умолчания limit=100, offset=0
   print(info)
   
   
get invoice
------------------------------------------

Эта функция дает возможность открыть счет

внимание на код

.. code-block:: python

   import api_Rocket as api
   app = api.Client(token="Your Token")
   info = app.get_invoice(id=0)
   print(info)
   
   
delete invoice
------------------------------------------

Эта функция дает возможность удалить счет

внимание на код

.. code-block:: python

   import api_Rocket as api
   app = api.Client(token="Your Token")
   info = app.delete_invoice(id=0)
   print(info)
 
 
 
.. |beta badge| image:: https://img.shields.io/badge/-beta-orange
  :alt: Beta badge
