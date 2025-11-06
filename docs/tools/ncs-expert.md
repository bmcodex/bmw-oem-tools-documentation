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
