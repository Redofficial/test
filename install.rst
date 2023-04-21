Rocket
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

This section should provide a reference to your project's API.

Contributing
------------------------------------------

This section should provide information on how to contribute to your project.

Changelog
------------------------------------------

This section should provide a changelog for your project.


Usage
==========================================

.. toctree::
   :maxdepth: 2

   Usage
   
 
Usage
------------------------------------------

This section should provide instructions on how to use your project.
