===============
Rozdział 2
===============

Stworzona aplikacja umożliwia zarządzanie bazą danych, która zajmuje się obsługą serwisową dla wskazanego budynku. Baza zawiera dane odnośnie dostepnego sprzętu oraz w którym pomieszczeniu jest zainstalowany. Można nazwać ją jako inwentaryzację sprzętową. 

Instrukcja części klienckiej
--------------------------------

Dane w bazie są zbierane w dwóch tabelach. Pierwsza tabela posiada kolumny takie jak: Typ urządzenia, Numer seryjny, Lokalizacja, Data zakupu, Gwarancja.
W drugiej tabeli zbierane są dane odnośnie przeglądów. Zawiera kolumny: Numer seryjny, Data przeglądu, Wynik przeglądu.
Numer seryjny sprzętu jest kluczem głównym dla tej bazy.
Obsługa serwisowa urządzeń części klienckiej odbywa się za pomocą konsoli. Uruchamiamy aplikację za pomocą pliku main.py.
Oto opis każdej opcji menu wraz z odpowiadającymi im plikami:

1. Wprowadź dane:
------------------------------------
Ta opcja pozwala na wprowadzenie danych do programu. Po uruchomieniu zadaje pytanie czy użytkownik chce dodać nowe dane. Po twierdzącej odpowiedzi, wprowadzamy dane: 
-"Podaj typ urządzenia: "
-"Podaj numer seryjny urządzenia: "
-"Podaj lokalizację urządzenia: "
-"Podaj datę zakupu urządzenia (yyyy-mm-dd): "
-"Czy urządzenie posiada gwarancję?: "
-"Podaj datę przeglądu (yyyy-mm-dd): "
-"Podaj wynik przeglądu: "

Odpowiada za to plik: (data.py)

2.Zaimportuj dane do SQLite:
-------------------------------------------
Ta opcja odpowiada za importowanie danych wprowadzonych w poprzedniej opcji (data.py) do bazy danych SQLite. Plik dataToDB.py zawiera skrypt, który wykonuje operacje związane z importem danych i zapisuje je w bazie danych SQLite.

Odpowiada za to plik: (dataToDB.py)

3.Zaimportuj dane do PostgreSQL:
------------------------------------------------------
Ta opcja służy do importowania danych wprowadzonych w data.py do bazy danych PostgreSQL. Skrypt importToPostgres.py zajmuje się operacjami związanymi z importem danych i zapisuje je w bazie danych PostgreSQL.

Odpowiada za to plik: (importToPostgres.py)

4.Utwórz strukturę bazy danych:
-----------------------------------------------------
Ta opcja odpowiada za utworzenie struktury bazy danych. Skrypt createStructure.py zawiera definicje tabel, relacji i innych obiektów bazy danych, które są potrzebne do prawidłowego funkcjonowania programu.

Odpowiada za to plik: (createStructure.py)

5. Wstaw dane testowe:
---------------------------------------
Ta opcja służy do wstawienia danych testowych do bazy danych. Plik testData.py zawiera skrypt, który generuje przykładowe dane testowe i wprowadza je do bazy danych.

Odpowiada za to plik: (testData.py)

6.Wyczyść tabelę:
----------------------------------
Ta opcja umożliwia wyczyszczenie zawartości wybranej tabeli w bazie danych. Użytkownik zostanie poproszony o podanie nazwy tabeli, a następnie skrypt clearDB.py wykonuje operacje usuwania danych z tej tabeli.

Odpowiada za to plik: (clearDB.py)

7. Wyczyść wszystkie tabele lub bazę danych (clearDB.py):
------------------------------------------------------------
Ta opcja pozwala na wyczyszczenie wszystkich tabel w bazie danych lub całej bazy danych. Użytkownik zostanie poproszony o podanie odpowiedniego parametru (--all lub --drop), a następnie skrypt clearDB.py wykonuje odpowiednie operacje czyszczenia.

Odpowiada za to plik: (clearDB.py)

8. Wyjdź z programu:
--------------------------
Opcja kończy działanie programu i zamyka go.