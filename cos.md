# Plik
Zaawansowany system garażowy NUI oparty na netr_garages.


# Opis
Wiem, że można go lepiej zoptymalizować, ale nie mam teraz na to czasu. Może w przyszłości to zrobię.

Zacznijmy od config. W Config.Garage ustawiasz garaże dla graczy. „Marker” to miejsce, w którym znajduje się garaż. „Blip” określa, czy blip jest widoczny na mapie. W tabeli „Widoczne” możesz wyznaczyć zadania, które mogą korzystać z wybranego garażu.

W Config.Impound wyznaczasz miejsce do holowania pojazdów gracza na mapie - jest ono oznaczone czerwoną ciężarówką.

W Config.PoliceImpound możesz ustawić miejsce dla parkingu policyjnego, który jest niewidoczny na mapie.

W Config.SetSubowner wyznaczasz miejsce do ustawiania współwłaścicieli pojazdów graczy.


# Jak to wszystko działa
Config.Garage nie jest nawet trudny. Możesz przechowywać naprawione pojazdy -> wartość, którą możesz określić w Config.MinimumHealth. Przechowujesz i ciągniesz pojazdy w jednym markerze i to wszystko, co musisz wiedzieć.

Znacznik zatrzymania odpowiada za holowanie pojazdów, które nie znajdują się na parkingu policyjnym. Oznacza to, że jeśli ktoś ukradł ci samochód lub zostałeś wyrzucony z gry, a samochód zniknął, w tym miejscu będziesz mógł odzyskać swój pojazd. Cena, którą możesz określić w Config. Jeśli pojazd jest już na mapie, zostanie usunięty, jeśli nikogo nie ma w środku.

Przede wszystkim, jeśli chcesz, aby Impuls Policyjny działał poprawnie, musisz wykonać polecenie odpowiedzialne za przeniesienie pojazdu na parking policyjny, np. https://pastebin.com/f6RLRs8j
Jeśli więc uczyniłeś ją użyteczną, wszystko, czego potrzebujesz, to praca policyjna zwana „policją” - tylko z tą pracą możesz użyć znacznika. Tam możesz zobaczyć pojazdy o stanie = 2 w swojej bazie danych. Jest to bardzo przydatne w odgrywaniu ról.

Ostatnią opcją w moim systemie garażowym jest ustawienie współwłaścicieli, podwładnych lub jakkolwiek to nazwiesz. Wchodzisz w znacznik i musisz wejść na tablicę rejestracyjną pojazdu, w przeciwnym razie nie będziesz w stanie ustawić ani zarządzać podległymi. Następnie, gdy jesteś właścicielem tego samochodu (właściciel_typ = 1 w tabeli Own_vehicles), możesz ustawić nowego podrzędnego (najbliższego gracza) lub zarządzać bieżącymi podległymi (usunąć je). Podrzędne są określone przez 0 w kolumnie typ_właściciela. Maksymalna liczba lub podrzędny, który możesz określić w Config. Jeśli nie chcesz zezwalać współwłaścicielom na sprzedaż samochodów, musisz podać to w częściach kodu, które je zawierają.


# Instalacja
Przeciągnij i upuść. Musisz także mieć zainstalowany es_extended. Nie zapomnij o pliku .sql!


# Filmy
https://medal.tv/clips/19162177/d1337nlInqvA - Holowanie pojazdów

https://medal.tv/clips/19162163/d1337biAo8nn - Policyjny Parking

https://medal.tv/clips/19162146/d1337tuUd68m - Ustalanie współwłaścicieli

