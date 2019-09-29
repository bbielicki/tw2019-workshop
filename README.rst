:title: TW2019 BDD workshop

.. :skip-help: true

:css: css/my.css

.. header::
    Testowanie BDD web aplikacji przy użyciu python'a oraz docker'a

.. footer::
    Dariusz Duleba & Bartosz Bielicki, TestWarez 2019

----

.. image:: img/start.png

----

Poznajmy się :)
---------------

.. note::
    * my zaczynamy - następny slajd
    * przedstawienie się uczestników warsztatu?
    * jakie są oczekiwania uczestników?
    * jaki jest ich poziom wiedzy?

----

================================== ============
O nas
================================== ============
.. image:: img/Dariusz-Duleba.jpg  .. image:: img/Bartosz-Bielicki.jpg
Dariusz Duleba                     Bartosz Bielicki
Software Engineer at Nokia         DevOps Engineer at Huuuge Games
================================== ============

----

Wprowadzenie
------------
O czym i co tak na prawdę będziemy robić?

.. note::
    * 2 bloki
    * jedna przerwa w każdym bloku? (10 min) - ustalimy jeśli będzie potrzebna
    * niejasności i problemy wyjaśniamy na bieżąco

----

Konfigurowanie środowiska
-------------------------
* instalacja VirtualBox'a 5.x/6.x
* tworzenie maszyny wirtulanej na podstawie przygotowanego obrazu - 15 GB (hasło: tw2019)
* rozwiązywanie problemów

----

Zapoznanie się ze środowiskiem
------------------------------
* środowisko działa offline
* wszytskie materiały dostępne są na GitHub
* źródła_prezentacji_
* Ubuntu Mate 18.04.3
* python 3
* PyCharm

----

Zapoznanie się z aplikacją
--------------------------
* aplikacja testowa na podstawie realworld_
* źródła_aplikacji_testowej_
* aplikacja jest skonteneryzowana
* frontend: react + redux
* backend: flask
* db: postgres
* docker-compose
* start-app.sh
* stop-app.sh
* http://127.0.0.1

----

Zapoznanie się z aplikacją
--------------------------
.. image:: img/conduit.png

----

Piramida testów
---------------
.. image:: img/test_pyramid.png
    :width: 600

https://i2.wp.com/ucgosu.pl/wp-content/uploads/2018/09/test_pyramid.png?ssl=1

.. note::
    * Przerwa jeśli będzie potrzebna i czas pozwoli - 10 min

----

Testy integracyjne
------------------
* źródła_testów_integracyjnych_
* z wykorzystaniem nokia_radish_bdd_extensions_

Czego się nauczymy:
===================
#. jak utworzyć wirtualne środowisko python'a
#. jak zaimplementować własnego REST klienta
#. jak wykorzystać klienta i napisać własne testy integracyjne (backend + db)
#. jak wygenerować raport z testów
#. jak debugować testy z użyciem PyCharm

.. note::
    * Jest to dobre wprowadzenie do środowiska przed przejściem do bardziej skomplikowanej implementacji testów, które wykorzystują BDD (gherkin) oraz selenium.

----

Python venv
-----------
.. code-block:: Bash

    $ python3 -m venv .env
    $ . .env/bin/activate
    $ pip install -U pip wheel
    $ pip install -r requirements.txt
    ...
    $ deactivate

----

Conduit REST klient
-------------------
https://github.com/bbielicki/tw2019-app-client/blob/master/conduit/client.py

----

Testy integracyjne
------------------
* rejestracja użytkownika
* powtórna rejestracja użytkownika
* pobranie informacji o zalogowanym użytkowniku
* artykół dostępny dla niezalogowanego użytkownika
* polubienie artykułu

----

Raport z testów
---------------
.. code-block:: Bash

    $ nosetests --with-xunit test.backend

----

Debugowanie testów
------------------

----

Q&A
---
.. note::
    * przerwa obiadowa


.. _źródła_prezentacji: https://github.com/bbielicki/tw2019-workshop
.. _realworld: https://github.com/gothinkster/realworld
.. _źródła_aplikacji_testowej: https://github.com/bbielicki/tw2019-app
.. _źródła_testów_integracyjnych: https://github.com/bbielicki/tw2019-app-client
.. _nokia_radish_bdd_extensions: https://github.com/nokia/radish-bdd-extensions
