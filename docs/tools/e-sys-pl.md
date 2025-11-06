# E-SYS (Engineering System)

## 1. Tytuł i Krótki Opis

**E-SYS** (Engineering System) to główne inżynierskie narzędzie programowe używane przez BMW do diagnostyki, kodowania i programowania pojazdów **serii F**, **serii G** i **serii I**. Działa na niższym poziomie niż ISTA/P, zapewniając szczegółową kontrolę nad konfiguracją Elektronicznych Jednostek Sterujących (**ECU**) za pomocą **FDL-Coding** (Function Data Line Coding) i flashowania.

## 2. Cel / Przypadki Użycia

E-SYS to potężne narzędzie używane głównie do zaawansowanych operacji, które wymagają bezpośredniej manipulacji parametrami **ECU**.

*   **FDL-Coding:** Modyfikowanie określonych funkcji i parametrów wewnątrz **ECU** (np. aktywacja funkcji, zmiana zachowania świateł).
*   **Flashowanie (Programowanie):** Aktualizacja oprogramowania układowego (firmware) jednej lub więcej **ECU** za pomocą plików **PSdZData**.
*   **Zarządzanie Zamówieniem Pojazdu (VO):** Odczytywanie, zapisywanie i modyfikowanie **VO** (lub **FA** - Fahrzeugauftrag) w celu zdefiniowania fabrycznej konfiguracji i opcji pojazdu.
*   **Wymiana Modułu:** Przygotowanie i kodowanie nowych lub używanych **ECU** w celu dopasowania do **VO** pojazdu.

## 3. Obsługiwane Generacje Pojazdów

E-SYS jest specjalnie zaprojektowany dla nowszych generacji pojazdów BMW, które wykorzystują protokół komunikacyjny **ENET** (Ethernet).

| Generacja | Przykładowe Modele | Interfejs Komunikacyjny |
| :--- | :--- | :--- |
| **Seria F** | F10, F30, F25 | ENET, ICOM |
| **Seria G** | G20, G30, G05 | ENET, ICOM |
| **Seria I** | i3, i8, iX | ENET, ICOM |

## 4. Interfejsy i Protokoły

E-SYS wymaga szybkiego i stabilnego połączenia ze względu na duży rozmiar plików programowania.

*   **ENET (Ethernet):** Standardowy, bezpośredni interfejs dla pojazdów serii F/G/I. Zapewnia niezbędną przepustowość do programowania.
*   **ICOM (Integrated Communication Optical Module):** Oficjalny interfejs, który zapewnia zarządzane i bardzo stabilne połączenie **ENET**, często preferowany do krytycznych zadań programowania.
*   **Protokoły:** E-SYS komunikuje się za pomocą protokołu **UDS** (Unified Diagnostic Services) przez **Ethernet**.

## 5. Instalacja i Dostęp

E-SYS jest zazwyczaj dystrybuowany jako część zestawu narzędzi inżynierskich BMW.

*   **Wymagania Systemowe:** Wymaga systemu operacyjnego Windows oraz znacznej mocy obliczeniowej i pamięci RAM, zwłaszcza do operacji programowania.
*   **Legalny Dostęp:** E-SYS jest przeznaczony głównie dla inżynierów BMW i autoryzowanych partnerów technicznych. Legalny dostęp do oprogramowania i niezbędnych plików **PSdZData** jest kontrolowany przez BMW AG.

## 6. Ogólny Przepływ Pracy / Typowe Procedury

### Procedura FDL-Coding:

1.  **Połącz:** Połącz pojazd za pomocą **ENET** lub **ICOM**.
2.  **Odczytaj VO:** Odczytaj **VO** pojazdu i zapisz go.
3.  **Odczytaj ECU:** Odczytaj dane kodowania z docelowej **ECU** (np. **HU_NBT** dla iDrive).
4.  **Edytuj FDL:** Zmodyfikuj żądane parametry w edytorze **FDL** (Function Data Line).
5.  **Koduj:** Zapisz zmodyfikowane **FDL** z powrotem do **ECU**.

### Procedura Programowania (Flashowania):

1.  **Połącz:** Połącz pojazd za pomocą **ICOM** (preferowane) lub **ENET**.
2.  **Zasilanie:** **KRYTYCZNE:** Podłącz stabilne źródło zasilania (13.5V+, 50A+) do akumulatora pojazdu.
3.  **Identyfikuj:** Zidentyfikuj pojazd i docelowe **ECU** do programowania.
4.  **Oblicz:** E-SYS oblicza niezbędne kroki programowania i pliki na podstawie **VO** i najnowszych **PSdZData**.
5.  **Flashuj:** Wykonaj proces programowania. **NIE PRZERYWAJ.**

## 7. Kluczowe Ekrany / Elementy Interfejsu Użytkownika

*   **Edytor Zamówienia Pojazdu (VO):** Używany do przeglądania i modyfikowania listy opcji i kodów wyposażenia (np. `S05AP` - Dekodowanie Asystenta Świateł Drogowych Bez Oślepiania).
*   **Edytor FDL:** Główny interfejs do kodowania, umożliwiający użytkownikowi zmianę parametrów z `nicht_aktiv` na `aktiv` lub modyfikację wartości.
*   **Edytor TAL (Target Address List):** Używany podczas programowania do definiowania sekwencji operacji flashowania i kodowania.

## 8. Bezpieczeństwo i Ryzyka

E-SYS jest narzędziem wysokiego ryzyka. Błędy mogą prowadzić do poważnych konsekwencji.

*   **Uceglenie (Bricking):** Przerwanie sesji programowania (np. z powodu utraty zasilania lub awarii połączenia) może trwale uszkodzić (**uceglić**) **ECU**, co wymaga jego wymiany.
*   **Niezgodność VO:** Nieprawidłowa modyfikacja **VO** może prowadzić do awarii systemu, kontrolek ostrzegawczych i awarii komponentów.
*   **Napięcie:** **ABSOLUTNIE KRYTYCZNE.** Programowanie musi być wykonywane wyłącznie przy podłączonym stabilnym zasilaczu o wysokim natężeniu.

## 9. Rozwiązywanie Problemów i Typowe Błędy

| Błąd | Opis | Diagnoza / Rozwiązanie |
| :--- | :--- | :--- |
| **Przekroczenie Limitu Czasu Połączenia** | E-SYS traci połączenie podczas sesji kodowania lub programowania. | Sprawdź integralność kabla **ENET**. Zweryfikuj, czy zapora sieciowa komputera jest wyłączona. Użyj dedykowanego interfejsu **ICOM** dla maksymalnej stabilności. |
| **Nie Znaleziono CAFD** | Plik danych kodowania **ECU** (**CAFD**) jest brakujący lub uszkodzony. | Zaktualizuj pliki **PSdZData** do najnowszej wersji. Ponownie odczytaj **ECU**, aby wygenerować **CAFD**. |
| **Błąd Obliczenia Celu SVT** | E-SYS nie może określić prawidłowej wersji oprogramowania dla **ECU**. | Upewnij się, że **VO** jest prawidłowe, a **PSdZData** jest kompletne i aktualne. |

## 10. Przykłady i Praktyczne Uwagi

*   **Video in Motion (VIM):** Częstym zadaniem FDL-Coding jest aktywacja VIM poprzez zmianę progu prędkości w **ECU** **HU_NBT** lub **HU_EVO**.
*   **Flash GTS:** E-SYS jest używany do flashowania oprogramowania układowego niektórych modułów (np. **DCT** lub **Dyferencjał**) oprogramowaniem zorientowanym na wydajność z modeli takich jak M4 GTS.

## 11. Odnośniki / Dalsza Lektura

*   [1] **Szkolenia Techniczne BMW Group:** Oficjalne materiały szkoleniowe często szczegółowo omawiają użycie E-SYS.
*   [2] **PSdZData:** Oficjalne pliki danych zawierające oprogramowanie układowe i parametry kodowania dla wszystkich **ECU**.

## 12. Dziennik Zmian / Wersjonowanie

Wersje E-SYS są ściśle powiązane z wersją **PSdZData**. Nowsze wersje E-SYS są wymagane do obsługi najnowszych **ECU** i wydań oprogramowania w nowych modelach BMW.

## 13. Rola

E-SYS jest używany głównie przez **Inżynierów BMW**, **Zaawansowanych Techników** i **Specjalistów od Kodowania**, którzy wymagają niskopoziomowego dostępu do konfiguracji pojazdu.

---
*Zobacz także: [Sprzęt ICOM](../tools/icom-hardware.md), [Słownik](../glossary.md)*
