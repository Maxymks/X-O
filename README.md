# X-O
# Kółko i Krzyżyk – README

To jest prosty skrypt gry „Kółko i Krzyżyk” napisany w JavaScript. Gra działa na planszy 3x3 i pozwala grać dwóm osobom na zmianę.

## Jak działa gra?

Po uruchomieniu skryptu pojawia się plansza z 9 polami. Gracze klikają na pola, żeby postawić swój znak (X lub O). Gra informuje, czyja jest tura, kto wygrał, albo czy jest remis. Można też zresetować grę przyciskiem.

## Jakie są tutaj funkcje?

- **createBoard()** – Tworzy planszę do gry, czyli 9 pól, na które można klikać.
- **handleCellClick(event)** – Obsługuje kliknięcie w pole. Ustawia znak gracza, sprawdza wygraną lub remis, zmienia gracza.
- **checkWin()** – Sprawdza, czy ktoś wygrał, porównując układ na planszy z możliwymi zwycięskimi kombinacjami.
- **drawWinningLine()** – Rysuje linię na planszy, która pokazuje zwycięski układ.
- **resetGame()** – Czyści planszę i ustawia wszystko od nowa, żeby można było zagrać jeszcze raz.

## Jakie są tutaj zmienne globalne?

- **board** – Element HTML, w którym jest plansza.
- **messageTur** – Element HTML, w którym wyświetla się informacja o turze lub wyniku.
- **resetBtn** – Przycisk do resetowania gry.
- **currentPlayer** – Zmienna, która mówi, czy teraz gra X czy O.
- **gameBoard** – Tablica, która przechowuje aktualny stan planszy.
- **winningCombo** – Tablica, która przechowuje zwycięską kombinację pól.
- **gameOver** – Zmienna, która mówi, czy gra się skończyła.


