# Specyfikacja elektronicznej deklaracji członkowskiej Stowarzyszenia Polska Grupa Użytkowników Pythona

>## 1. PANEL KLIENTA

**1.1 Wypełnienie formularza rejestracji**

Pola oznaczone gwiazdką "*" są polami wymaganymi. Bez ich wypełnienia rejestracja członkostwa nie jest możliwa. Wypełnienie pozostałych pól jest dobrowolne.

Widok z formularzem rejestracji uwzględnia następujące sekcje i ich pola:

**Dane podstawowe:**

* Imię* _[input, type=text, maxlength=20]_,
* Nazwisko* _[input, type=text, maxlength=50]_,
* E-mail* _[input, type=email, maxlength=256]_,
* Telefon komórkowy _[input, type=text, maxlength=15]_,
* Data urodzenia* _[input, type=date]_,
* Kraj* _[select, default=Polska]_,
* PESEL* _[input, type=text, maxlength=11]_,
* Płeć* _[select, set={kobieta, mężczyzna, inne}]_,
* Jestem studentem lub osobą uczącą się _[checkbox, default=false]_:
  * Nazwa uczelni, wydziału / szkoły* _[input, type=text, maxlength=25]_,
  * Adres placówki* _[input, type=text, maxlength=50]_.

Pole _E-mail_, _Telefon komórkowy_ oraz _PESEL_ mają być wyposażone w dodatkowe walidatory sprawdzające ich poprawność, zgodnie z przyjętymi normami.

Pole _PESEL_ jest polem obowiązkowym wyłącznie gdy w liście rozwijanej _Kraj_ wybrano "Polska".

Pole _Nazwa uczelni, wydziału / szkoły_ oraz _Adres placówki_ pojawiają się oraz stają polami obowiązkowymi wyłącznie gdy użytkownik zaznaczy _Jestem studentem lub osobą uczącą się_. Odznaczenie tego pola ukrywa je.

**Adres zamieszkania:**

* Ulica* _[input, type=text, maxlength=40]_,
* Numer domu* _[input, type=text, maxlength=5]_,
* Numer mieszkania _[input, type=text, maxlength=5]_,
* Kod pocztowy* _[input, type=text, maxlength=6]_,
* Miejscowość* _[input, type=text, maxlength=20]_,
* Adres do korenspondencji _[checkbox, default=false]_.

Jeżeli pole typu checkbox _Adres do korespondencji_ nie zostało zaznaczone, użytkownik musi wypełnić również formularz "Adres do korespondencji".

**Adres do korespondencji:**

* Ulica* _[input, type=text, maxlength=40]_,
* Numer domu* _[input, type=text, maxlength=5]_,
* Numer mieszkania _[input, type=text, maxlength=5]_,
* Kod pocztowy* _[input, type=text, maxlength=6]_,
* Miejscowość* _[input, type=text, maxlength=20]_,
* Kraj* _[select]_.

**Wymagane zgody:**

* Oświadczam, że znany mi jest statut Stowarzyszenia Polska Grupa Użytkowników Pythona i zobowiązuję się do przestrzegania jego postanowień* _[checkbox, default=false]_,
* Akceptuję Regulamin formularza elektronicznej deklaracji członkowskiej Stowarzyszenia Polska Grupa Użytkowników Pythona* _[checkbox, default=false]_,
* Wyrażam zgodę na przetwarzanie moich danych dla celów związanych z realizacją celów statutowych Stowarzyszenia Polska Grupa Użytkowników Pythona z siedzibą na ul. Madalińskiego 106, 02-506 Warszawa, Polska. Oświadczam, że zostałem poinformowany, iż administratorem moich danych osobowych będzie Stowarzyszenie Polska Grupa Użytkowników Pythona, przysługuje mi prawo dostępu do treści moich danych oraz ich poprawiania oraz usunięcia, a podanie danych osobowych jest dobrowolne, lecz konieczne do świadczenia usługi* _[checkbox, default=false]_,
* Wyrażam zgodę na udostępnienie moich danych współpracującym ze Stowarzyszeniem Polska Grupa Użytkowników Pythona podmiotami w celu niezbędnym do realizacji zadań statutowych* _[checkbox, default=false]_,
* Wyrażam zgodę na przesyłanie mi newslettera Stowarzyszenia Polska Grupa Użytkowników Pythona _[checkbox, default=false]_.

Fragment "statut Stowarzyszenia Polska Grupa Użytkowników Pythona" musi być podlinkowana do strony [1].

Fragment "Regulamin" musi być podlinkowany do strony [2]

Przyciski:

* Wyślij zgłoszenie _[input, type=submit]_

> Po poprawnym wypełnieniu formularza użytkownik otrzymuje komunikat potwierdzający sukces rejestracji o treści:

> Rejestracja deklaracji członkowskiej zakończyła się pomyślnie.

> Na adres e-mail podany w formularzu otrzymasz niebawem decyzję przyjęcia do Stowarzyszenia Polska Grupa Użytkowników Pythona.

> Na chwilę obecną prosimy o zapoznanie się treścią maila zawierającego dane niezbędne do realizacji opłaty składki członkowskiej PLPUG.

Treść maila o którym mowa powyżej, np:

> Witaj,

> Dziękujemy za dokonanie rejestracji członkostwa w Stowarzyszeniu Polska Grupa Użytkowników Pythona.

> Prosimy o dokonanie przelewu na składkę członkowską posługując się poniższymi danymi:

> Nazwa banku: Bank BZWBK

> Numer konta: 02 1090 2590 0000 0001 2993 4371  

> Tytuł przelewu: Imię i nazwisko - składka za <okres> / 2015  

> Kwota: <kwota zależna od statusu członka>  

> Adres: Stowarzyszenie Polska Grupa Użytkowników Pythona, ul. Madalińskiego 106, 02-506 Warszawa, Polska

> Pozdrawiamy,  
> Stowarzyszenie PLPUG

**1.2 Edycja danych konta członka**

Użytkownik może edytować konto w systemie wysyłając maila do Administratora.

Administrator po weryfikacji zgłoszenia nanosi zmiany w koncie w sposób jaki opisano w rozdziale 2.2.

**1.3 Usunięcie konta członka**

Użytkownik może usunąć konto w systemie wysyłając maila do Administratora.

Administrator po weryfikacji zgłoszenia usuwa konto w sposób jaki opisano w rozdziale 2.3.

>## 2. PANEL ADMINISTRATORA

**2.1 Lista zarejestrowanych członków**

Zestawienie tabelaryczne zarejestrowanych członków, w skład którego wychodzą kolumny:

* imię,
* nazwisko,
* e-mail,
* telefon komórkowy,
* miejscowość,
* status przyjęcia _[checkbox, default=false]_,
* zgoda na przesyłanie newslettera,
* data rejestracji.

Ponadto, model użytkownika zarejestrowanego posiada pola:

* status usunięcia (is_active),
* data ostatniej modyfikacji konta,
* komentarz _[textarea]_.

Domyślne sortowanie listingu następuje po polu _Data rejestracji_.

**Wyszukiwarka**

Widok uwzględnia wyszukiwarkę po polach:

* imię,
* nazwisko,
* e-mail,
* telefon komórkowy,
* PESEL.

**Filtry**

Widok uwzględnia filtry względem pól:

* miejscowość,
* płeć,
* status przyjęcia,
* status usunięcia (is_active),
* zgoda na przesyłanie newslettera,
* data rejestracji,
* data ostatniej modyfikacji konta.

Filtry powinny działać także łącznie.

**2.2 Podgląd / Edycja konta zarejestrowanego członka**

Podgląd konta zarejestrowanego członka to odrębny widok uwzględniający jego wszystkie pola, w trybie do edycji (poza ID nadawanym przez bazę danych).

**2.3 Usunięcie konta zarejestrowanego członka**

W przypadku 1.3 lub gdy działania członka Stowarzyszenia naruszają przepisy prawa oraz postanowienia Regulaminu, Statutu oraz Uchwał Stowarzyszenia Polska Grupa Użytkowników Pythona, negatywnie wpływają na dobre imię Stowarzyszenia Administrator, może usunąć konto zarejestrowanego członka.

Usunięcie konta odbywa się dzięki akcji "Usuń zaznaczonych członków" w widoku Lista zarejestrowanych członków.

Usunięcie konta wypełnia dane usuwanego konta losowymi znakami. Dzieje się tak wyłącznie dla pól, które mogą pozwolić na jednoznaczną identyfikację osoby:

* Nazwisko,
* E-mail,
* Telefon komórkowy,
* Data urodzenia,
* PESEL,
* Ulica,
* Numer domu,
* Numer mieszkania,
* Pola formularza Adres do korespondencji.

Pozostałe pola usuwanego konta mogą pozostać niezmienne i posłużą do celów statystycznych.

Ponadto, usunięcie konta powoduje wysłanie do użytkownika e-maila na adres podany w jego koncie, o treści:

>### TODO: Treść maila

**2.4 Przyjęcie członka do Stowarzyszenia PLPUG**

W przypadku, gdy członek zgodnie ze Statutem Stowarzyszenia PLPUG oraz Uchwałą nr 1/2015 uiści na koncie Stowarzyszenia ustaloną opłatę członkowską, Administrator może zmienić mu status przyjęcia na True.

Zmiana statusu odbywa się dzięki akcji "Zmień status zaznaczonym członkom" w widoku Lista zarejestrowanych członków.

Zmiana statusu przyjęcia powoduje wysłanie do użytkownika e-maila na adres podany w jego koncie, o treści:

>### TODO: Treść maila

[1] [https://github.com/plpug/plpug-statut](https://github.com/plpug/plpug-statut)
>### TODO: [2] Link regulaminu
