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

Test cases based on own experience: 

##### Subtask 3

*Why we write test cases?*

Well-written test cases help systematize the testing process. They allow to catch inaccuracies in the documentation, to clarify requirements. They make it easier and faster for a new person in team unfamiliar with the project to perform tests, for example, in case of illness of another tester. This reduces costs and the risk of schedule delays. Test cases are also useful for test automation - they describe the steps that should be automated. Of course, the number of test cases and their level of detail depend on the specifics of a particular project.

