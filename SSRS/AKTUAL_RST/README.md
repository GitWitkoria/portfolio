<h2 style="text-align: center;">Lista aktualnych zgłoszeń</h2>


**Opis:**
Raport prezentuje zestawienie wszystkich aktualnych zgłoszeń wraz z możliwością przechodzenia do szczegółowych danych. Umożliwia filtrowanie wyników za pomocą parametru Siedziba z obsługą multi-select oraz funkcją „Select All”.
Raport oparty jest na wcześniej przygotowanych widokach w SSMS z systemu testowego, które agregowały dane i upraszczały logikę raportu.

**Nawigacja między raportami (drill-through)**
•	Numer zgłoszenia – link prowadzący do szczegółowego widoku zgłoszenia, zawierającego:
o	tabelę wykonanych prac,
o	listę wydanych materiałów,
o	zaplanowane czynności.
•	Kod obiektu – link przechodzący do raportu z historią obiektu, zawierającego:
o	tabelę wszystkich przeszłych zleceń,
o	wykres liczby zleceń w podziale na miesiące,
o	wykres liczby zleceń w podziale na typy.
**Funkcjonalności raportowe**
•	Sortowanie wyników po każdej kolumnie
•	Dynamiczne filtrowanie po siedzibach
•	Przejrzysty układ tabelaryczny (tablix)
•	Projekt dostosowany do wyświetlania po publikacji (SSRS web viewer)
•	Pełna obsługa eksportu do Excel (z zachowaniem tabel i struktury danych)
•	Raport pełnił rolę narzędzia operacyjnego do bieżącej kontroli zgłoszeń i szybkiej nawigacji po historii obiektów.

**Zdalna publikacja**
Na GitHub zostały umieszczone wyłącznie zrzuty ekranu z pełną anonimizacją danych, bez oryginalnych plików .rdl z uwagi na wrażliwe dane.

**Wizualizacja raportu**
1. ![Strona główna raportu](images/AKTUAL_RST_1.jpg)
2. ![Szczegóły zgłoszenia](images/AKTUAL_RST_2.jpg)
3. ![Historia obiektu](images/AKTUAL_RST_3.jpg)

