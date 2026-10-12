# Studio CRM — Post-Stroke Creators

Gotowy CRM dla jednej osoby sprzedającej strony internetowe. Bez instalacji bibliotek, kont i płatnych usług. Interfejs po polsku; działa na komputerze i telefonie.

## Uruchom od razu, bez hostingu

1. Rozpakuj ZIP do stałego folderu na komputerze.
2. Otwórz index.html w Chrome, Edge lub Firefox.
3. Kliknij „Dodaj firmę”. Wpisz kontakt, etap sprzedaży i datę kolejnej rozmowy.
4. Po rozmowie otwórz firmę, dopisz wynik kontaktu i zapisz.
5. Pod koniec pracy: Kopie i instrukcja → Pobierz kopię JSON.

Zawsze używaj tego samego pliku i profilu przeglądarki. Zachowanie pamięci przy adresach file:// zależy od przeglądarki. Sprawdź zapis jednej próbnej firmy po zamknięciu i ponownym otwarciu przed rozpoczęciem pracy. Przenosząc plik lub przechodząc na adres internetowy, najpierw wyeksportuj JSON, a następnie przywróć go pod nowym adresem.

## Co zawiera

- Firma, osoba kontaktowa, branża / miejscowość, telefon, e-mail i WWW.
- Statusy: Nowa firma, Do kontaktu, Po rozmowie, Oferta wysłana, Negocjacje, Wygrana, W realizacji, Rezygnacja.
- Data kolejnego kontaktu, priorytet, wartość oferty, potrzeby i notatki.
- Historia wyników rozmów oraz zmian statusu i terminu.
- Wyszukiwarka, filtry, widok „Do kontaktu” oraz tablica etapów sprzedaży.
- Kopia JSON i przywracanie całej bazy; CSV do Excela z historią.
- Usuwanie firmy z potwierdzeniem, ochrona przed nadpisaniem bazy zmienionej w innej karcie.

„Do kontaktu” obejmuje aktywne firmy z terminem dziś lub wcześniejszym. Wygrana, W realizacji i Rezygnacja nie wchodzą do tego widoku. Aby ponownie zaplanować sprzedaż dla takiej firmy, zmień status na aktywny. Sama etykieta „Do kontaktu”, bez daty, nie tworzy przypomnienia. Otwarte oferty to suma wartości etapów Oferta wysłana i Negocjacje. Kwoty wpisuj konsekwentnie według własnej zasady netto lub brutto — aplikacja nie oblicza podatków.

## Dane i kopie

Dane są zapisywane w localStorage na danym urządzeniu, w profilu przeglądarki i pod danym adresem strony. Nie są przesyłane do GitHuba ani innych usług. Brak logowania, szyfrowania i synchronizacji między urządzeniami. Dostęp do Twojego profilu przeglądarki oznacza dostęp do bazy.

Usunięcie danych witryny, utrata urządzenia lub tryb prywatny mogą spowodować utratę danych. Pobieraj JSON codziennie i sprawdzaj, czy plik faktycznie znalazł się w Pobranych. JSON odtwarza całą bazę, zastępując obecną — nie scala rekordów. Przed importem pobierz aktualną kopię. Limit importu: 20 MB i 20 000 firm. Dostępne miejsce w pamięci zależy od przeglądarki; przy błędzie zapisu aplikacja nie potwierdza zapisania zmian.

CSV służy do przeglądania danych w Excelu; przywracanie działa tylko z JSON. Kopie zawierają kontakty i notatki — trzymaj je prywatnie. Nie umieszczaj ich w publicznym repozytorium.

Przypomnienia działają w otwartej aplikacji. Nie ma powiadomień w tle, automatycznych telefonów ani e-maili. Tablica etapów otwiera kartę firmy; etap zmienisz w formularzu (bez przeciągania).

Pamięć localStorage jest wspólna dla stron w tym samym origin, także repozytoriów pod tym samym kontem github.io. Uruchamiaj tam tylko zaufany kod. Meta noindex jest prośbą do wyszukiwarek, nie zabezpieczeniem dostępu.

## GitHub — kod i opcjonalna publikacja

Możesz przechowywać kod w swoim repozytorium GitHub. Projekt jest technicznie zgodny z GitHub Pages, lecz zgodność techniczna nie oznacza zgody na każdy sposób wykorzystania usługi.

Dokumentacja GitHub Pages ogranicza użycie jako darmowego hostingu do prowadzenia działalności internetowej, obsługi transakcji komercyjnych oraz komercyjnego SaaS. Nie potwierdzam, że operacyjny CRM sprzedażowy jest dozwolonym przypadkiem. Do pracy od razu możesz korzystać lokalnie. Przed użyciem Pages do tego celu sprawdź warunki lub uzyskaj potwierdzenie GitHub Support.

Źródło, sprawdzone 12.10.2026:
https://docs.github.com/en/pages/getting-started-with-github-pages/github-pages-limits

Techniczna procedura publikacji, jeśli wybrane zastosowanie mieści się w warunkach:

1. Na GitHub kliknij „New repository”. Nazwa: crm-psc.
2. W darmowym GitHub Free Pages wymaga repozytorium Public. Kod oraz pliki w repozytorium będą publiczne.
3. Kliknij „Add file” → „Upload files”. Wgraj index.html bezpośrednio do katalogu głównego, nie ZIP i nie folder zawierający kolejny folder. Możesz dodać INSTRUKCJA.md i .nojekyll. Nie wgrywaj danych klientów.
4. Zatwierdź „Commit changes”.
5. Otwórz „Settings” → „Pages”.
6. W „Build and deployment” ustaw „Source: Deploy from a branch”.
7. Wybierz gałąź main i katalog /(root). Kliknij Save.
8. Po zakończeniu wdrożenia GitHub pokaże właściwy adres. Typowy format: https://TWOJ-LOGIN.github.io/crm-psc/ — to wzór, nie już utworzony adres.
9. Otwórz adres, dodaj próbny kontakt i odśwież stronę. Następnie usuń próbny kontakt. Jeśli masz wcześniejszą bazę lokalną, przywróć kopię JSON.

Źródło procedury:
https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

Sam publiczny adres aplikacji nie udostępnia automatycznie Twojej lokalnej bazy innym odwiedzającym. Nie jest jednak prywatnym panelem chronionym kontem. Każdy odwiedzający korzysta z własnej pamięci przeglądarki.

## Pliki i aktualizacja

index.html — cała aplikacja, bez zewnętrznych bibliotek, fontów, trackerów i połączeń z API.
INSTRUKCJA.md — instrukcja i ograniczenia.
.nojekyll — wyłączenie przetwarzania Jekyll w Pages.
.gitignore — wykluczenie typowych nazw kopii przy pracy przez Git; nie chroni przed ręcznym wgraniem danych przez przeglądarkę.

Przed aktualizacją zawsze wykonaj kopię JSON. Zachowaj stały adres aplikacji. W razie potrzeby odtwórz kopię.
