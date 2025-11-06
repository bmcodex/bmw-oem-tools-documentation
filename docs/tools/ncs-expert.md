# 🌍 Wybierz język / Choose language

[🇵🇱 Polski](#-polska-wersja) | [🇬🇧 English](#-english-version)

#

# 🇬🇧 English version
# NCS Expert (Non-Coding Software Expert)

## 1. Title and Short Description

**NCS Expert** (Non-Coding Software Expert) is a legacy BMW Group software tool used for **coding** and customizing the Electronic Control Units (**ECU**) of **E-series** vehicles. It allows advanced users to read the current vehicle configuration and write new parameters to the **ECU**s using profile-based coding files.

## 2. Purpose / Use Cases

NCS Expert is a powerful, low-level tool for modifying vehicle features.

*   **Custom Coding:** Activating or deactivating specific functions (e.g., digital speed display, cornering lights, seat belt warnings).
*   **Module Replacement:** Coding a new or used **ECU** to match the vehicle's **VO** (Vehicle Order).
*   **Profile-Based Coding:** Using different profiles (e.g., Expert Mode, Manipulation) to control the level of coding performed.

## 3. Supported Vehicle Generations

NCS Expert is exclusively a tool for the older **E-series** vehicles. It is not compatible with F-series and newer, which use **E-SYS** for coding.

| Generation | Communication Support | Notes |
| :--- | :--- | :--- |
| **E-series** | D-CAN, K-Line | Full functionality |
| **F-series** | Not Supported | Coding is performed using **E-SYS**. |

## 4. Interfaces & Protocols

NCS Expert relies on the older communication protocols and the **EDIABAS** interface.

*   **K-DCAN Cable:** The standard interface for NCS Expert, supporting both **K-Line** and **D-CAN**.
*   **Protocols:** K-Line (ISO 9141) and D-CAN (ISO 15765).

## 5. Installation & Access

NCS Expert is part of the older **EDIABAS** toolset.

*   **System Requirements:** Requires a Windows operating system (typically XP/7) and the **EDIABAS** interface to be correctly configured.
*   **Legal Access:** Like INPA, NCS Expert is largely superseded by **ISTA/P** and **E-SYS** and is not actively distributed by BMW AG for general service use.

## 6. General Workflow / Typical Procedures

1.  **Connect K-DCAN:** Connect the K-DCAN cable to the vehicle and the service PC.
2.  **Launch NCS Expert:** Select the appropriate profile (e.g., **Expert Mode**).
3.  **Select Chassis:** Select the correct chassis code (e.g., E90).
4.  **Select ECU:** Choose the **ECU** to be coded (e.g., **CAS**, **FRM**).
5.  **Read ECU:** Read the current coding data (**FSW_PSW.TRC** file).
6.  **Edit Data:** Edit the coding parameters in the trace file (or use a pre-modified **.MAN** file).
7.  **Code ECU:** Write the modified data back to the **ECU**.

## 7. Key Screens / UI Elements

*   **Profile Selection:** Determines the coding behavior (e.g., reading only, full coding).
*   **Chassis Selection:** Used to specify the vehicle model.
*   **Job Selection:** Used to select the specific coding operation (e.g., `SG_CODIEREN` - Code ECU).

## 8. Safety & Risks

NCS Expert is a high-risk tool due to its low-level access and lack of guided procedures.

*   **Bricking Risk:** Incorrect coding or interruption during the write process can permanently damage the **ECU**.
*   **VO Mismatch:** Coding an **ECU** with the wrong **VO** can lead to functional errors and warning lights.
*   **Backup:** Always save the original coding data (**FSW_PSW.TRC**) before making any changes.

## 9. Troubleshooting & Common Errors

| Error | Description | Diagnosis / Solution |
| :--- | :--- | :--- |
| **VIN is Faulty** | NCS Expert cannot read the **VIN** or the **VO**. | Check the **EDIABAS** configuration. Ensure the **K-DCAN** cable is properly connected and the vehicle's ignition is on. |
| **COAPI-1020: Error in ECU-ID** | NCS Expert cannot identify the selected **ECU**. | Ensure the correct chassis and **ECU** are selected. Update the **DATEN** files (coding data). |

## 10. Examples & Practical Notes

*   **Digital Speedometer:** Activating the digital speed display in the instrument cluster (**KOMBI**).
*   **Angel Eyes Brightness:** Adjusting the brightness of the daytime running lights (**FRM** module).

## 11. References / Further Reading

*   [1] **BMW Coding Forums:** Community-driven resources are often the only source for specific coding parameters.

## 12. Change Log / Versioning

NCS Expert is a legacy tool and is no longer actively developed. Updates are limited to community-driven **DATEN** file updates.

## 13. Role

NCS Expert is used by **Advanced Enthusiasts** and **Specialized Technicians** for deep customization of E-series vehicles.

---
*See also: [INPA](../tools/inpa.md), [Tool32](../tools/tool32.md), [Glossary](../glossary.md)*




# 🇵🇱 Polska wersja
# NCS Expert (Non-Coding Software Expert)

## 1. Tytuł i krótki opis

**NCS Expert** (Non-Coding Software Expert) to starsze oprogramowanie Grupy BMW służące do **kodowania** i personalizacji modułów elektronicznych (**ECU**) w pojazdach serii **E**. Umożliwia zaawansowanym użytkownikom odczytanie aktualnej konfiguracji pojazdu oraz zapis nowych parametrów do modułów **ECU** przy użyciu plików profili kodowania.

## 2. Cel / Zastosowania

NCS Expert to potężne, niskopoziomowe narzędzie do modyfikowania funkcji pojazdu.

*   **Kodowanie niestandardowe:** Aktywacja lub dezaktywacja wybranych funkcji (np. cyfrowy prędkościomierz, światła doświetlające zakręty, ostrzeżenie o pasach bezpieczeństwa).  
*   **Wymiana modułu:** Kodowanie nowego lub używanego **ECU** w celu dopasowania go do **VO** (Vehicle Order) pojazdu.  
*   **Kodowanie profilowe:** Używanie różnych profili (np. *Expert Mode*, *Manipulation*) do kontroli zakresu i sposobu kodowania.  

## 3. Obsługiwane generacje pojazdów

NCS Expert działa wyłącznie z pojazdami **E-series**. Nie jest kompatybilny z nowszymi modelami (seria F i G), w których używa się programu **E-SYS**.

| Generacja | Obsługiwane protokoły | Uwagi |
| :--- | :--- | :--- |
| **E-series** | D-CAN, K-Line | Pełna funkcjonalność |
| **F-series** | Nieobsługiwana | Kodowanie odbywa się przez **E-SYS** |

## 4. Interfejsy i protokoły

NCS Expert wykorzystuje starsze protokoły komunikacyjne oraz interfejs **EDIABAS**.

*   **Kabel K-DCAN:** Standardowy interfejs do połączenia z pojazdem, obsługujący zarówno **K-Line**, jak i **D-CAN**.  
*   **Protokoły:** K-Line (ISO 9141) i D-CAN (ISO 15765).  

## 5. Instalacja i dostęp

NCS Expert jest częścią starszego zestawu narzędzi **EDIABAS**.

*   **Wymagania systemowe:** System Windows (zazwyczaj XP lub 7) oraz poprawnie skonfigurowany interfejs **EDIABAS**.  
*   **Dostęp legalny:** Oprogramowanie to zostało zastąpione przez **ISTA/P** i **E-SYS**, dlatego nie jest już oficjalnie dystrybuowane przez BMW AG.  

## 6. Ogólny przebieg pracy / Typowe procedury

1.  **Podłącz K-DCAN:** Podłącz kabel do pojazdu i komputera serwisowego.  
2.  **Uruchom NCS Expert:** Wybierz odpowiedni profil (np. **Expert Mode**).  
3.  **Wybierz podwozie:** Określ kod serii (np. E90).  
4.  **Wybierz moduł:** Wskaż moduł **ECU** do kodowania (np. **CAS**, **FRM**).  
5.  **Odczytaj moduł:** Pobierz aktualne dane kodowania (**FSW_PSW.TRC**).  
6.  **Edytuj dane:** Zmień parametry w pliku śledzenia lub użyj gotowego pliku **.MAN**.  
7.  **Zakoduj moduł:** Zapisz zmodyfikowane dane do **ECU**.  

## 7. Kluczowe ekrany / Elementy interfejsu

*   **Wybór profilu:** Określa sposób pracy (np. tylko odczyt, pełne kodowanie).  
*   **Wybór podwozia:** Pozwala zdefiniować typ pojazdu.  
*   **Wybór zadania (Job):** Określa konkretną operację (np. `SG_CODIEREN` – kodowanie modułu).  

## 8. Bezpieczeństwo i ryzyka

NCS Expert jest narzędziem o wysokim ryzyku, ponieważ zapewnia bezpośredni dostęp do modułów bez procedur ochronnych.

*   **Ryzyko uszkodzenia modułu:** Przerwanie procesu zapisu lub błędne dane mogą trwale uszkodzić **ECU**.  
*   **Niezgodność VO:** Kodowanie z użyciem niewłaściwego **VO** może powodować błędy funkcjonalne i kontrolki ostrzegawcze.  
*   **Kopia zapasowa:** Zawsze należy zapisać oryginalny plik kodowania (**FSW_PSW.TRC**) przed wprowadzeniem zmian.  

## 9. Rozwiązywanie problemów / Typowe błędy

| Błąd | Opis | Diagnoza / Rozwiązanie |
| :--- | :--- | :--- |
| **VIN is Faulty** | Program nie może odczytać numeru VIN lub VO. | Sprawdź konfigurację **EDIABAS**, połączenie kabla **K-DCAN** oraz czy zapłon jest włączony. |
| **COAPI-1020: Error in ECU-ID** | Program nie może zidentyfikować wybranego modułu **ECU**. | Upewnij się, że wybrano poprawne podwozie i moduł. Zaktualizuj pliki **DATEN**. |

## 10. Przykłady i uwagi praktyczne

*   **Cyfrowy prędkościomierz:** Aktywacja cyfrowego wyświetlania prędkości w zestawie wskaźników (**KOMBI**).  
*   **Jasność ringów:** Zmiana jasności świateł do jazdy dziennej (**FRM**).  

## 11. Źródła / Dalsze informacje

*   [1] **BMW Coding Forums:** Społecznościowe źródła wiedzy o parametrach kodowania i plikach profili.  

## 12. Dziennik zmian / Wersjonowanie

NCS Expert to narzędzie archiwalne i nie jest już rozwijane. Aktualizacje ograniczają się do społecznościowych aktualizacji plików **DATEN**.  

## 13. Rola

NCS Expert jest używany przez **zaawansowanych entuzjastów** oraz **specjalistycznych techników** do głębokiej personalizacji pojazdów serii E.  

---
*Zobacz także: [INPA](../tools/inpa.md), [Tool32](../tools/tool32.md), [Glosariusz](../glossary.md)*
