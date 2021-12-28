Place
	properties
		name: Nazwa budynku
		Category: kategoria budynku
		description: opis budynku
		address
			countryCode: POL
			state: województwo
			county: powiat
			city: miejscowość
			postalCode: kod pocztowy
			street: ulica
			house: numer budynku
			level: piętro
			room: nazwa pokoju, na przykład numer
		placeWebsiteUrl: adres strony internetowej
		phoneNumber: numer telefonu
		emailAddress: adres email
		accessibility
			parking (null jeżeli w ogóle nie ma parkingu)
			entrances
				entrance
					name: Nazwa wejścia
					isMainEntrance: true/false Główne wejście do budynku.
					isLevel: true/false do wejścia nie prowadzą schody i nie jest potrzebna pochylnia. Wejście z poziomu gruntu
					hasFixedRamp: true/false Ma stałą pochylnię
					hasRemovableRamp: true/false Ma składaną rampę
					slopeAngle: kąt nachylenia pochylni
					schody
						name: nazwa schodów
						count: liczba schodów
						stepHeight: wysokość stopnia
						hasHighContrastNosing: true/false Stopnie są kontrastowo oznaczone
						hasTactileSafetyStrips: true/false Dotykowe pasy ostrzegawcze przed schodami
						hasAntiSlipNosing: true/false Stopnie są wykonane z materiału antypoślizgowego
						hasHandRail: true/false Schody mają poręcz
					door
						isRevolving: true/false Drzwi są obrotowe
						isAutomaticOrAlwaysOpen: true/false Drzwi otwierają się automatycznie lub są zawsze otwarte.
						doorOpensToOutside: true/false Drzwi otwierają się na zewnątrz.
						isEasyToHoldOpen: true/false Można je łatwo utrzymać w pozycji otwartej.
						hasErgonomicDoorHandle: true/false Drzwi mają wygodną klamkę.
						hasClearMarkingOnGlassDoor: true/false Przeźroczyste drzwi są oznaczone kontrastowo. Undefined gdy drzwi nie są przeźroczyste.
						Width: szerokość drzwi
			staff
				canSeeVisitorsFromInside: true/false Pracownicy widzą wchodzących
				hasFreeAssistantForVisitors: true/false Pracownik oferuje asystę odwiedzającym.
				spokenLanguages: PJM, POL, ENG Znajomość języków
			serviceContact: sposób kontaktu z obsługą
			orientation (dodane przeze mnie na potrzeby ustawy)
					hasTactilePlan: true/false dotykowy plan pomieszczeń
					hasLargePrintPlan: true/false Plan z dużymi czcionkami
					hasHighContrastPlan: true/false Plan jest kontrastowy
					hasAudioSystem: true/false Dźwiękowe wspomaganie nawigacji.
			hasTactileGuideStrips: true/false ścieżki prowadzące
			hasInductionLoop: true/false pętla indukcyjna
			hasSignLanguageService: true/false Dostępność tłumacza PJM
			isQuiet: true/false miejsce jest ciche
			isWellLit: true/false miejsce jest dobrze oświetlone
			animalPolicy
				allowsAnyAnimals: true/false Można wchodzić z każdym zwierzęciem.
				allowsDogs: true/false Można przyjść z psem
				allowsGuideDogs: true/false Można przyjść z psem przewodnikiem lub psem asystującym
				dogsNeedMuzzle: true/false Pies musi mieć kaganiec
				suppliesWaterForPets: true/false Woda dla zwierzaka.
			pathways
			restrooms (null jeżeli w budynku nie ma toalet) Można powielać obiekt.
				name: nazwa łazienki
				entrance
				turningSpaceInside: przestrzeń manewrowa.
				hasSupportRails: true/false poręcze
				hasMirror: true/false Lustro
				heightOfDrier: wysokość zawieszenia ręcznika
				heightOfSoap: wysokość na jakiej jest mydło
				toilet
					hasFoldingHandles: true/false składane pochwyty przy sedesie
					heightOfBase: wysokość miski ustępowej
					spaceInFront: przestrzeń przed ustępem
					spaceOnUsersLeftSide: przestrzeń po lewej stronie ustępu
					spaceOnUsersRightSide: przestrzeń po prawej stronie ustępu
: 				hasShower: true/false prysznic
				hasBathTub: true/false wanna
				I