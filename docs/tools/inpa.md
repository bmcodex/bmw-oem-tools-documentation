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
