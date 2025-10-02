<h2 style="text-align: center;">Raport obecnych wyników firmy</h2>

<h3>Co zawiera raport?</h3>

Raport zawiera 3 zakładki znajdujące się w górnym menu: Dashboard (Pulpit nawigacyjny), Sales insights (Analiza sprzedaży), Time Analysis (Tredny i prognoza). 


<h3>Jak powstał raport?</h3>

W tym raporcie mój asystent AI wcielił się w rolę klienta menedżera (średniego szczebla w firmie handlowej) i przedstawił mi swoje oczekiwania wobec raportu w Power BI przygotowanego na bazie hurtowni **AdventureWorksDW2019**. Raport miał być użyteczny, intuicyjny i przypominać mini-aplikację (max 3 zakładki). 
Zależało mi, aby pierwsza strona zawierała kluczowe wskaźniki a pozostałe strony - szczegóły. Całość miała sprawiać wrażenia mini-aplikacji po której mógłby się poruszać klient korzystając, m.in. z:
- wykresu z drill through prowadzącym do faktur,
- wykresu z zastosowaniem hierarchii i drill down dla różnych poziomów szczegółowości,
- przycisków, które zmieniają wykres na stronie.

<h3>Odbiorca raportu</h3>

Raport jest przeznaczony dla menedżerów sprzedaży i marketingu. Potrzebują oni szybkiego podglądu bieżących wyników firmy oraz możliwości pogłębienia analizy (drill-through do szczegółów).
Pytania, na które raport ma odpowiadać: <br>
• Jak wyglądają aktualne wyniki sprzedaży w poprzednich lat? <br>
• Które produkty, kategorie i regiony generują największy przychód i marżę? <br>
• Którzy klienci są najważniejsi i jak kształtuje się ich rentowność? <br>
• Jakie są trendy sprzedażowe i czy widzimy sezonowość? <br>

<h3>Kluczowe KPI i wizualizacje</h3>

• KPI:  Zysk brutto, % Marży, Ilość zamówień, Średnia wartość zamówienia. <br>
• Wizualizacje: wykres liniowy (trendy), mapa (regiony sprzedaży), heatmap (produkty), tabelki z możliwością drill-through do faktur/klientów. 



<h3>Krok 1 – Przygotowanie szablonu tła raportu</h3>

Szablon przygotowałam za pomocą narzędzi graficznych m.in. Figma i GIMP.


<h3>Krok 2 – Przygotowanie źródła raportu oraz nadanie relacji pomiędzy widokami</h3>

1. **Pobieram dane** do Power BI za pomocą funkcji „Pobierz dane” -> SQL Server i łączę się z hurtownią AdventureWorksDW2019.
2. W MS SQL Server tworzę odpowiednie widoki, aby nie musieć wykonywać odatkowych operacjiw Power Query. Utworzyłam widok faktów vw_FactInternetSales_Denorm oraz 4 widoki wymiarów: vw_DimProduct, vw_DimCustomer, vw_DimSalesTerritory, vwDimDate i jedną tabelę przechowującą wszystkie miary.
3. Nadaję relacje zgodnie ze schematem gwiazdy.

![Zastosowany schemat gwiazdy](Images/StarSchema.png)
   

<h3>Krok 3 – Utworzenie stron raportu z wysuwanym panelem filtrów</h3>

Zakładka 1: Dashboard menedżerski (dashboard) <br>

👉 Cel: szybki podgląd bieżących wyników <br>

• Kafle KPI (Zysk brutto, % Marży, Ilość zamówień, Średnia wartość zamówienia).  <br>
• Wykres liniowy: trend sprzedaży. <br>
• Top 5 produktów wg przychodu (kolumnowy). <br>
• Mapa sprzedaży po regionach (kontynent/kraj/stan). <br>
• Informacja o obecnym wyniku sperzedaży do 2014 roku. <br>
• Wysuwane filtry za pomocą toggle switch: rok, region, kategoria produktu. <br>

Zakładka 2: Analiza sprzedaży (sales insights) <br>

👉 Cel: pogłębiona analiza sprzedaży wg produktów i klientów  <br>

• Macierz (Kategoria produktu → Produkt → Kwota sprzedaży, Zysk, Marża) w podziela na lata.  <br>
• Heatmap (region × produkt = sprzedaż).  <br>
• Wykres słupkowy: Top 10 klientów wg przychodu z możliwością drill-through do faktur, KPI z wartością sprzedaży, zyskiem brutto, ilością zamówień i trendem sprzedaży w czasie.  <br>
• Segmentacja klientów: nowi vs powracający. <br>
• Wysuwane filtry za pomocą toggle switch: rok, region, kategoria produktu. <br>

Zakładka 3: Trendy i prognoza (time analysis) <br>

👉 Cel: spojrzenie długoterminowe i przewidywania <br>

• Wykres liniowy: sprzedaż miesięczna z trendline i prognozą na kolejne 3 lata.  <br>
• Sezonowość: porównanie sprzedaży rok do roku. <br>
• Wykres key influencers z analizą całkowitej sprzedaży w opraciu o region, kategorię produktu, płeć konsumenta, rok kalendarzowy, miesiąc. •	Wysuwane filtry za pomocą toggle switch: rok, region, kategoria produktu. <br>

<h3>Krok 4 – Wnioski na podstawie raprotu</h3>

👉 Na podstawie przygotowanego raportu w Power BI można zauważyć kilka kluczowych trendów: 

📈 Rok 2013 był najlepszym okresem sprzedażowym dla firmy. <br>
🗓️ W większości analizowanych lat czerwiec wyróżniał się jako miesiąc o najwyższej sprzedaży. <br>
🚴 Rowery to kategoria dominująca pod względem wartości sprzedaży – szczególnie w Australii oraz w regionie Southwest. <br>
👥 Analiza klientów wskazuje, że w badanym okresie pojawia się więcej nowych klientów niż powracających, co sugeruje skuteczność w pozyskiwaniu nowych odbiorców. <br>


<br> <br> 
<h3>WIZUALIZACJA RAPORTU</h3>

1. Strona pierwsza raportu
   ![Strona pierwsza raportu](Images/Dash1.png)
2. Strona druga raportu
   ![Strona druga raportu](Images/Dash2.png)
3. Widok strony po przejściu drill through dla danego klienta
   ![Widok strony po przejściu drill through](Images/Dash3.png)
4. Strona trzecia raportu
   ![Strona trzecia raportu](Images/Dash4.png)
5. Strona trzecia raportu z wysuniętym panelem filtrów
   ![Strona trzecia raportu z filtrem](Images/Dash5.png)
   
   
