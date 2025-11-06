# AIR (Aftersales Information Research)

## 1. Title and Short Description

**AIR** (Aftersales Information Research) is a key component of the BMW Group's aftersales ecosystem, primarily serving as a repository and search engine for technical and service-related information. It is designed to provide technicians with rapid access to the vast knowledge base required for complex diagnostics and repairs.

## 2. Purpose / Use Cases

AIR's main function is to support the service process by providing on-demand technical documentation.

*   **Technical Documentation:** Access to repair instructions, wiring diagrams, component locations, and technical service bulletins (**TSB**).
*   **Search Engine:** A powerful search tool to quickly find relevant information based on symptoms, fault codes (**DTC**), or component names.
*   **Integration:** Often integrated directly into the **ISTA/D** workflow, allowing technicians to pull up relevant documentation during a guided test plan.

## 3. Supported Vehicle Generations

AIR covers all vehicle generations for which BMW AG provides official service documentation.

## 4. Interfaces & Protocols

AIR is primarily a web-based or network-based service.

*   **Network Access:** Requires a stable network connection to the BMW backend servers.
*   **Integration:** Accessed via the **ISPI Next** platform or directly through a web browser (for authorized users).

## 5. Installation & Access

AIR is a service, not a standalone application.

*   **System Requirements:** Access is typically granted through the **ISPI Next** platform or the **AOS** portal.
*   **Legal Access:** Access is restricted to authorized BMW Group dealers, service partners, and independent operators who have purchased access through **AOS** [1].

## 6. General Workflow / Typical Procedures

1.  **Search:** Technician enters a search query (e.g., a **DTC** code or a symptom).
2.  **Retrieve:** AIR returns a list of relevant documents, repair instructions, and technical bulletins.
3.  **Apply:** The technician uses the information to perform the necessary repair or diagnostic step.

## 7. Key Screens / UI Elements

*   **Search Bar:** The primary interface for querying the knowledge base.
*   **Document Viewer:** Displays repair instructions, often with integrated graphics and step-by-step procedures.

## 8. Safety & Risks

The primary risk is using outdated or incorrect information.

*   **Outdated Information:** Technicians must ensure they are using the latest version of the documentation, as procedures can change with software updates.

## 9. Troubleshooting & Common Errors

| Error | Description | Diagnosis / Solution |
| :--- | :--- | :--- |
| **Search Results Not Found** | The query is too specific or the information is not yet available. | Broaden the search query or check for related **TSB**s. |
| **Access Denied** | User lacks the necessary subscription or authorization. | Verify user credentials and **AOS** subscription status. |

## 10. Examples & Practical Notes

*   **Technical Service Bulletins (TSB):** AIR is the source for all official **TSB**s, which detail known issues and official repair procedures.

## 11. References / Further Reading

*   [1] **BMW Aftersales Online System (AOS):** The portal through which independent operators can purchase access to AIR. *URL Placeholder: https://aos.bmwgroup.com*

## 12. Change Log / Versioning

AIR is continuously updated as new vehicles are released and new technical information becomes available.

## 13. Role

AIR is a **Critical Support Tool** for all BMW service personnel, providing the necessary technical knowledge to perform repairs.

---
*See also: [AOS](../tools/aos.md), [ISTA/D](../tools/ista-d.md), [Glossary](../glossary.md)*
