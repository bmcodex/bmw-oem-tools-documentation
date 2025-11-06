# 🌍 Wybierz język / Choose language

[🇵🇱 Polski](#-polska-wersja) | [🇬🇧 English](#-english-version)

#

# 🇬🇧 English version
# Tool32

## 1. Title and Short Description

**Tool32** is a low-level, command-line interface tool developed by BMW, part of the **EDIABAS** toolset. It allows for direct, unguided communication with individual Electronic Control Units (**ECU**) using specific job files (**.PRG**). It is a powerful, yet dangerous, tool that bypasses the guided procedures of **ISTA/D** and **ISTA/P**.

## 2. Purpose / Use Cases

Tool32 is used for highly specific, low-level service and diagnostic functions.

*   **Direct ECU Communication:** Sending specific commands (jobs) directly to an **ECU** without the need for a guided test plan.
*   **Service Functions:** Performing functions not exposed in higher-level tools (e.g., resetting specific counters, activating components in a non-standard way).
*   **Reading Low-Level Data:** Accessing raw data and internal status variables of an **ECU**.
*   **Troubleshooting:** Advanced diagnosis of communication issues or specific **ECU** faults.

## 3. Supported Vehicle Generations

Tool32 supports all vehicle generations that communicate via the **EDIABAS** interface, which includes E, F, and G series.

| Generation | Communication Support | Notes |
| :--- | :--- | :--- |
| **E-series** | D-CAN, K-Line | Full functionality |
| **F/G-series** | ENET, ICOM | Requires proper **EDIABAS** configuration for **ENET** communication. |

## 4. Interfaces & Protocols

Tool32 relies on the **EDIABAS** interface for communication.

*   **K-DCAN Cable:** Used for E-series vehicles.
*   **ENET Cable:** Used for F/G-series vehicles.
*   **ICOM:** Recommended for stable communication across all generations.
*   **Protocols:** K-Line, D-CAN, and ENET.

## 5. Installation & Access

Tool32 is part of the older **EDIABAS** toolset.

*   **System Requirements:** Requires a Windows operating system and the **EDIABAS** interface to be correctly configured.
*   **Legal Access:** Like other EDIABAS tools, Tool32 is largely superseded by ISTA/D and E-SYS and is not actively distributed by BMW AG for general service use.

## 6. General Workflow / Typical Procedures

1.  **Connect Interface:** Connect the vehicle interface (**K-DCAN**, **ENET**, or **ICOM**).
2.  **Launch Tool32:** Launch the application.
3.  **Load Job File:** Load the specific **ECU** job file (**.PRG**) (e.g., `DME.PRG` for engine electronics).
4.  **Select Job:** Select the desired job from the list (e.g., `steuern_reset_adaptionen` - reset adaptations).
5.  **Execute Job:** Execute the job. The results (status, return values) are displayed in the results window.

## 7. Key Screens / UI Elements

*   **Job Window:** Displays the list of available jobs for the loaded **ECU** file.
*   **Results Window:** Displays the output, status, and return values after a job is executed.
*   **Arguments Window:** Used to input required parameters for certain jobs.

## 8. Safety & Risks

Tool32 is considered a high-risk tool due to its direct, unguided access to **ECU** functions.

*   **Unguided Access:** There are no safety checks or guided procedures. Executing the wrong job can lead to functional errors, component damage, or even bricking the **ECU**.
*   **Voltage:** Stable voltage is essential to prevent communication errors during job execution.

## 9. Troubleshooting & Common Errors

| Error | Description | Diagnosis / Solution |
| :--- | :--- | :--- |
| **Error: API-0001** | Communication error with the **EDIABAS** interface. | Check the **EDIABAS** configuration and ensure the interface is properly connected. |
| **Job Not Found** | The selected job is not available in the loaded **.PRG** file. | Ensure the correct **ECU** job file is loaded and the job name is spelled correctly. |

## 10. Examples & Practical Notes

*   **Resetting FRM Short Circuit Counter:** Used to reset the short circuit counter in the Footwell Module (**FRM**) after a faulty light bulb has been replaced. This function is often not available in ISTA/D.
*   **Reading Injector Data:** Can be used to read detailed injector data and status that may be hidden in higher-level tools.

## 11. References / Further Reading

*   [1] **EDIABAS Documentation:** Technical documentation for the underlying communication layer.

## 12. Change Log / Versioning

Tool32 is a legacy tool and is no longer actively developed. Its functionality is now often integrated into the service functions of **ISTA/D** or performed via **E-SYS**.

## 13. Role

Tool32 is used by **Expert Users** and **Engineers** for specialized, low-level diagnostics and service functions.

---
*See also: [INPA](../tools/inpa.md), [NCS Expert](../tools/ncs-expert.md), [Glossary](../glossary.md)*


# 🇵🇱 Polska wersja
# Tool32

## 1. Tytuł i krótki opis

**Tool32** to niskopoziomowe narzędzie wiersza poleceń opracowane przez BMW, będące częścią pakietu **EDIABAS**. Umożliwia bezpośrednią, niekierowaną komunikację z poszczególnymi modułami elektronicznymi (**ECU**) przy użyciu plików zadań (**.PRG**). To potężne, ale ryzykowne narzędzie, które omija prowadzone procedury znane z **ISTA/D** i **ISTA/P**.

## 2. Cel / Zastosowania

Tool32 służy do zaawansowanych, niskopoziomowych czynności diagnostycznych i serwisowych.

*   **Bezpośrednia komunikacja z ECU:** Wysyłanie określonych komend (tzw. *jobs*) bez konieczności korzystania z planów testowych.  
*   **Funkcje serwisowe:** Wykonywanie czynności niedostępnych w wyższych narzędziach (np. reset liczników błędów, aktywacja komponentów w niestandardowy sposób).  
*   **Odczyt danych niskopoziomowych:** Dostęp do surowych danych i wewnętrznych statusów modułów **ECU**.  
*   **Diagnostyka problemów:** Ustalanie źródła błędów komunikacyjnych lub specyficznych usterek modułów.  

## 3. Obsługiwane generacje pojazdów

Tool32 obsługuje wszystkie generacje pojazdów, które komunikują się poprzez interfejs **EDIABAS**, w tym serie E, F i G.

| Generacja | Obsługiwane interfejsy | Uwagi |
| :--- | :--- | :--- |
| **E-series** | D-CAN, K-Line | Pełna funkcjonalność |
| **F/G-series** | ENET, ICOM | Wymaga poprawnej konfiguracji **EDIABAS** dla komunikacji **ENET** |

## 4. Interfejsy i protokoły

Tool32 opiera się na interfejsie **EDIABAS**.

*   **Kabel K-DCAN:** Dla pojazdów serii E.  
*   **Kabel ENET:** Dla pojazdów serii F i G.  
*   **ICOM:** Zalecany dla stabilnej komunikacji w każdej generacji.  
*   **Protokoły:** K-Line, D-CAN, ENET.  

## 5. Instalacja i dostęp

Tool32 jest częścią starszego zestawu narzędzi **EDIABAS**.

*   **Wymagania systemowe:** System Windows z poprawnie skonfigurowanym interfejsem **EDIABAS**.  
*   **Dostęp legalny:** Tak jak inne narzędzia EDIABAS, Tool32 został zastąpiony przez **ISTA/D** i **E-SYS** i nie jest już oficjalnie dystrybuowany przez BMW AG.  

## 6. Ogólny przebieg pracy / Typowe procedury

1.  **Podłącz interfejs:** Podłącz **K-DCAN**, **ENET** lub **ICOM**.  
2.  **Uruchom Tool32:** Otwórz aplikację.  
3.  **Załaduj plik zadań:** Wczytaj odpowiedni plik **.PRG** (np. `DME.PRG` dla sterownika silnika).  
4.  **Wybierz zadanie:** Wskaż żądaną funkcję z listy (np. `steuern_reset_adaptionen` – reset adaptacji).  
5.  **Wykonaj zadanie:** Uruchom komendę – wynik (status, wartości zwrotne) pojawi się w oknie wyników.  

## 7. Kluczowe ekrany / Elementy interfejsu

*   **Okno zadań (Job Window):** Lista wszystkich dostępnych zadań dla załadowanego pliku **ECU**.  
*   **Okno wyników (Results Window):** Pokazuje status i wyniki po wykonaniu zadania.  
*   **Okno argumentów (Arguments Window):** Służy do wprowadzania parametrów wymaganych przez niektóre komendy.  

## 8. Bezpieczeństwo i ryzyka

Tool32 jest narzędziem wysokiego ryzyka ze względu na brak zabezpieczeń i bezpośredni dostęp do funkcji modułów.

*   **Brak prowadzenia użytkownika:** Nie ma żadnych zabezpieczeń ani ostrzeżeń — błędne zadanie może uszkodzić moduł, komponent lub nawet zablokować **ECU**.  
*   **Stabilne napięcie:** Niezbędne do uniknięcia błędów komunikacji podczas wykonywania komend.  

## 9. Rozwiązywanie problemów / Typowe błędy

| Błąd | Opis | Diagnoza / Rozwiązanie |
| :--- | :--- | :--- |
| **Error: API-0001** | Błąd komunikacji z interfejsem **EDIABAS**. | Sprawdź konfigurację **EDIABAS** i poprawność połączenia interfejsu. |
| **Job Not Found** | Wybrane zadanie nie istnieje w załadowanym pliku **.PRG**. | Upewnij się, że wczytano poprawny plik **ECU** i wpisano właściwą nazwę zadania. |

## 10. Przykłady i uwagi praktyczne

*   **Reset licznika zwarć FRM:** Używane do zresetowania licznika zwarć w module świateł **FRM** po wymianie żarówki – funkcja często niedostępna w ISTA/D.  
*   **Odczyt danych wtryskiwaczy:** Pozwala odczytać szczegółowe dane i statusy wtryskiwaczy, niedostępne w wyższych narzędziach.  

## 11. Źródła / Dalsze informacje

*   [1] **Dokumentacja EDIABAS:** Oficjalne materiały techniczne dotyczące warstwy komunikacyjnej.  

## 12. Dziennik zmian / Wersjonowanie

Tool32 to narzędzie archiwalne, które nie jest już rozwijane. Jego funkcje są obecnie zintegrowane z **ISTA/D** lub realizowane przez **E-SYS**.  

## 13. Rola

Tool32 jest używany przez **ekspertów i inżynierów** do specjalistycznych, niskopoziomowych czynności diagnostycznych i serwisowych.  

---
*Zobacz także: [INPA](../tools/inpa.md), [NCS Expert](../tools/ncs-expert.md), [Glosariusz](../glossary.md)*
