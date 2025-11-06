# 🌍 Wybierz język / Choose language

[🇵🇱 Polski](#-polska-wersja) | [🇬🇧 English](#-english-version)

#


# 🇬🇧 English version
# WinKFP (Windows Comfort Flash Program)

## 1. Title and Short Description

**WinKFP** (Windows Comfort Flash Program) is a legacy BMW Group software tool used for **programming** (flashing) individual Electronic Control Units (**ECU**) in **E-series** vehicles. It operates at a low level, allowing the user to select a specific **ECU** and flash it with a chosen program file (**.PRG**) and data file (**.DAT**).

## 2. Purpose / Use Cases

WinKFP is a dedicated tool for flashing **ECU**s, primarily used for:

*   **Firmware Updates:** Updating the software of a single **ECU** to the latest version.
*   **Module Replacement:** Flashing a new, blank **ECU** with the correct software for the vehicle.
*   **Downgrading:** In some cases, WinKFP can be used to flash an older software version onto an **ECU**.

## 3. Supported Vehicle Generations

WinKFP is a tool for the older **E-series** vehicles. It has been largely replaced by **ISTA/P** and **E-SYS** for newer generations.

| Generation | Programming Scope | Required Interface |
| :--- | :--- | :--- |
| **E-series** | Full programming of individual **ECU**s | K-DCAN, ICOM (D-CAN) |
| **F-series** | Not Supported | Programming is performed using **ISTA/P** or **E-SYS**. |

## 4. Interfaces & Protocols

WinKFP relies on the **EDIABAS** interface for communication.

*   **K-DCAN Cable:** The standard interface for E-series vehicles.
*   **ICOM (D-CAN):** Provides a more stable connection, which is highly recommended for programming operations.
*   **Protocols:** K-Line and D-CAN.

## 5. Installation & Access

WinKFP is part of the older **EDIABAS** toolset.

*   **System Requirements:** Requires a Windows operating system and the **EDIABAS** interface to be correctly configured.
*   **Legal Access:** Like other EDIABAS tools, WinKFP is largely superseded and not actively distributed by BMW AG for general service use.

## 6. General Workflow / Typical Procedures

1.  **Connect Interface:** Connect the vehicle interface (**K-DCAN** or **ICOM**) and a **stable power supply** (13.5V+).
2.  **Select ECU:** Choose the **ECU** family (e.g., **DME** for engine electronics).
3.  **Select Program:** Select the specific program file (**.PRG**) to be flashed.
4.  **Check ZB-Number:** Verify the correct ZB-Number (Assembly Part Number) for the target **ECU**.
5.  **Program:** Execute the programming process. **DO NOT INTERRUPT.**

## 7. Key Screens / UI Elements

*   **Comfort Mode:** Allows flashing based on the **VIN** or ZB-Number, simplifying the process.
*   **Expert Mode:** Allows manual selection of the **ECU** and program file.

## 8. Safety & Risks

WinKFP is a high-risk tool due to its low-level access and the critical nature of programming.

*   **Power Supply:** **CRITICAL.** A voltage drop during programming will almost certainly lead to a failed flash and a **bricked ECU**. A stable power supply is mandatory.
*   **Interruption:** The programming process **MUST NOT** be interrupted.
*   **ZB-Number:** Flashing an **ECU** with the wrong ZB-Number can cause severe functional errors.

## 9. Troubleshooting & Common Errors

| Error | Description | Diagnosis / Solution |
| :--- | :--- | :--- |
| **Error 200: IFH-0009: No Response from Control Unit** | WinKFP cannot establish communication. | Check the **EDIABAS** configuration. Ensure the interface is properly connected and the vehicle's ignition is on. |
| **Error 211: Program Status Invalid** | The selected program file is incorrect or incompatible with the **ECU**. | Verify the ZB-Number and ensure the correct **SP-Daten** (programming data) are installed. |

## 10. Examples & Practical Notes

*   **DME Update:** Used to update the Digital Motor Electronics (**DME**) software to the latest version.
*   **Module Initialization:** Used to flash a brand new, unprogrammed **ECU** before it can be coded with **NCS Expert**.

## 11. References / Further Reading

*   [1] **BMW SP-Daten:** The official data files containing the program and data files for all **ECU**s.

## 12. Change Log / Versioning

WinKFP is a legacy tool and is no longer actively developed. Updates are limited to community-driven **SP-Daten** file updates.

## 13. Role

WinKFP is used by **Advanced Technicians** and **Enthusiasts** for low-level programming of E-series **ECU**s.

---
*See also: [NCS Expert](../tools/ncs-expert.md), [Tool32](../tools/tool32.md), [Glossary](../glossary.md)*



# 🇵🇱 Polska wersja
# WinKFP (Windows Comfort Flash Program)

## 1. Tytuł i krótki opis

**WinKFP** (Windows Comfort Flash Program) to starsze oprogramowanie BMW Group używane do **programowania** (flashowania) poszczególnych sterowników elektronicznych (**ECU**) w pojazdach serii **E**. Działa na niskim poziomie, umożliwiając użytkownikowi wybór konkretnego **ECU** i wgranie do niego odpowiedniego pliku programu (**.PRG**) oraz pliku danych (**.DAT**).

## 2. Cel / Zastosowania

WinKFP to dedykowane narzędzie do flashowania sterowników (**ECU**), wykorzystywane głównie do:

*   **Aktualizacji oprogramowania:** Wgrywanie najnowszej wersji oprogramowania do pojedynczego **ECU**.
*   **Wymiany modułu:** Programowanie nowego, pustego **ECU** właściwym oprogramowaniem dla danego pojazdu.
*   **Downgrade’u:** W niektórych przypadkach WinKFP pozwala wgrać starszą wersję oprogramowania do **ECU**.

## 3. Obsługiwane generacje pojazdów

WinKFP przeznaczony jest dla starszych pojazdów z serii **E**. W nowszych generacjach został zastąpiony przez **ISTA/P** i **E-SYS**.

| Generacja | Zakres programowania | Wymagany interfejs |
| :--- | :--- | :--- |
| **E-seria** | Pełne programowanie pojedynczych **ECU** | K-DCAN, ICOM (D-CAN) |
| **F-seria** | Nieobsługiwana | Programowanie realizowane przez **ISTA/P** lub **E-SYS**. |

## 4. Interfejsy i protokoły

WinKFP korzysta z interfejsu **EDIABAS** do komunikacji.

*   **K-DCAN Cable:** Standardowy interfejs dla serii E.  
*   **ICOM (D-CAN):** Zapewnia stabilniejsze połączenie, szczególnie zalecane przy programowaniu.  
*   **Protokoły:** K-Line i D-CAN.

## 5. Instalacja i dostęp

WinKFP jest częścią starszego pakietu narzędzi **EDIABAS**.

*   **Wymagania systemowe:** System operacyjny Windows z poprawnie skonfigurowanym interfejsem **EDIABAS**.  
*   **Dostępność prawna:** Jak inne narzędzia EDIABAS, WinKFP nie jest już oficjalnie dystrybuowany przez BMW AG do ogólnego użytku serwisowego.

## 6. Ogólny przebieg pracy / typowe procedury

1.  **Podłącz interfejs:** Podłącz **K-DCAN** lub **ICOM** oraz **stabilne zasilanie** (min. 13,5V).  
2.  **Wybierz ECU:** Wybierz rodzinę sterowników, np. **DME** dla elektroniki silnika.  
3.  **Wybierz program:** Wskaż odpowiedni plik programu (**.PRG**) do flashowania.  
4.  **Sprawdź numer ZB:** Zweryfikuj poprawność numeru ZB (numer części oprogramowania) dla wybranego **ECU**.  
5.  **Programuj:** Rozpocznij proces programowania. **NIE PRZERYWAJ PROCESU!**

## 7. Kluczowe elementy interfejsu

*   **Tryb Comfort:** Umożliwia programowanie na podstawie numeru **VIN** lub numeru **ZB**, co upraszcza proces.  
*   **Tryb Expert:** Umożliwia ręczny wybór sterownika i pliku programu.

## 8. Bezpieczeństwo i ryzyko

WinKFP to narzędzie wysokiego ryzyka ze względu na niskopoziomowy dostęp i krytyczny charakter procesu programowania.

*   **Zasilanie:** **KLUCZOWE!** Spadek napięcia podczas programowania prawie zawsze prowadzi do nieudanego flasha i **uszkodzenia ECU**.  
*   **Przerwanie procesu:** Proces programowania **NIE MOŻE** zostać przerwany.  
*   **Numer ZB:** Wgranie niepoprawnego numeru ZB może spowodować poważne błędy w działaniu sterownika.

## 9. Rozwiązywanie problemów i typowe błędy

| Błąd | Opis | Diagnoza / Rozwiązanie |
| :--- | :--- | :--- |
| **Error 200: IFH-0009: No Response from Control Unit** | Brak komunikacji z jednostką sterującą. | Sprawdź konfigurację **EDIABAS**, połączenie interfejsu i stan zapłonu. |
| **Error 211: Program Status Invalid** | Wybrany plik programu jest niepoprawny lub niezgodny z **ECU**. | Zweryfikuj numer ZB i upewnij się, że zainstalowano odpowiednie dane **SP-Daten**. |

## 10. Przykłady i notatki praktyczne

*   **Aktualizacja DME:** Aktualizacja oprogramowania elektronicznego sterownika silnika (**DME**) do najnowszej wersji.  
*   **Inicjalizacja modułu:** Programowanie nowego, nieużywanego **ECU**, które następnie można zakodować w **NCS Expert**.

## 11. Źródła / dalsza lektura

*   [1] **BMW SP-Daten:** Oficjalne pakiety danych zawierające pliki programów i danych dla wszystkich **ECU**.

## 12. Historia zmian / wersjonowanie

WinKFP to narzędzie archiwalne, nie jest już rozwijane. Aktualizacje ograniczają się do społecznościowych aktualizacji plików **SP-Daten**.

## 13. Rola

WinKFP jest używany przez **zaawansowanych techników** i **entuzjastów** do niskopoziomowego programowania sterowników serii **E**.

---
*Zobacz także: [NCS Expert](../tools/ncs-expert.md), [Tool32](../tools/tool32.md), [Słownik](../glossary.md)*
