# 🌍 Wybierz język / Choose language

[🇵🇱 Polski](#-polska-wersja) | [🇬🇧 English](#-english-version)

#

# 🇬🇧 English version
# INPA (Integrated Service Technical Application / INPA)

## 1. Title and Short Description

**INPA** (Integrated Service Technical Application / INPA) is a legacy diagnostic and service tool developed by BMW. It provides a text-based, low-level interface for direct communication with Electronic Control Units (**ECU**) in older BMW vehicles. It is known for its ability to read real-time data and perform simple activations that may not be easily accessible in the newer **ISTA/D** system.

## 2. Purpose / Use Cases

INPA is primarily used for quick diagnostics and low-level component testing on E-series vehicles.

*   **Real-Time Data:** Reading live sensor data, engine parameters, and status flags.
*   **Fault Code Reading:** Reading and clearing **DTC**s (Diagnostic Trouble Codes) directly from the **ECU**.
*   **Component Activation:** Performing simple activations (e.g., testing solenoids, relays, or lights).
*   **Service Functions:** Executing basic service functions like resetting service intervals.

## 3. Supported Vehicle Generations

INPA is primarily a tool for the older **E-series** vehicles. Its functionality is limited on F-series and newer.

| Generation | Communication Support | Notes |
| :--- | :--- | :--- |
| **E-series** | D-CAN, K-Line | Full functionality |
| **F-series** | Limited | Can only read basic data via **ENET** with proper configuration. |

## 4. Interfaces & Protocols

INPA relies on the older communication protocols.

*   **K-DCAN Cable:** The standard interface for INPA, supporting both **K-Line** (older E-series) and **D-CAN** (newer E-series).
*   **Protocols:** K-Line (ISO 9141) and D-CAN (ISO 15765).

## 5. Installation & Access

INPA is part of the older **EDIABAS** toolset.

*   **System Requirements:** Typically runs on Windows XP/7. Requires the **EDIABAS** interface to be correctly configured.
*   **Legal Access:** INPA is largely superseded by ISTA/D and is not actively distributed by BMW AG for general service use.

## 6. General Workflow / Typical Procedures

1.  **Connect K-DCAN:** Connect the K-DCAN cable to the vehicle and the service PC.
2.  **Select Model:** Launch INPA and select the correct chassis and engine type.
3.  **Select ECU:** Choose the specific **ECU** to communicate with (e.g., **DME** for engine electronics).
4.  **Read Status:** Use the function keys (F1-F10) to navigate the menus and read fault memory or live data.

## 7. Key Screens / UI Elements

*   **Function Keys:** The primary navigation method, with each key corresponding to a specific function (e.g., F4 for Fault Memory, F5 for Status).
*   **Text-Based Interface:** INPA is characterized by its simple, text-based, green-on-black interface.

## 8. Safety & Risks

INPA is a low-level tool that allows direct, unguided access to **ECU** functions.

*   **Unguided Access:** Unlike ISTA/D, INPA does not provide guided procedures. Incorrect use of activation functions can potentially damage components.
*   **Voltage:** While not used for programming, stable voltage is still required to prevent communication errors.

## 9. Troubleshooting & Common Errors

| Error | Description | Diagnosis / Solution |
| :--- | :--- | :--- |
| **IFH-0009: No Response from Control Unit** | INPA cannot establish communication. | Check the **EDIABAS** configuration (`obd.ini` and `ediabas.ini`). Ensure the K-DCAN cable drivers are installed and the cable is set to the correct COM port. |
| **INPA Not Displaying Correctly** | Missing or incorrect scripts. | Ensure the correct **SGDAT** and **CFGDAT** files for the selected model are present in the INPA installation directory. |

## 10. Examples & Practical Notes

*   **Injector Correction Values:** INPA is often used to quickly read the injector correction values for diesel and gasoline engines.
*   **Battery Reset:** Can be used to reset the battery registration on some E-series vehicles.

## 11. References / Further Reading

*   [1] **EDIABAS Documentation:** Technical documentation for the underlying communication layer.

## 12. Change Log / Versioning

INPA is a legacy tool and is no longer actively developed or updated by BMW AG.

## 13. Role

INPA is used by **Advanced Technicians** and **Enthusiasts** who require quick, low-level access to E-series vehicles.

---
*See also: [Tool32](../tools/tool32.md), [Glossary](../glossary.md)*


# 🇵🇱 Polska wersja
# INPA (Integrated Service Technical Application / INPA)

## 1. Tytuł i krótki opis

**INPA** (Integrated Service Technical Application / INPA) to starsze narzędzie diagnostyczne i serwisowe opracowane przez BMW. Zapewnia tekstowy, niskopoziomowy interfejs do bezpośredniej komunikacji z jednostkami sterującymi (**ECU**) w starszych pojazdach BMW. Znane jest z możliwości odczytu danych w czasie rzeczywistym i wykonywania prostych aktywacji, które mogą być niedostępne w nowszym systemie **ISTA/D**.

## 2. Cel / Zastosowania

INPA jest wykorzystywane głównie do szybkiej diagnostyki i niskopoziomowych testów komponentów w pojazdach serii E.

*   **Dane w czasie rzeczywistym:** Odczyt bieżących danych z czujników, parametrów silnika i flag statusowych.
*   **Odczyt kodów błędów:** Odczyt i kasowanie kodów błędów (**DTC**) bezpośrednio z jednostki **ECU**.
*   **Aktywacja komponentów:** Wykonywanie prostych aktywacji (np. test cewek, przekaźników lub świateł).
*   **Funkcje serwisowe:** Wykonywanie podstawowych funkcji serwisowych, takich jak resetowanie interwałów przeglądowych.

## 3. Obsługiwane generacje pojazdów

INPA jest narzędziem przeznaczonym głównie dla starszych pojazdów **serii E**. Jego funkcjonalność w przypadku serii F i nowszych jest ograniczona.

| Generacja | Obsługa komunikacji | Uwagi |
| :--- | :--- | :--- |
| **Seria E** | D-CAN, K-Line | Pełna funkcjonalność |
| **Seria F** | Ograniczona | Możliwy tylko odczyt podstawowych danych przez **ENET** po odpowiedniej konfiguracji. |

## 4. Interfejsy i protokoły

INPA korzysta ze starszych protokołów komunikacyjnych.

*   **Kabel K-DCAN:** Standardowy interfejs dla INPA, obsługujący zarówno **K-Line** (starsze E-serie), jak i **D-CAN** (nowsze E-serie).
*   **Protokoły:** K-Line (ISO 9141) oraz D-CAN (ISO 15765).

## 5. Instalacja i dostęp

INPA jest częścią starszego pakietu narzędzi **EDIABAS**.

*   **Wymagania systemowe:** Zazwyczaj działa w systemach Windows XP/7. Wymaga poprawnie skonfigurowanego interfejsu **EDIABAS**.
*   **Dostęp legalny:** INPA została zastąpiona przez ISTA/D i nie jest już aktywnie dystrybuowana przez BMW AG do użytku serwisowego.

## 6. Ogólny przebieg pracy / Typowe procedury

1.  **Podłącz K-DCAN:** Podłącz kabel K-DCAN do pojazdu i komputera serwisowego.
2.  **Wybierz model:** Uruchom INPA i wybierz odpowiednie podwozie oraz typ silnika.
3.  **Wybierz ECU:** Wybierz konkretną jednostkę sterującą (**ECU**) do komunikacji (np. **DME** dla elektroniki silnika).
4.  **Odczytaj status:** Użyj klawiszy funkcyjnych (F1–F10), aby nawigować po menu i odczytać pamięć błędów lub dane w czasie rzeczywistym.

## 7. Kluczowe ekrany / Elementy interfejsu

*   **Klawisze funkcyjne:** Główna metoda nawigacji – każdy klawisz odpowiada konkretnej funkcji (np. F4 – pamięć błędów, F5 – status).
*   **Interfejs tekstowy:** Charakterystyczny prosty interfejs tekstowy o kolorystyce zielony na czarnym tle.

## 8. Bezpieczeństwo i ryzyka

INPA to narzędzie niskopoziomowe, umożliwiające bezpośredni, niekierowany dostęp do funkcji **ECU**.

*   **Brak prowadzenia użytkownika:** W przeciwieństwie do ISTA/D, INPA nie zawiera procedur krok po kroku. Nieprawidłowe użycie funkcji aktywacji może spowodować uszkodzenie komponentów.
*   **Napięcie:** Choć INPA nie służy do programowania, wymagane jest stabilne napięcie, aby uniknąć błędów komunikacji.

## 9. Rozwiązywanie problemów / Typowe błędy

| Błąd | Opis | Diagnoza / Rozwiązanie |
| :--- | :--- | :--- |
| **IFH-0009: No Response from Control Unit** | INPA nie może nawiązać komunikacji. | Sprawdź konfigurację **EDIABAS** (`obd.ini` i `ediabas.ini`). Upewnij się, że sterowniki kabla K-DCAN są zainstalowane i że kabel przypisany jest do właściwego portu COM. |
| **INPA wyświetla się niepoprawnie** | Brakujące lub błędne skrypty. | Upewnij się, że w katalogu instalacyjnym INPA znajdują się poprawne pliki **SGDAT** i **CFGDAT** dla wybranego modelu. |

## 10. Przykłady i uwagi praktyczne

*   **Korekty wtryskiwaczy:** INPA często wykorzystywana jest do szybkiego odczytu wartości korekcji wtryskiwaczy w silnikach benzynowych i wysokoprężnych.
*   **Reset akumulatora:** Może być używana do resetowania rejestracji akumulatora w niektórych pojazdach serii E.

## 11. Źródła / Dalsze informacje

*   [1] **Dokumentacja EDIABAS:** Dokumentacja techniczna warstwy komunikacyjnej.

## 12. Dziennik zmian / Wersjonowanie

INPA to narzędzie przestarzałe i nie jest już aktywnie rozwijane ani aktualizowane przez BMW AG.

## 13. Rola

INPA jest używana przez **zaawansowanych techników** oraz **entuzjastów**, którzy potrzebują szybkiego, niskopoziomowego dostępu do pojazdów serii E.

---
*Zobacz także: [Tool32](../tools/tool32.md), [Glosariusz](../glossary.md)*
