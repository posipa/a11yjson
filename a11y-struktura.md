# Place

## properties

1. name: Nazwa miejsca
2. Category: kategoria miejsca (szkoła, przedszkole, żłobek, biblioteka, urząd, kino, teatr, muzeum itp.
3. description: opis miejsca.
4. [address {#address}](#address) adres strukturalizowany.
7. placeWebsiteUrl: adres strony internecienetowej
8. phoneNumber: numer telefonu
9. emailAddress: adres email
10. accessibility:
	1. [parking](#parking) (null jeżeli w ogóle nie ma parkingu) Otwiera się okienko opisu parkingu.
	2. [entrances](entrance) lista wejść, okienko opisu wejścia.
	3. staff
	1. canSeeVisitorsFromInside: true/false Pracownicy widzą wchodzących.
	2. hasFreeAssistantForVisitors: true/false Pracownik oferuje asystę odwiedzającym.
	3. spokenLanguages: PJM, POL, ENG Znajomość języków.
4. serviceContact: sposób kontaktu z obsługą.
5. orientation (dodane przeze mnie na potrzeby ustawy)
	1. hasTactilePlan: true/false dotykowy plan pomieszczeń.
	2. hasLargePrintPlan: true/false Plan z dużymi czcionkami.
	3. hasHighContrastPlan: true/false Plan jest kontrastowy.
	4. hasAudioSystem: true/false Dźwiękowe wspomaganie nawigacji.
6. . hasTactileGuideStrips: true/false ścieżki prowadzące.
7. hasInductionLoop: true/false pętla indukcyjna.
8. hasSignLanguageService: true/false Dostępność tłumacza PJM (dodane przeze mnie).
9. isQuiet: true/false miejsce jest ciche.
10. isWellLit: true/false miejsce jest dobrze oświetlone.
11. [animalPolicy](#animalPolicy) domyślnie taki sam dla miejsc o tym samym adresie. Okienko opisu.
12. [pathways](#pathway) okienko szczegółów.
13. ground

## Parking {parking}

Standardowe kontrolki.

### Okienko szczegółów

### Właściwości

1. forWheelchairUsers:
	1. count: liczba miejsc parkingowych dla osób niepełnosprawnych.
	2. distanceToEntrance: odległość do wejścia.
	3. width: szerokość miejsca parkingowego.
	4. length: długość miejsca parkingowego.
	5. hasDedicatedSignage: true/false prawidłowe oznaczenie miejsc parkingowych.
	6. location: opis usytuowania parkingu.
	7. isLocatedInside: true/false parking jest w budynku lub pod dachem.
	8. maxVehicleHeight: maksymalna wysokość pojazdów.
	9. paymentBySpace: true/false płatność za miejsce parkingowe.
2. Count: liczba wszystkich miejsc parkingowych.

## animalPolicy {#animalPolicy}]

Okienko szczegółów. Obowiązkowe dla podmiotów publicznych.

### Okienko szczegółów

Lista wyboru z pozycjami 1-3 i dodatkową o zakazie wchodzenia ze zwierzętami. W tym ostatnim przypadku wszystkie właściwości ustawione na false i pojawia się okienko uzasadnienia. Pozycje 4 i 5 aktywne gdy wybrana jest opcja 1-3.

### Właściwości

1. allowsAnyAnimals: true/false Można wchodzić z każdym zwierzęciem.
2. allowsDogs: true/false Można przyjść z psem.
3. allowsGuideDogs: true/false Można przyjść z psem przewodnikiem lub psem asystującym.
4. dogsNeedMuzzle: true/false Pies musi mieć kaganiec.
5. suppliesWaterForPets: true/false Woda dla zwierzaka.


## entrance

Obszar wejściowy. Dotyczy zarówno wejść z zewnątrz, jak i pomiędzy różnymi miejscami. Obowiązkowy dla każdego miejsca.

### Okienko szczegółów

Standardowe pola edycyjne i wyboru. Okienka szczegółów schodów i drzwi możliwe do aktywowania, gdy dany element jest zaznaczony. W przypadku drzwi domyślnie zaznaczone.

### Właściwości

1. name: Nazwa wejścia
2. isMainEntrance: true/false Główne wejście.
3. isLevel: true/false do wejścia nie prowadzą schody i nie jest potrzebna pochylnia. Wejście z poziomu gruntu
4. hasFixedRamp: true/false Ma stałą pochylnię
5. hasRemovableRamp: true/false Ma składaną rampę.
6. slopeAngle: kąt nachylenia pochylni lub innego podjazdu.
7. [stairs](#stairs) okienko szczegółów schodów.
. 8. [door]()](#door) okienko szczegółów drzwi.


## stairs {#stairs}

Opis schodów. Tu brakuje kilku właściwości, na przykład czy schody są proste, szerokość schodów. Nie ma też właściwości poręczy, co akurat w Polsce jest istotne. To trzeba będzie dodać. Można jeszcze dołożyć głębokość stopni.

### Okienko szczegółów

Standardowe kontrolki.

### Właściwości

1. name: nazwa schodów
2. count: liczba schodów.
3. stepHeight: wysokość stopnia.
4. hasHighContrastNosing: true/false Stopnie są kontrastowo oznaczone.
5. hasTactileSafetyStrips: true/false Dotykowe pasy ostrzegawcze przed schodami.
6. hasAntiSlipNosing: true/false Stopnie są wykonane z materiału antypoślizgowego.
7. hasHandRail: true/false Schody mają poręcz.
8. stepDepth: głębokość stopnia (dodane przeze mnie).
9. stepWidth: szerokość stopnia w najwęższym miejscu (dodane przeze mnie).
10. isRegular: true/false schody są proste (dodane przeze mnie).


## door {#door}

Obiekt opisujący drzwi. Dotyczy każdego rodzaju drzwi, w tym do windy. Do dodania właściwość opisująca łatwość otwierania drzwi (opór).

### Okienko szczegółów

Standardowe kontrolki. isEasyToOpen powinno mieć jakieś domyślne wartości do wyboru, na przykład: 0 drzwi są bardzo ciężkie, 0.5 drzwi otwierają się ciężko, ale otworzy je osoba dorosła, 1 drzwi otwierają się lekko. W przyszłości może jakieś wartości dynamometryczne.

### Właściwości

1. isRevolving: true/false Drzwi są obrotowe
2. isAutomaticOrAlwaysOpen: true/false Drzwi otwierają się automatycznie lub są zawsze otwarte.
3. doorOpensToOutside: true/false Drzwi otwierają się na zewnątrz.
4. isEasyToHoldOpen: true/false Można je łatwo utrzymać w pozycji otwartej.
5. hasErgonomicDoorHandle: true/false Drzwi mają wygodną klamkę.
6. hasClearMarkingOnGlassDoor: true/false Przeźroczyste drzwi są oznaczone kontrastowo. Undefined gdy drzwi nie są przeźroczyste.
7. width: szerokość drzwi.
8. turningSpaceInFront: przestrzeń manewrowa przed drzwiami.
9. isEasyToOpen: łatwość otwierania drzwi w przedziale 0-1. Dodane przeze mnie.

## restroom

Opis łazienki

### Okienko szczegółów

### Właściwości

1. name: nazwa łazienki.
2. [entrance](#entrance) wejście do łazienki.
3. turningSpaceInside: przestrzeń manewrowa wewnątrz łazienki.
4. hasSupportRails: true/false poręcze na ścianach.
5. hasMirror: true/false Lustro. Po zaznaczeniu można dodać szczegóły:
	1. heightFromGround: wysokość, na jakiej jest dolna krawędź lustra.
	2. isLocatedInsideRestroom: true/false. W przypadku łazienki domyślnie zaznaczone i tylko do odczytu.
	3. isAccessibleWhileSeated: true/false można korzystać z pozycji siedzącej, czyli lustro jest na odpowiedniej wysokości.
6. heightOfDrier: wysokość zawieszenia ręcznika
7. heightOfSoap: wysokość na jakiej jest mydło.
8. toilet
	1. hasFoldingHandles: true/false składane pochwyty przy sedesie. Po zaznaczeniu można dodać szczegóły:
		1. onUsersLeftSide: true/false pochwyt po lewej stronie użytkownika.
		2. onUsersRightSide: true/false pochwyt po prawej stronie użytkownika
	 3. distanceBetweenHandles: odległość między pochwytami. (Aktywne, gdy zaznaczone są oba pochwyty).
	4. topHeightFromFloor: wysokość pochwytu.
	2. heightOfBase: wysokość miski ustępowej
	3. spaceInFront: przestrzeń przed ustępem.
	4. spaceOnUsersLeftSide: przestrzeń po lewej stronie ustępu
	5. spaceOnUsersRightSide: przestrzeń po prawej stronie ustępu
9. : 				hasShower: true/false prysznic.
10. hasBathTub: true/false wanna.

## address {#address}

Lokalizacja miejsca (place).

### Okienko szczegółów

Adres dla miejsca będzie się zmieniał dla konkretnego budynku. W szczególności dodawanie pięter i pomieszczeń będzie generować kolejne miejsca. To musi się odbywać w tle, bez wiedzy użytkownika. Wizualnie może to być struktura drzewiasta. Do pięter można dodawać pomieszczenia (room) i łazienki (restroom).

Do każdego dodanego miejsca można dodać zdjęcie ilustracyjne. Można włączyć generowanie mapy z Google Maps lub OpenStreetMaps.

### Właściwości

1. countryCode: POL (zakładamy opisywanie lokacji w Polsce).
2. state: województwo
3. county: powiat
4. city: miejscowość
5. postalCode: kod pocztowy
6. street: ulica
7. house: numer budynku
8. level: piętro
9. room: nazwa pomieszczenia, na przykład numer, sala konferencyjna, lobby, szatnia

## Room

Opis pomieszczenia. 
Ma tylko jedną właściwość (poniżej). Trzeba dodać właściwość "entrance".

### Właściwości

.isAccessibleWithWheelchair: true/false dostępne dla osób na wózkach.