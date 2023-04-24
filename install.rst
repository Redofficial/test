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
   
 
api version
------------------------------------------

Эта функция дает возможность узнать версию используваемого API

внимание на код

.. code-block:: python

   import api_Rocket as api
   app = api.Client(token="Your Token")
   ver = app.api_version()
   print(ver)







.. |beta badge| image:: https://img.shields.io/badge/-beta-orange
  :alt: Beta badge
