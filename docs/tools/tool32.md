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
