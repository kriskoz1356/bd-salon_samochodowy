# Salon Samochodowy

## 1. Hierarchia funkcji

### 1.1. Zarządzanie pracownikami
* Dodanie pracownika
* Edycja danych pracownika
* Wyszukiwanie pracownika
* Usuwanie pracownika

### 1.2. Zarządzanie klientami
* Dodanie klienta
* Edycja danych klienta
* Wyszukiwanie klienta
* Usuwanie klienta

### 1.3. Zarządzanie samochodami
* Dodanie samochodu
* Edycja właściwości samochodu (rodzaj silnika, model)
* Edycja danych samochodu (np. przebieg, cena)
* Aktualizacja statusu samochodu (np. wyprzedany, wycofany)

### 1.4. Zarządzanie serwisem
* Przyjmowanie samochodu na serwis (konsultacja)
* Identyfikacja poszczególnych napraw (jakie auto, jakie części)
* Przeglądanie historii serwisowej

### 1.5. Zarządzanie sprzedażą
* Rejestracja sprzedaży (kto sprzedał?, co sprzedał?)
* Przygotowanie formalności do sprzedaży (też gwarancyjnych)

### 1.6. System raportów
* Generowanie raportów na podstawie uzyskanych wyników np. ze sprzedaży

## 2. Hierarchia ról
### 2.1. Administrator systemu
jest giga adminem i może wszystko, nawet usunąć katalog `/`
### 2.2. Kierownik salonu
* nadzoruje salon
* analizuje raporty
### 2.3. Sprzedawca
* przyjmuje klienta
* informuje klienta o ofertach, rabatach
* zachęca do wybrania konkretnego modelu
* przyjmuje zamówienie
### 2.4. Serwisant
* konsultuje się z klientem
* wykonuje naprawy
* wykonywanie przeglądów


## 3. Diagram przypadków użycia
### 3.1. Kod do wykorzystania na stronie plantuml.com

```@startuml
left to right direction

actor Administrator
actor Kierownik
actor Sprzedawca
actor "Pracownik serwisu" as Serwisant
actor Księgowa

rectangle "System salonu Mercedes" {
  usecase "Zarządzaj użytkownikami i systemem" as UC1
  usecase "Przeglądaj raporty" as UC2

  usecase "Zarządzaj klientami" as UC3
  usecase "Przeglądaj samochody" as UC4
  usecase "Przygotuj ofertę" as UC5
  usecase "Zarejestruj sprzedaż" as UC6

  usecase "Zarządzaj samochodami" as UC7
  usecase "Rejestruj wizyty serwisowe" as UC8
  usecase "Rejestruj naprawy" as UC9
  usecase "Przeglądaj historię serwisową" as UC10
  usecase "Dokonaj zamówienia potrzebnych części naprawczych" as UC11

  usecase "Sprawdź poprawność zamówień sprzedawców i serwisantów" as UC12
  usecase "Zapewnij archwiziację dokumentacji i finansów" as UC13
  usecase "Nadzoruj przepływ pieniędzy" as UC14
}

Administrator --> UC1
Administrator --> UC2

Kierownik --> UC2
Kierownik --> UC7

Sprzedawca --> UC3
Sprzedawca --> UC4
Sprzedawca --> UC5
Sprzedawca --> UC6

Serwisant --> UC8
Serwisant --> UC9
Serwisant --> UC10
Serwisant --> UC11

Księgowa --> UC12
Księgowa --> UC13
Księgowa --> UC14
@enduml
```

### 3.2. Bezpośredni link do wygenerowanego diagramu
https://www.plantuml.com/plantuml/png/TPFFZjCm4CRlVefHxoknRVVFNj0Yk27GYeeBjy6PjjCcTcGxiXB41R7Y6Qfz36veRoJlXLFiRBlPtk9Vlld6C-EvjGwDgufSvBHqu3GONgqTP6n8EjPA29HE6tYJ5QpOEeFX5Dbx9gEzucqyBqhJK8PUOWIJEuDohm1BnhEj9e0M5ljlL2xvM6vtA-rHY3uhgbLEC5dKrb415dEjAlX0Hb96TWBV141bIQ8DeYzeclO-Qt03LVTOk-q-6nOC37PlGCK-v-UtvuTnTwQXLHuYGw31KXjNHzbKdF3VvapA1Uied9toirXekTPPSfm_4zOhxQeDw2KPr-wYwE9PLjgGTIR8xF-cTezHU7dgVYdjqmsl3fMV1aVFJUtgE17jAQglNrOhB0twLClDgQBNR9qsOOw3RtkV6l_gCEYTtceL0Xei_lxsJ8eHIks2rLTLopN8fjrr3v9ZOja4c8pEZsfVzF-pxay8xx-KxXxQNuDlzpErpii0-lUGdbqu9iVfSJDByeetW4QkFJUCSXCAolIsAaYvSE9WisI5oXvu73s4ZvWrkkzRdxliVjGUohx8TfSrTOgOY-z276qKd9szxl-yIAT23AkMq8XS2V6qVv7DncW-HXTZT2d4iAGHNO_8pOY4IOzGcDcmtubDnsWsHdDnIoghYlmV
