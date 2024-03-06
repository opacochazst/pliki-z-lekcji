T: Sieć to nie tylko internet, czyli poznajemy topologię sieci komputerowych.

Wyróżniamy topologie fizyczne i logiczne sieci.

Topologia fizyczna określa, w jaki sposób urządzenia i hosty są ze sobą połączone. 
Topologia logiczna określa sposób przesyłania danych między urządzeniami sieciowymi i hostami.

Wyróżniamy następujące topologie fizyczne:

- topologia magistrali (bus) - charakteryzuje się tym, że wszystkie urządzenia podłącza sie od wspólnego medium transmisyjnego. Medium transmisyjnym był kabel koncentryczny.
	Zalety: niewielki koszt wdrożenia (brak urządzeń dostępowych).
	Wady: mała przepustowość, podatność na awarię sieci (przerwanie magistrali powoduje brak dostepu do internetu).

- topologia pierścienia - każde urządzenie podłączone jest z dwoma sąsiadami, tworzące zamknięty krąg.
	Zalety: Stosowanie małej ilości okablowania, niewielki koszt wdrożenia.
	Wady: Podatność na awarię - przerwanie medium transmisyjnego lub awaria hosta spowoduje brak dostępu do internetu.

- topologia gwiazdy - urządzenia podłączone są do centralnego punktu, stanowiącego punkt dostępu do sieci (router lub switch).
	Zalety: Prosta w zaprojektowaniu, łatwa administracja siecią, odporna na awarie.
	Wady: Koszt rozbudowy sieci (wymagane dodatkowe urządzenia), ilość hostów z dostępem do internetu przewodowo zależna od urządzeń sieciowych.  

- topologia gwiazdy rozszerzonej
	Zalety: możliwość łaczenia ze sobą mniejszych sieci, ograniczenie liczby kabli między głównym przełącznikiem a znacznie oddalonymi grupai komputerów i urządzeń. 
	Wady: konieczność rozbudowy infrastruktury o dodatkowe urządzenia, zwiększenie poboru energii przez infrastrukturę, konieczność przygotowania odpowiednich miejsc na dodatkowe przełączniki.

- topologia P2P-network (peer-to-peer (każdy z każdym))

Topologie fizyczne:

- topologia punkt-punkt - dane przesyłane są od jednego urządzenia do drugiego bezpośrednio np. komputer z przełącznikiem, lub pośrednio np. dwa routery. Topologie punkt-punkt
	wykorzystuje się w topologii fizycznej gwiazdy.

- topologia logiczna przekazywania żetonu (token passing) - dane przekazywane są kolejno do urządzeń połączonych w sieć. Urządzenie, które otrzyma porcję danych, analizuje
	czy są one kierowane do niego czy też nie. Jeśli dane nie sa do niego adresowane, przekazuje je dalej, do sąsiedniego urządzenia. W taki sposób, dane przesyłane są 
	przez wszystkie urządzenia występujące pomiędzy urządzeniem źródłowym, a docelowym. 

- topologia logiczna wielodostępowa.
_____________________________________________________________________________________________________________________________________________________________________________

T: Model sieciowy ISO i OSI.

(Open System Interconnection Reference Model)

Model ten został stworzony w celu normalizacji zasad komunikacji w sieci. Model ten został przygotowany z myślą o tworzeniu tak zwanego systemu otwartego, który nie będzie należał do żadnej zamkniętej sieci.
Model ten jest modelem poglądowym (teoretycznym) i został podzielony na siedem warstw:

7. warstwa aplikacji - umożliwia komunikacje z użytkownikiem (strony WWW), poczta elektroniczna.

6. warstwa prezentacji - zajmuje się konwersją danych i definiowaniem formatu - odpowiada również za odpowiednie kodowanie danych (szyfrowanie) na urządzeniu źródłowym i ich odkodowanie na urządzeniu docelowym.

5. warstwa sesji - zarządza sesjami użytkowników korzystających np. ze stron WWW czy komunikacji video.

4. warstwa transportu - głównym zadaniem jest sprawna obługa komunikacji pomiędzy urządzeniami. W warstwie tej dane dzielone są na mniejsze części (segmentowanie), a następnie opatrywane są dodatkowymi informacjami, m.in.
   nadawane są numery porządkowe, które pozwalają na przydzielenie do właściwej aplikacji.

3. warstwa sieci - segmenty danych są wzbogacane o nagłówki w sieci zawierające adres IP, źródła i celu. W ten sposób tworzy się pakiety danych. Głównym zadaniem warstwy sieciowej jest wybieranie najlepszej drogi od nadawcy
   do odbiorcy dla stworzonych w niej pakietów.
