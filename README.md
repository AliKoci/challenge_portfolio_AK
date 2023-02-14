# challenge_portfolio_AK


### TASK 1

##### Subtask 1
10

##### Subtask 3
    
Cześć, testowanie oprogramowania to coś, co chcę robić choćby na emeryturze :wink:
Odkąd skończyłam studia podyplomowe *Tester Oprogramowania*, utrwalam i poszerzam zdobytą wiedzę, wykorzystując różne metody. 

Portfolio Challenge jest jedną z takich okazji - cieszę się na myśl o oczekujących zadaniach, indywidualnym feedbacku i ciekawym testerskim portfolio. 
Wierzę, że challenge zbliży mnie do wymarzonej pracy.

__*Alicja*__


##### Subtask 4

Aplikacja http://scouts-test.futbolkolektyw.pl jest stroną umożliwiającą przeglądanie informacji o zawodnikach (m.in. wiek, waga, wzrost, pozycja, rozegrane mecze itd.). Nazwa wskazuje jako grupę użytkowników łowców talentów, jednak równie interesująca może być dla miłośników piłki nożnej czy dziennikarzy sportowych.

Funkcjonalności aplikacji:
1.	Logowanie/wylogowanie.
2.	Lista graczy.
3.	Możliwość wyszukiwania gracza
4.	Pobranie danych w formacie csv – spodziewałabym się, że pobiorę dane wszystkich graczy, tu pobierane są tylko wyniki z danej strony listy zawodników.
5.	Wydruk listy zawodników.
6.	Wybór wyświetlanych kolumn z danymi graczy.
7.	Filtrowanie graczy według: imienia, nazwiska, wieku, pozycji, klubu, rate
8.	Sortowanie wyników według kolumn: imię, nazwisko, wiek, pozycja, klub, recenzja.
9.	Dodanie gracza.
10.	Edycja gracza.
11.	Dodawanie meczów.
12.	Dodawanie raportów.

Interfejs aplikacji – ubogi, nie przykuwający uwagi, przypomina mi aplikacje z moich czasów szkolnych (czyli ponad 20 lat temu).

Czy aplikacja jest intuicyjna? 
Aplikacja nie jest intuicyjna. Na stronie głównej menu po lewej zawiera tylko pozycje „Strona główna”, „Gracze”, „English” i „Wyloguj”, co sugerowałoby, że możemy tylko operować graczami, zmienić język na angielski i wylogować się.
Znajdująca się obok menu tabliczka „Scouts Panel. Panel zarządzania graczami, meczami i do tworzenia raportów” sugeruje, że tu możemy operować graczami, meczami i raportami. Niestety z tego miejsca jedyny aktywny link to „DEV TEAM CONTACT”, który nie oferuje żadnej z tych funkcjonalności, a jedynie przekierowuje do Slacka.
Listwa u góry strony głównej podzielona jest na 4 kolumny: „Ilość graczy: 1824, Ilość meczy: 289, „Ilość raportów: 394”, „Ilość akcji: 681”. Żaden z tych elementów nie jest klikalny.
Dopiero tabliczka „Linki pomocnicze DODAJ GRACZA” zawiera łącze, które przekierowuje do formularza dodania piłkarza. Formularz zawiera liczne błędy. 
Nie ma opcji usuń gracza (lub trudno ją znaleźć).
W mecze i raporty można wejść dopiero z poziomu podstrony danego zawodnika,
Brak możliwości dodania/usunięcia użytkownika.
Brak informacji o użytkowniku i jego uprawnieniach.

Błędy w polskiej wersji językowej (printscreeny do błędów 1-5 na dysku google https://drive.google.com/drive/folders/10UWeEZQvSHtxEbuA1GruTfIJ7dx_XDRG?usp=share_link):
1. DEV TEAM CONTACT - pojawiają się dwa błędy: po pierwsze jako że testuję polskojęzyczną wersję strony, powinno być "KONTAKT" zamiast "CONTACT"; po drugie odnośnik "DEV TEAM CONTACT" sugeruje przekierowanie do formularza kontaktu lub listy dostępnych kanałów komunikacji (np. e-mail, telefon, FB itp.), tu zaś przekierowuje do logowania do aplikacji Slack, a po zalogowaniu po prostu na kanał general.
2. Ponownie błąd - brak tłumaczenia na język polski: po kliknięciu na "Gracze" pojawia się u góry możliwość wyszukiwania gracza, brak tłumaczenia "Search" -> "Wyszukaj"
3. Wyszukiwanie – brak sprecyzowania po czym można wyszukiwać; lista wyników wyszukiwania działa błędnie: pierwsza strona jest ok, przy naciśnięciu strzałki przekierowującej na następną stronę wyników pojawiają się już wszyscy gracze (uwaga: w niektórych wyszukiwaniach działa poprawnie, temat do dokładniejszego sprawdzenia w czasie kolejnej sesji eksploracyjnej).
4. Możliwość dodawania wielokrotnie tego samego gracza z identycznymi danymi.
5. Niepoprawne filtrowanie według wieku.
6. Brak tłumaczenia w filtrach: „Age” – „Wiek”, „Rate” – „Recenzja” (tu dodatkowy problem słowo „rate” nie ma tłumaczenia „recenzja”, dopiero po zobaczeniu wyników filtrowania można określić, że to o to chodzi; z kolei znając sposób oceny piłkarzy określenie np. „współczynnik” byłoby lepszym do nazwy kolumny zamiast „recenzja”.
7. Formularz dodawania gracza:
- na podstronie „Dodaj gracza” w formularzu są 4 pola oznaczone gwiazdką („Imię”, „Nazwisko”, „Data urodzenia”, „Dominująca pozycja” – doświadczenie z formularzami internetowymi pozwala się domyślić, że są to pola obowiązkowe, ale brak takiego wyjaśnienia; dopiero próba dodania gracza bez tych danych  skutkuje komunikatem „Please fill out this field” (znów brak tłumaczenia!) i zaznaczeniem na czerwono brakujących pól;
- brak tłumaczenia głównych przycisków u dołu strony: „Submit” -> „Wyślij” oraz „Clear” -> „Wyczyść”;
- wymagane pola „Imię”, „Nazwisko”, „Dominująca pozycja” można wypełnić dowolnymi znakami (także pojedynczą spacją) – powinny być dozwolone tylko litery;
- nie można dodać gracza z błędnym formatem email (tzn. bez @), jednak oprócz komunikatu „Nie udało się dodać gracza” nie ma żadnej wskazówki, co poszło nie tak;
- bez problemu została zaakceptowana ujemna waga gracza (-100 nie wiadomo czego – kg, funtów, gram? - nie ma podanej jednostki, w jakiej ma być podana waga), ujemny wzrost (-222 cm) oraz przyszła data urodzenia (02/18/2026; udało się również dodać gracza urodzonego w 1 roku naszej ery). Tu jeszcze jedna uwaga – chociaż format mm/dd/rrrr jest dopuszczalny, w Polsce preferowany jest format dd/mm/rrrr;
- w polu „Telefon” można dodać dowolne znaki (powinny być dozwolone tylko cyfry), podobnie w polu „Języki” (tu tylko litery);
- w przypadku wypełnienia pól „Wzrost” i „Waga” znakami innymi niż cyfry pojawia się komunikat (dopiero przy próbie dodania gracza) „Please enter a number” (brak tłumaczenia!), kursor trafia w odpowiednie pole, jednak nie jest ono wyróżnione innym kolorem, przez co trudno zauważyć, o które chodzi;
- pole „Województwo” zawiera rozwijaną listę polskich województw, nie można wpisać nic z klawiatury, a nigdzie nie ma informacji, że program ogranicza się tylko do Polski;
- ulepszenie: wskazana rozwijana lista w polach „Poziom rozgrywek”, „Główna pozycja”, „Alternatywna pozycja”, „Dodaj język”.
8. Można edytować dane dowolnych graczy, nie tylko tych dodanych przez siebie.

*Uwagi do następnej sesji eksploracyjnej: przetestować dodawanie raportów i meczów*.


### TASK 2 https://drive.google.com/drive/folders/1Wlex-hjNYMkfRaSQIz_YeHg1Q4oiGR0u?usp=share_link

##### Subtask 1
Test cases based on User Story: https://docs.google.com/spreadsheets/d/1fCXSx9H1WHpmUckkFsxQXEN7WVACTqxX/edit?usp=share_link&ouid=103988214272257934032&rtpof=true&sd=true


##### Subtask 2

Test cases based on own experience: https://docs.google.com/spreadsheets/d/1tB4qH8yE8Z8vlBmzYdgiMLMlWVJHy-dD/edit?usp=sharing&ouid=103988214272257934032&rtpof=true&sd=true


##### Subtask 3

*Why we write test cases?*

Well-written test cases help systematize the testing process. They allow to catch inaccuracies in the documentation, to clarify requirements. They make it easier and faster for a new person in team unfamiliar with the project to perform tests, for example, in case of illness of another tester. This reduces costs and the risk of schedule delays. Test cases are also useful for test automation - they describe the steps that should be automated. Of course, the number of test cases and their level of detail depend on the specifics of a particular project.

### TASK 4 https://drive.google.com/drive/folders/1g0il0nEQ0cTZXfTFLyqGU97zcokEm0QL?usp=sharing

##### Subtask 1 and 2

Exploratory testing and bug reporting: 
https://drive.google.com/drive/folders/1Gcf53hQU0Rd3Md0SX0yBnrfDwtC29Iku?usp=sharing
https://docs.google.com/spreadsheets/d/1IpL74dSupXD_j2nwyPPNb39hevhDRuo_/edit?usp=sharing&ouid=103988214272257934032&rtpof=true&sd=true


##### Subtask 3

Do czego służy ta aplikacja? Jaki jest cel tej aplikacji?

Aplikacja OLX jest mobilną wersją strony internetowej portalu ogłoszeń. Obejmuje oferty kupna/sprzedaży, wymiany, poszukiwania/oferowania pracy, usług, „oddam za darmo”.
Kto ma być użytkownikiem końcowym aplikacji? 
Aplikacja przeznaczona jest dla klientów indywidulanych i firmowych, rozróżnienie tych dwóch typów użytkowników widoczne jest już w momencie rejestracji, gdy trzeba wybrać jedną z opcji. 

Czy aplikacja jest user friendly?  Jak byś usprawnił aplikację?

Aplikacja przyjazna użytkownikowi powinna być przyjemna i łatwa w obsłudze dla różnych użytkowników. Na plus zaliczam poprawne wyświetlanie w pionie i poziomie, możliwość wyboru trybu ciemnego i jasnego, duże ikony kategorii, ogólną czytelność wyświetlanej strony i szybkość działania. Jeśli chodzi o dostęp do najczęstszych funkcji, to również mam mieszane uczucia. Z jednej strony są  popularne odnośniki na dole strony – strona główna, ulubione, dodaj, wiadomości, konto, ale… Strona główna opisana jest błędnie jako szukaj, brakuje odnośnika szukaj (jest co prawda u góry strony), a odnośnik konto przekierowuje do mnóstwa innych odnośników, z których jeden z najważniejszych – ustawienia – jest niemal na samym dole. Odnośniki pomoc, regulamin, polityka prywatności przekierowują do przeglądarki mobilnej, co wydłuża czas odnalezienia potrzebnych treści. Trudno znaleźć funkcję stworzenia profilu zawodowego kandydata i dołączenia CV – są dostępne dopiero po przewinięciu części opcji w koncie. Brakuje również dostępnego kontaktu z właścicielami/twórcami portalu.

Jakie dostrzegasz różnice pomiędzy testowaniem aplikacji internetowej, a natywnej?

Różnice wynikają m.in. z różnego sposobu korzystania z komputera/laptopa a smartfona/tabletu. Są na pewno kosztowniejsze i bardziej czasochłonne ze względu na zalecane testowanie na różnych urządzeniach – emulatory nie do końca zastępują testowanie na rzeczywistym urządzeniu. Ze względu na postępującą cyfryzację i uzależnienie możliwości skorzystania z różnych usług od użycia aplikacji mobilnej szczególnego znaczenia nabierają testy dostępności.

### TASK 5


##### Subtask 3


1. Wyświetl tabelę actors w kolejności alfabetycznej sortując po kolumnie surname.


    __SELECT * FROM actors ORDER BY surname__

    ![5_1](https://user-images.githubusercontent.com/122850133/218643829-1607fd5c-9bed-4d8d-8768-9f1815c1f3b2.jpg)

2. Wyświetl film, który powstał w 2019 roku.


    __SELECT * FROM movies WHERE year_of_production = 2019__

    ![5_2](https://user-images.githubusercontent.com/122850133/218645395-ce72e1dd-1dfa-4649-a854-445da1f3d067.jpg)

3. Wyświetl wszystkie filmy, które powstały między 1900, a 1999 rokiem.

    
    __SELECT * FROM movies WHERE year_of_production BETWEEN 1900 AND 1999__

   ![5_3](https://user-images.githubusercontent.com/122850133/218646084-f45a1885-bdd8-43e0-a63f-4388e4297933.jpg) 

4. Wyświetl JEDYNIE tytuł i cenę filmów, które kosztują poniżej 7$

    
    __SELECT title, price FROM `movies` WHERE price < 7__

    ![5_4](https://user-images.githubusercontent.com/122850133/218646923-76a95de8-1984-4aad-94f2-ef11cd297178.jpg)

5. Użyj operatora logicznego AND, aby wyświetlić aktorów o actor_id pomiędzy 4-7 (4 i 7 powinny się wyświetlać). NIE UŻYWAJ operatora BETWEEN.


    __SELECT * FROM actors WHERE actor_id >=4 AND actor_id<=7__

    ![5_5](https://user-images.githubusercontent.com/122850133/218647677-5fdce8ee-307d-47fc-8cba-e7a46fa57950.jpg)

6. Wyświetl klientów o id 2,4,6 wykorzystaj do tego warunek logiczny.


    __SELECT * FROM customers WHERE customer_id = 2 OR customer_id = 4 OR customer_id = 6__

    ![5_6](https://user-images.githubusercontent.com/122850133/218648030-538d43af-238b-4b4b-bb66-b2ccc48f8d05.jpg)

7. Wyświetl klientów o id 1,3,5 wykorzystaj do tego operator IN.

    
    __SELECT * FROM customers WHERE customer_id IN (1, 3, 5)__

    ![5_7](https://user-images.githubusercontent.com/122850133/218649266-ffc87c15-9eac-4aa9-a3c7-2e7f64becb72.jpg)

8. Wyświetl dane wszystkich osób z tabeli ‘actors’, których imię zaczyna się od ciągu “An”.

    
    __SELECT * FROM actors WHERE name LIKE 'An%'__

    ![5_8](https://user-images.githubusercontent.com/122850133/218649699-700a1735-823a-4fea-8a4f-b223ba5408a7.jpg)

9. Wyświetl dane klienta, który nie ma podanego adresu email.

    
    __SELECT * FROM customers WHERE email IS NULL__  

    ![5_9](https://user-images.githubusercontent.com/122850133/218649963-b9f3b3cd-42eb-4b92-996a-712858df004a.jpg)  

10. Wyświetl wszystkie filmy, których cena wynosi powyżej 9$ oraz ich ID mieści się pomiędzy 2 i 8 movie_id.

    
    __SELECT * FROM movies WHERE price > 9 AND movie_id > 2 AND movie_id < 8__

    ![5_10](https://user-images.githubusercontent.com/122850133/218654322-090c3bbb-824b-4499-9be1-c76ef07fb0b6.jpg)
