# System Kas Samoobsługowych w Supermarkecie

Autorzy: 
* Paweł Cirko, 
* Bartosz Tatys, 
* Krzysztof Wiśniewski

## Słownik pojęć
* SKSO - System Kas Samoobsługowych
* KSO - Kasa Samoobsługowa
* JCK - Jednostka Centralna Kas
* PKS - Punkt Kontroli Sprzedaży
* UKS - Umowa Kupna-Sprzedaży

## Lista 1 - wstęp
### Co?
Celem systemu jest usprawnienie procesu zawierania umów kupna-sprzedaży pomiędzy sklepem a klientem detalicznym. 

Przez "usprawnienie" rozumiemy: 
1. Przyspieszenie procesu zakupów dla klientów,
2. zwiększenie wydajności sklepu dzięki zmniejszeniu kolejek,
3. oszczędność czasu personelu,
4. oszczędność przestrzeni na sali sprzedaży,
5. dostosowanie do preferencji klientów,
6. zwiększenie poziomu bezpieczeństwa,
7. automatyzacja zbierania danych sprzedażowych.

### Jak?
SKSO umożliwiają wykonanie powyższego, dzięki zastosowaniu szeregu rozwiązań hardwarowych oraz softwarowych. Wstępna wersja systemu wygląda następująco: 

![alt text](Diagrams/uproszczonyDiagramElemetnowSystemu.png)

* **Kasa samoobsługowa** - Głównym jej zadaniem jest sprzedaż towarów z wykorzystaniem sensorów (skaner, waga). Użytkownik komunikuje się z kasą za pomocą ekranu dotykowego. Aby ograniczyć koszty oraz zwiększyć możliwości rozbudowy, KSO posiada ograniczoną moc obliczeniową oraz niewielką pamięć wewnętrzną. Kasa komunikuje się z peryferiami takimi jak kasy fiskalne czy terminale płatności kartą, które same w sobie nie są częścią systemu. KSO wysyła informacje o swoim aktualnym stanie (zeskanowanie towaru, status płatności) do JCK. Kasa przyjmuje polecenia od JCK.

* **Jednostka centralna kas** - mózg całego systemu. Z tego punktu możliwy jest podgląd utargu, czy zarządzanie funkcjonowaniem poszczególnych KSO. JCK pobiera dane ze wszystkich KSO, nastepnie je przekształca do formy przydatnej dla pracowników sklepu. JCK przekazuje niektóre z tych danych do PKS. W przypadku sieci z wieloma lokalizacjami możliwe jest także wysyłanie danych w czasie rzeczywistym do "centrali".

* **Punkt kontroli sprzedaży** - Umożliwia integrację z systemem kamer bezpieczeństwa wyświetlając informacje odnośnie aktualnie skanowanych towarów oraz statusu płatności. Dane pobiera z JCK.

### Gdzie?

KSO musi zostać umieszczone w specjalnie do tego przygotowanej strefie, zazwyczaj znajdującej się obok tradycyjnych kas sprzedażowych. Punkt taki musi posiadać stały dostęp do prądu. Co więcej, KSO musi zostać wyposażone w dostępny na stanie sklepu terminal do przyjmowania płatności kartą oraz kasę fiskalną. Zalecane jest także umieszczenie kamery monitoringu bezpośrednio nad strefą kasowania towarów. 

JCK umieszczone jest na zapleczu sklepu, w miejscu dogodnym dla managera. 

PKS umieszczone jest w miejscu pracy pracownika ochrony sklepu.

Każde KSO musi zostać połączone z fizycznym kablem do JCK.
JCK i PKS posiadają dostep do Internetu.

### Kto?
SKSO przewiduje następujące osoby korzystające z systemu:
1. **Klient sklepu** - umożliwia się mu dokonywanie zakupów poprzez skanowanie towarów oraz obsługę płatności.
2. **Pracownik sklepu** - umożliwia się mu to, co klientowi sklepu. Dodatkowo pracownik może wycofać ówcześnie zeskanowane towary, potwierdzić wiek osoby kupującej, włączać/wyłączać SCO.
3. **Manager sklepu** - umożliwia się mu to, co pracownikowi sklepu. Dodatkowo manager może zdalnie zmieniać ceny produktów oraz kontrolować utarg KSO. Stacjonarnie może podpinać podzespoły takie jak terminale czy kasy fiskalne. 
4. **Pracownik ochrony sklepu** - umożliwia się mu zdalne kontrolowanie zeskanowanych towarów w czasie rzeczywistym.
5. **Serwisant** - umożliwia się mu wszystko to, co pozostałym kategoriom. Dodatkowo serwisant może uzyskać dostep do logów generowanych przez system.

### Dostosowanie do wymogów
Ustawodawca przewidział szereg ograniczeń do UKS, które system wykorzystywany komercyjnie musi spełniać:
1. Przepisy dotyczące **uczciwego handlu**: Warunek ten zostane spełniony przez zastosowanie atestowanych czujników.
2. Regulacje dotyczące **ochrony danych osobowych** RODO. Warunek ten zostanie spełniony przez niezbieranie danych umożliwiających identyfikację kupującego.
3. Regulacje dotyczące **zapewnienia dostępności**. Warunek ten zostanie spełniony poprzez dodanie przycisku umożliwiającego wezwanie pomocy pracownika sklepu na dowolnym etapie interakcji z systemem.
4. Przepisy dotyczące **praw konsumenta**. Warunek ten zostanie spełniony przez dodanie do systemu kasy fiskalnej drukującej paragony oraz faktur uproszczonych (paragon z NIP). Wszelkie zwroty będą rozliczane w kasach obsługiwanych przez pracowników sklepu.
5. Przepisy dotyczące **ochrony zdrowia nieletnich**. Warunek ten zostanie spełniony dzięki uniemożliwieniu sprzedaży konkretnych towarów bez zatwierdzenia wieku klienta przez pracownika sklepu.

## Lista 2 - przypadki użycia 
### Lista przypadków użycia
![Przypadki-użycia_page-0001](https://github.com/KaWis17/SelfCheckout-Documentation/assets/33382483/85cf2288-c286-4332-8917-53325f1e96cb)
![Przypadki-użycia_page-0002](https://github.com/KaWis17/SelfCheckout-Documentation/assets/33382483/58266439-195e-4129-bc44-a220a6e9fde1)
![Przypadki-użycia_page-0003](https://github.com/KaWis17/SelfCheckout-Documentation/assets/33382483/52686e63-4cb1-440a-8a64-4bb18ca908e2)
![Przypadki-użycia_page-0004](https://github.com/KaWis17/SelfCheckout-Documentation/assets/33382483/e842d60d-a8f4-4653-bea7-aeb28d478a2b)
![Przypadki-użycia_page-0005](https://github.com/KaWis17/SelfCheckout-Documentation/assets/33382483/388c10dd-2ed9-4040-aad1-ee7d59c18454)
![Przypadki-użycia_page-0006](https://github.com/KaWis17/SelfCheckout-Documentation/assets/33382483/a320a86a-0ca1-4a00-a7f9-48e343a7bf89)
![Przypadki-użycia_page-0007](https://github.com/KaWis17/SelfCheckout-Documentation/assets/33382483/ed2c001a-58d6-4856-b2a8-c3a2f1c284fb)
![Przypadki-użycia_page-0008](https://github.com/KaWis17/SelfCheckout-Documentation/assets/33382483/19c8b572-7c08-49f4-8612-6185293243b7)
![Przypadki-użycia_page-0009](https://github.com/KaWis17/SelfCheckout-Documentation/assets/33382483/a522cafa-1f74-4ed1-a086-edc071f72da5)
![Przypadki-użycia_page-0010](https://github.com/KaWis17/SelfCheckout-Documentation/assets/33382483/02d0a42b-d5e6-43d4-9525-bdc60be8146a)

### Diagram przypadków użycia
![Przypadki-użycia_page-0011](https://github.com/KaWis17/SelfCheckout-Documentation/assets/33382483/455dc788-5e66-4aff-930e-40e4728d187e)

<!---

## Lista 3 - hardware
### Diagram komponentów systemu
### Diagram stanów systemu

## Lista 4 - 
### Opis działania systemu
### Integracja dokumentacji
-->
