# 🌍 Wybierz język / Choose language

[🇵🇱 Polski](#-polska-wersja) | [🇬🇧 English](#-english-version)

#


# 🇬🇧 English version
# ISTA/D (Integrated Service Technical Application / Diagnostics)

## 1. Title and Short Description

**ISTA/D** (Integrated Service Technical Application / Diagnostics) is the official BMW Group diagnostic software used by authorized dealers and service centers worldwide. It is the primary tool for reading fault codes (**DTC**), performing guided troubleshooting, executing test plans, and carrying out service functions on all modern BMW, Mini, and Rolls-Royce vehicles.

## 2. Purpose / Use Cases

ISTA/D is the cornerstone of the BMW diagnostic process. Its main use cases include:

*   **Guided Troubleshooting:** Automatically generating a test plan based on read **DTC**s, guiding the technician step-by-step through the repair process.
*   **Fault Memory Management:** Reading, clearing, and detailed analysis of fault codes from all Electronic Control Units (**ECU**).
*   **Component Testing:** Activating and testing individual components (e.g., fuel pump, injectors, actuators) to verify functionality.
*   **Service Functions:** Performing necessary service procedures such as battery registration, brake pad replacement mode, and steering angle sensor calibration.
*   **Technical Information:** Providing integrated access to repair instructions, wiring diagrams, and component locations.

## 3. Supported Vehicle Generations

ISTA/D supports virtually all BMW Group vehicles from the late **E-series** (e.g., E60, E90) through the current **F-series**, **G-series**, and **I-series** (electric vehicles).

| Generation | Example Models | Communication Interface |
| :--- | :--- | :--- |
| **E-series** | E60, E70, E90 | ICOM (D-CAN) |
| **F-series** | F10, F30, F25 | ICOM (ENET) |
| **G-series** | G20, G30, G05 | ICOM (ENET) |
| **I-series** | i3, i8, iX | ICOM (ENET) |

## 4. Interfaces & Protocols

ISTA/D requires a stable communication interface to connect to the vehicle's communication buses.

*   **ICOM (Integrated Communication Optical Module):** The official, multi-protocol interface that is highly recommended for all operations due to its stability and support for all protocols (**D-CAN**, **ENET**, **MOST**).
*   **ENET (Ethernet):** Used for F/G/I-series vehicles, providing a direct, high-speed connection.
*   **K-DCAN:** Can be used for E-series vehicles, though ICOM is preferred for full functionality.

## 5. Installation & Access

ISTA/D is part of the **ISPI Next** (Integrated Service Processes Initiative) platform.

*   **System Requirements:** Typically requires a Windows operating system (often 64-bit) with significant storage space for the diagnostic data and integrated technical information.
*   **Legal Access:** Authorized access is granted to BMW Group dealers and service partners. Independent operators can legally purchase access to technical information and programming services through the **AOS** (Aftersales Online System) portal [1].

## 6. General Workflow / Typical Procedures

A typical diagnostic session in ISTA/D follows a structured, guided process:

1.  **Connect ICOM:** Connect the ICOM interface to the vehicle's **OBD-II** port and the service PC.
2.  **Vehicle Identification:** Start ISTA/D and initiate the connection to identify the vehicle via its **VIN** (Vehicle Identification Number).
3.  **Read Fault Memory:** ISTA/D reads the fault memory from all connected **ECU**s.
4.  **Generate Test Plan:** Based on the read **DTC**s, ISTA/D automatically generates a prioritized test plan.
5.  **Guided Testing:** The technician follows the test plan, which includes guided measurements, component checks, and step-by-step instructions.
6.  **Repair and Clear:** After the repair is complete, the fault memory is cleared, and a final check is performed.

## 7. Key Screens / UI Elements

*   **Fault Memory:** Displays a list of all current and historical **DTC**s, categorized by severity and module.
*   **Test Plan:** The central screen for guided diagnostics, showing the sequence of required actions.
*   **Vehicle Tree:** A graphical representation of the vehicle's **ECU** network, allowing direct access to individual modules.
*   **Repair Instructions:** Integrated technical documentation, including torque specifications and removal/installation procedures.

## 8. Safety & Risks

While ISTA/D is primarily a diagnostic tool, safety precautions are still necessary:

*   **Voltage:** Although diagnostics consume less power than programming, a stable battery is crucial. Low voltage can cause communication errors and lead to incorrect diagnoses.
*   **Component Activation:** Be cautious when activating components (e.g., fuel pump, ignition) to avoid damage or injury.

## 9. Troubleshooting & Common Errors

| Error | Description | Diagnosis / Solution |
| :--- | :--- | :--- |
| **Vehicle Identification Failed** | ISTA/D cannot establish communication with the vehicle. | Check ICOM/ENET connection. Verify the **ZGW** (Central Gateway) module is powered. Ensure the correct interface is selected in ISTA/D settings. |
| **DTCs Cannot Be Cleared** | Fault codes reappear immediately after clearing. | The underlying fault is still present (e.g., short circuit, faulty sensor). Follow the guided test plan to find the root cause. |
| **Communication Timeout** | Connection drops during a test or reading. | Often caused by an unstable **ENET** connection or low battery voltage. Use an ICOM or a high-quality **ENET** cable. |

## 10. Examples & Practical Notes

*   **Battery Registration:** After replacing the vehicle battery, ISTA/D is used to register the new battery in the **ECU** (specifically the **CAS** or **BDC** module) to ensure correct charging parameters.
*   **Forced DPF Regeneration:** ISTA/D contains service functions to initiate a forced regeneration of the Diesel Particulate Filter (**DPF**) when passive regeneration fails.

## 11. References / Further Reading

*   [1] **BMW Aftersales Online System (AOS):** The official source for purchasing technical information and service access. *URL Placeholder: https://aos.bmwgroup.com*
*   [2] **BMW Technical Information System (TIS):** The legacy system for repair instructions, now largely integrated into ISTA/D.

## 12. Change Log / Versioning

ISTA/D is regularly updated to support new vehicle models and diagnostic procedures. Updates often include:

*   New **DTC** definitions and corresponding test plans.
*   Updated repair instructions and wiring diagrams.
*   Support for new **ECU** variants and software versions.

## 13. Role

ISTA/D is primarily used by **ASO (Authorized Service Organization) Technicians** and **Certified Independent Workshops**. Its guided nature makes it the standard tool for day-to-day service and repair work.

---
*See also: [ICOM Hardware](../tools/icom-hardware.md), [Glossary](../glossary.md)*


# 🇵🇱 Polska wersja
# ISTA/D (Integrated Service Technical Application / Diagnostics)

## 1. Tytuł i krótki opis

**ISTA/D** (Integrated Service Technical Application / Diagnostics) to oficjalne oprogramowanie diagnostyczne Grupy BMW, używane przez autoryzowane serwisy i dealerów na całym świecie. Jest to główne narzędzie do odczytu błędów (**DTC**), prowadzenia diagnostyki krok po kroku, wykonywania planów testowych oraz funkcji serwisowych w pojazdach BMW, Mini i Rolls-Royce.

## 2. Cel / Zastosowania

ISTA/D stanowi podstawę procesu diagnostycznego w BMW. Jej główne zastosowania obejmują:

*   **Prowadzona diagnostyka:** Automatyczne tworzenie planu testowego na podstawie odczytanych **DTC**, prowadzącego technika krok po kroku przez proces naprawy.
*   **Zarządzanie pamięcią błędów:** Odczyt, kasowanie i szczegółowa analiza błędów ze wszystkich modułów sterujących (**ECU**).
*   **Testowanie komponentów:** Aktywacja i sprawdzanie poszczególnych podzespołów (np. pompy paliwa, wtryskiwaczy, siłowników) w celu weryfikacji ich działania.
*   **Funkcje serwisowe:** Wykonywanie procedur serwisowych, takich jak rejestracja nowego akumulatora, tryb wymiany klocków hamulcowych czy kalibracja czujnika kąta skrętu.
*   **Informacje techniczne:** Zintegrowany dostęp do instrukcji napraw, schematów elektrycznych i lokalizacji podzespołów.

## 3. Obsługiwane generacje pojazdów

ISTA/D obsługuje praktycznie wszystkie pojazdy Grupy BMW – od późnych modeli **E-serii** (np. E60, E90) po współczesne **F-, G-** i **I-serie** (pojazdy elektryczne).

| Generacja | Przykładowe modele | Interfejs komunikacyjny |
| :--- | :--- | :--- |
| **Seria E** | E60, E70, E90 | ICOM (D-CAN) |
| **Seria F** | F10, F30, F25 | ICOM (ENET) |
| **Seria G** | G20, G30, G05 | ICOM (ENET) |
| **Seria I** | i3, i8, iX | ICOM (ENET) |

## 4. Interfejsy i protokoły

ISTA/D wymaga stabilnego interfejsu komunikacyjnego do połączenia z magistralami pojazdu.

*   **ICOM (Integrated Communication Optical Module):** Oficjalny, wieloprotokołowy interfejs BMW, zalecany do wszystkich operacji ze względu na stabilność i obsługę wszystkich protokołów (**D-CAN**, **ENET**, **MOST**).
*   **ENET (Ethernet):** Stosowany w pojazdach serii F/G/I, zapewniający szybkie, bezpośrednie połączenie.
*   **K-DCAN:** Może być używany w serii E, choć ICOM jest preferowany dla pełnej funkcjonalności.

## 5. Instalacja i dostęp

ISTA/D jest częścią platformy **ISPI Next** (Integrated Service Processes Initiative).

*   **Wymagania systemowe:** Zazwyczaj system Windows 64-bit z dużą ilością miejsca na dane diagnostyczne i dokumentację techniczną.
*   **Dostęp legalny:** Autoryzowany dostęp mają dealerzy i partnerzy serwisowi BMW. Niezależni operatorzy mogą legalnie zakupić dostęp do informacji technicznych i usług programowania poprzez portal **AOS** (Aftersales Online System) [1].

## 6. Ogólny przebieg pracy / Typowe procedury

Typowa sesja diagnostyczna w ISTA/D przebiega według ustrukturyzowanego procesu:

1.  **Podłącz ICOM:** Połącz interfejs ICOM z portem **OBD-II** pojazdu i komputerem serwisowym.  
2.  **Identyfikacja pojazdu:** Uruchom ISTA/D i zidentyfikuj pojazd po numerze **VIN**.  
3.  **Odczyt błędów:** ISTA/D odczytuje pamięć błędów ze wszystkich modułów **ECU**.  
4.  **Tworzenie planu testowego:** Na podstawie błędów **DTC** program generuje priorytetowy plan testowy.  
5.  **Diagnostyka prowadzona:** Technik wykonuje kolejne kroki zgodnie z planem (pomiar, test, wymiana itp.).  
6.  **Naprawa i czyszczenie błędów:** Po naprawie błędy są kasowane i wykonywany jest końcowy test.  

## 7. Kluczowe ekrany / Elementy interfejsu

*   **Pamięć błędów:** Lista wszystkich bieżących i historycznych błędów **DTC**, z podziałem na moduły i priorytety.  
*   **Plan testowy:** Główne okno diagnostyczne z sekwencją czynności do wykonania.  
*   **Drzewo pojazdu:** Graficzne przedstawienie sieci **ECU**, umożliwiające bezpośredni dostęp do modułów.  
*   **Instrukcje napraw:** Zintegrowana dokumentacja techniczna, w tym momenty dokręcania i procedury demontażu/montażu.  

## 8. Bezpieczeństwo i ryzyka

Choć ISTA/D służy głównie do diagnostyki, należy zachować środki ostrożności:

*   **Napięcie:** Niski poziom napięcia akumulatora może powodować błędy komunikacji lub nieprawidłowe odczyty.  
*   **Aktywacja komponentów:** Ostrożnie uruchamiaj elementy takie jak pompa paliwa czy zapłon – mogą spowodować obrażenia lub uszkodzenia.  

## 9. Rozwiązywanie problemów / Typowe błędy

| Błąd | Opis | Diagnoza / Rozwiązanie |
| :--- | :--- | :--- |
| **Nie można zidentyfikować pojazdu** | Brak komunikacji z pojazdem. | Sprawdź połączenie ICOM/ENET, zasilanie modułu **ZGW**, wybór interfejsu w ustawieniach ISTA/D. |
| **Nie można skasować błędów DTC** | Błędy pojawiają się ponownie po kasowaniu. | Usterka wciąż obecna – wykonaj pełny plan testowy, aby znaleźć przyczynę. |
| **Przerwanie komunikacji (timeout)** | Połączenie przerywa w trakcie testu lub odczytu. | Przyczyna to zwykle niestabilne połączenie **ENET** lub niskie napięcie akumulatora. Użyj ICOM lub wysokiej jakości kabla. |

## 10. Przykłady i uwagi praktyczne

*   **Rejestracja akumulatora:** Po wymianie akumulatora ISTA/D służy do jego zarejestrowania w module **CAS** lub **BDC**, co zapewnia prawidłowe parametry ładowania.  
*   **Wymuszona regeneracja DPF:** ISTA/D umożliwia inicjację wymuszonej regeneracji filtra cząstek stałych (**DPF**), gdy regeneracja pasywna nie zachodzi.  

## 11. Źródła / Dalsze informacje

*   [1] **BMW Aftersales Online System (AOS):** Oficjalne źródło zakupu dostępu do informacji technicznych i usług. *URL: https://aos.bmwgroup.com*  
*   [2] **BMW Technical Information System (TIS):** Starszy system instrukcji napraw, obecnie w większości zintegrowany z ISTA/D.  

## 12. Dziennik zmian / Wersjonowanie

ISTA/D jest regularnie aktualizowana, aby obsługiwać nowe modele i procedury diagnostyczne. Aktualizacje obejmują m.in.:

*   Nowe definicje błędów **DTC** i odpowiadające im plany testowe.  
*   Zaktualizowane instrukcje napraw i schematy elektryczne.  
*   Obsługę nowych wariantów **ECU** i wersji oprogramowania.  

## 13. Rola

ISTA/D jest używana głównie przez **techników ASO BMW** oraz **certyfikowane niezależne warsztaty**. Dzięki prowadzonemu charakterowi stanowi podstawowe narzędzie w codziennej diagnostyce i naprawie pojazdów BMW.

---
*Zobacz także: [ICOM Hardware](../tools/icom-hardware.md), [Glosariusz](../glossary.md)*
