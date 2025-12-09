<h2 style="text-align: center;">Statystyka zgłoszeń</h2>



<h3>Opis</h3>
Raport prezentuje przekrojową analizę zgłoszeń w wybranym okresie. Został zaprojektowany zarówno do podglądu po publikacji na serwerze SSRS, jak i do eksportu do PDF, co umożliwiało szybkie udostępnianie raportu innym użytkownikom.<br>
Raport oparty jest na wcześniej przygotowanych widokach w SSMS z systemu testowego, które agregowały dane i upraszczały logikę raportu.


<h3>Parametry wejściowe</h3>
•	Data od / Data do<br>
•	Status zgłoszenia – multi-select + select all<br>
•	Typ zgłoszenia – multi-select + select all<br>
•	Zgłaszający – multi-select + select all<br>
•	Kod obiektu – multi-select + select all<br>
•	Siedziba – multi-select + select all<br>
Uwaga: Wszystkie parametry poza datami były domyślnie wypełnione wartościami wskazanymi przez klienta.

<h3>Rozwijane parametry raportu</h3>
•	Parametry można rozwijać przyciskiem „+” i ukrywać przyciskiem „−”, co ułatwia kontrolę widoku raportu.

<h3>Wykresy i wizualizacje</h3>
•	Liczba zgłoszeń w podziale na obiekty<br>
•	Liczba zgłoszeń w podziale na typy zgłoszeń<br>
•	Liczba zgłoszeń w podziale na zgłaszających<br>
•	Pełna lista zgłoszeń w tabeli spełniająca wybrane parametry wejściowe<br>

<h3>Funkcjonalności raportowe</h3>
•	Raport dostosowany do publikacji na serwerze SSRS (web viewer)<br>
•	Obsługa eksportu do PDF<br>
•	Możliwość filtrowania danych przez wszystkie parametry wejściowe<br>
•	Przejrzysty układ tabelaryczny oraz wykresy wspierające szybkie podejmowanie decyzji operacyjnych<br>


<h3>Zdalna publikacja</h3>
Na GitHub umieszczono wyłącznie zrzuty ekranu z pełną anonimizacją, bez plików .rdl z uwagi na wrażliwe dane.

<h3>Wizualizacja raportu</h3>

![Strona główna raportu](images/STAT_ZGLOSZEN_1.png)
![Strona główna raportu](images/STAT_ZGLOSZEN_2.png)
![Strona główna raportu](images/STAT_ZGLOSZEN_3.png)


