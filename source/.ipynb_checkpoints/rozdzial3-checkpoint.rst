===============
Rozdział 2
===============

Stworzona aplikacja umożliwia zarządzanie bazą danych, która zajmuje się obsługą serwisową dla wskazanego budynku. Baza zawiera dane odnośnie dostepnego sprzętu oraz to gdzie się znajduje. Można nazwać ją jako inwentaryzację sprzętową. Numer seryjny sprzętu jest kluczem głównym dla tej bazy.

Instrukcja części klienckiej
-------------

Obsługa serwisowa urządzeń części klienckiej odbywa się za pomocą konsoli. Uruchamiamy aplikację za pomocą pliku main.py.
Oto opis każdej opcji menu wraz z odpowiadającymi im plikami:

1. Wprowadź dane (data.py):
-------------
Ta opcja pozwala na wprowadzenie danych do programu. Po uruchomieniu zadaje pytanie czy użytkownik chce dodać nowe dane. Po twierdzącej odpowiedzi, wprowadzamy dane: 
-"Podaj typ urządzenia: "
-"Podaj numer seryjny urządzenia: "
-"Podaj lokalizację urządzenia: "
-"Podaj datę zakupu urządzenia (yyyy-mm-dd): "
-"Czy urządzenie posiada gwarancję?: "
-"Podaj datę przeglądu (yyyy-mm-dd): "
-"Podaj wynik przeglądu: "

2.Zaimportuj dane do SQLite (dataToDB.py):
-------------
Ta opcja odpowiada za importowanie danych wprowadzonych w poprzedniej opcji (data.py) do bazy danych SQLite. Plik dataToDB.py zawiera skrypt, który wykonuje operacje związane z importem danych i zapisuje je w bazie danych SQLite.

3.Zaimportuj dane do PostgreSQL (importToPostgres.py):
-------------
Ta opcja służy do importowania danych wprowadzonych w data.py do bazy danych PostgreSQL. Skrypt importToPostgres.py zajmuje się operacjami związanymi z importem danych i zapisuje je w bazie danych PostgreSQL.

4.Utwórz strukturę bazy danych (createStructure.py):
-------------
Ta opcja odpowiada za utworzenie struktury bazy danych. Skrypt createStructure.py zawiera definicje tabel, relacji i innych obiektów bazy danych, które są potrzebne do prawidłowego funkcjonowania programu.

5. Wstaw dane testowe (testData.py):
-------------
Ta opcja służy do wstawienia danych testowych do bazy danych. Plik testData.py zawiera skrypt, który generuje przykładowe dane testowe i wprowadza je do bazy danych.

6.Wyczyść tabelę (clearDB.py):
-------------
Ta opcja umożliwia wyczyszczenie zawartości wybranej tabeli w bazie danych. Użytkownik zostanie poproszony o podanie nazwy tabeli, a następnie skrypt clearDB.py wykonuje operacje usuwania danych z tej tabeli.

7. Wyczyść wszystkie tabele lub bazę danych (clearDB.py):
-------------
Ta opcja pozwala na wyczyszczenie wszystkich tabel w bazie danych lub całej bazy danych. Użytkownik zostanie poproszony o podanie odpowiedniego parametru (--all lub --drop), a następnie skrypt clearDB.py wykonuje odpowiednie operacje czyszczenia.

8. Wyjdź z programu:
-------------
Opcja kończy działanie programu i zamyka go.