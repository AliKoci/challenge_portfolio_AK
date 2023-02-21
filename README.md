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


    __SELECT * FROM actors__ 
      
    __ORDER BY surname;__

    ![5_1](https://user-images.githubusercontent.com/122850133/218643829-1607fd5c-9bed-4d8d-8768-9f1815c1f3b2.jpg)

2. Wyświetl film, który powstał w 2019 roku.


    __SELECT * FROM movies__ 
      
    __WHERE year_of_production = 2019;__

    ![5_2](https://user-images.githubusercontent.com/122850133/218645395-ce72e1dd-1dfa-4649-a854-445da1f3d067.jpg)

3. Wyświetl wszystkie filmy, które powstały między 1900, a 1999 rokiem.

    
    __SELECT * FROM movies__ 
      
    __WHERE year_of_production BETWEEN 1900 AND 1999;__

   ![5_3](https://user-images.githubusercontent.com/122850133/218646084-f45a1885-bdd8-43e0-a63f-4388e4297933.jpg) 

4. Wyświetl JEDYNIE tytuł i cenę filmów, które kosztują poniżej 7$

    
    __SELECT title, price FROM `movies`__ 
      
    __WHERE price < 7;__

    ![5_4](https://user-images.githubusercontent.com/122850133/218646923-76a95de8-1984-4aad-94f2-ef11cd297178.jpg)

5. Użyj operatora logicznego AND, aby wyświetlić aktorów o actor_id pomiędzy 4-7 (4 i 7 powinny się wyświetlać). NIE UŻYWAJ operatora BETWEEN.


    __SELECT * FROM actors__ 
      
    __WHERE actor_id >=4 AND actor_id<=7;__

    ![5_5](https://user-images.githubusercontent.com/122850133/218647677-5fdce8ee-307d-47fc-8cba-e7a46fa57950.jpg)

6. Wyświetl klientów o id 2,4,6 wykorzystaj do tego warunek logiczny.


    __SELECT * FROM customers__ 
      
    __WHERE customer_id = 2 OR customer_id = 4 OR customer_id = 6;__

    ![5_6](https://user-images.githubusercontent.com/122850133/218648030-538d43af-238b-4b4b-bb66-b2ccc48f8d05.jpg)

7. Wyświetl klientów o id 1,3,5 wykorzystaj do tego operator IN.

    
    __SELECT * FROM customers__
    
    __WHERE customer_id IN (1, 3, 5);__

    ![5_7](https://user-images.githubusercontent.com/122850133/218649266-ffc87c15-9eac-4aa9-a3c7-2e7f64becb72.jpg)

8. Wyświetl dane wszystkich osób z tabeli ‘actors’, których imię zaczyna się od ciągu “An”.

    
    __SELECT * FROM actors__
    
    __WHERE name LIKE 'An%';__

    ![5_8](https://user-images.githubusercontent.com/122850133/218649699-700a1735-823a-4fea-8a4f-b223ba5408a7.jpg)

9. Wyświetl dane klienta, który nie ma podanego adresu email.

    
    __SELECT * FROM customers__
    
    __WHERE email IS NULL;__  

    ![5_9](https://user-images.githubusercontent.com/122850133/218649963-b9f3b3cd-42eb-4b92-996a-712858df004a.jpg)  

10. Wyświetl wszystkie filmy, których cena wynosi powyżej 9$ oraz ich ID mieści się pomiędzy 2 i 8 movie_id.

    
    __SELECT * FROM movies__
    
    __WHERE price > 9 AND movie_id > 2 AND movie_id < 8;__

    ![5_10](https://user-images.githubusercontent.com/122850133/218654322-090c3bbb-824b-4499-9be1-c76ef07fb0b6.jpg)
    

### TASK 6


##### Subtask 1 SQL part 2


11. Popełniłam błąd wpisując nazwisko Ani Miler – wpisałam Muler. Znajdź i zastosuj funkcję, która poprawi mój karkołomny błąd.


    __UPDATE customers__
      
    __SET surname = 'Miler'__
      
    __WHERE surname = 'Muler';__
    
      ![11](https://user-images.githubusercontent.com/122850133/220407011-7dac302a-ee40-41a4-81b0-f48d52afd8a1.jpg)

12. Pobrałam za dużo pieniędzy od klienta, który kupił w ostatnim czasie film o id 4. Korzystając z funkcji join sprawdź, jak ma na imię klient i jakiego ma maila. W celu napisania mu wiadomości o pomyłce fantastycznej szefowej.


    __SELECT movie_id, name, email__ 
      
    __FROM sale__  
    
    __JOIN customers ON sale.customer_id = customers.customer_id WHERE movie_id = 4;__
      
      ![12](https://user-images.githubusercontent.com/122850133/220408750-7807b5bc-7163-4e81-b617-6b15cd0effa3.jpg)

13. Na pewno zauważył_ś, że sprzedawca zapomniał wpisać emaila klientce Patrycji. Uzupełnij ten brak wpisując: pati@mail.com.


    __UPDATE customers__
      
    __SET email = 'pati@mail.com'__
      
    __WHERE name = 'Patrycja';__
      
      ![13](https://user-images.githubusercontent.com/122850133/220409410-225d9491-ed21-412e-8528-776bd66ffbf8.jpg)
      
14. Dla każdego zakupu wyświetl imię i nazwisko klienta, który dokonał wypożyczenia oraz tytuł wypożyczonego filmu. (wykorzystaj do tego funkcję inner join, zastanów się wcześniej, które tabele Ci się przydadzą do wykonania ćwiczenia). 


    __SELECT name AS imię, surname AS nazwisko, title AS tytuł__
      
    __FROM customers INNER JOIN sale ON customers.customer_id=sale.customer_id INNER JOIN movies__ 
      
    __ON sale.movie_id=movies.movie_id;__
      
      ![14](https://user-images.githubusercontent.com/122850133/220410249-0ed21944-8f2b-423e-b16f-e9d9cd68c012.jpg)
      
15. W celu anonimizacji danych, chcesz stworzyć pseudonimy swoich klientów. - Dodaj kolumnę o nazwie ‘pseudonym’ do tabeli customer,- Wypełnij kolumnę w taki sposób, aby pseudonim stworzył się z dwóch pierwszych liter imienia i ostatniej litery nazwiska, np. Natalie Pilling → Nag.


    __ALTER TABLE customers ADD COLUMN pseudonym varchar (3)__ 
      
    __UPDATE customers__ 
      
    __SET pseudonym = CONCAT(LEFT(name,2), RIGHT(surname,1));__
      
     ![15_1](https://user-images.githubusercontent.com/122850133/220411133-4a555c6c-d1c9-45c9-a663-41348e329f56.jpg) 
     
     ![15_2](https://user-images.githubusercontent.com/122850133/220411711-6c421b1c-2586-4c0f-8984-50b4035087d4.jpg)
  
16. Wyświetl tytuły filmów, które zostały zakupione, wyświetl tabelę w taki sposób, aby tytuły się nie powtarzały.      


    __SELECT DISTINCT title__ 
     
    __FROM movies__
    
     
    __JOIN sale ON sale.movie_id = movies.movie_id;__     
     
    ![16](https://user-images.githubusercontent.com/122850133/220415290-d23fdcc3-9640-4929-9e8a-721b40e6cc35.jpg)
    
    
 17. Wyświetl wspólną listę imion wszystkich aktorów i klientów, a wynik uporządkuj alfabetycznie. (Wykorzystaj do tego funkcji UNION)


     __SELECT name__
 
     __FROM actors__

     __UNION__ 

     __SELECT name__
    
     __FROM customers__
    
     __ORDER BY name;__        

     ![17](https://user-images.githubusercontent.com/122850133/220417550-e7772c4b-5428-4ae4-80a4-31a81f177269.jpg)
     
18. Polskę opanowała inflacja i nasz sklepik z filmami również dotknął ten problem. Podnieś cenę wszystkich filmów wyprodukowanych po 2000 roku o 2,5 $ (Pamiętaj, że dolar to domyślna jednostka- nie używaj jej nigdzie).


    __UPDATE movies__ 
    
    __SET price = (price + 2.5)__
    
    __WHERE year_of_production > 2000;__
    
      ![18_1](https://user-images.githubusercontent.com/122850133/220429008-274bf77f-ac37-49cd-96ea-669c91b65eaa.jpg)
      
      ![18_2](https://user-images.githubusercontent.com/122850133/220430908-eb0d14c0-ef41-4a61-8d2a-e164095af527.jpg)
      
19. Wyświetl imię i nazwisko aktora o id 4 i tytuł filmu, w którym zagrał.



    __SELECT name, surname, title__

    __FROM actors__

    __INNER JOIN cast ON cast.actor_id = actors.actor_id__ 

    __INNER JOIN movies ON cast.movie_id = movies.movie_id__
    
    __WHERE actors.actor_id = 4;__    
    
     ![19](https://user-images.githubusercontent.com/122850133/220430986-434997b5-c5d7-4623-bdc3-b22cb1bf4898.jpg)
     
20. A gdzie nasza HONIA!? Dodaj do tabeli customers nową krotkę, gdzie customer_id = 7, name = Honia, surname = Stuczka-Kucharska, email = honia@mail.com oraz pseudonym = Hoa


    __INSERT INTO customers (customer_id, name, surname, email, pseudonym__)

    __VALUES ('7', 'Honia', 'Stuczka-Kucharska', 'honia@mail.com', 'Hoa');__

     ![20](https://user-images.githubusercontent.com/122850133/220431424-c428bc39-8db7-4511-aeb1-09cd67457328.jpg)
     
     
##### Subtask 2

    
   ![wynik_testu](https://user-images.githubusercontent.com/122850133/220435523-e2631128-e3e4-4d43-9377-45ad4b2c6826.jpg)


##### Subtask 3

https://github.com/AliKoci/AlicjaKocinska_Portfolio/blob/main/README.md


