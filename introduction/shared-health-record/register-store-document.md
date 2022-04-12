# Register / Store Document

‌

This transaction can be used to register the document metadata and optionally store documents in a SHR or document repository. This transaction can also be used to support storage of vaccine certificates.

| **Workflow Maturity**         | <p>​​<img src="https://lh6.googleusercontent.com/Kxkqfa92YGW3mIOmWio0Twi4YLMA92z6mL1MuFzkx4AWS5CX5zbzWid5z4p2W-e6O66llKpaU0r6lzwyXfhbIiWmkVEuPDy6stX5x5L8uC2DkEXs6qUFX-7xxXTlb9hbkg" alt="">​</p><p><strong>Newly Defined</strong></p> | <p>​</p><ul><li><strong>Workflow is defined by WHO and has OpenHIE ARB approval</strong></li><li><strong>Initial implementations are being considered.</strong></li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| ----------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Standards                     | ​Content                                                                                                                                                                                                                               | <p>​</p><ul><li>The Register / Store Document transaction is based on <a href="https://profiles.ihe.net/ITI/MHD/ITI-65.html#2365412-message-semantics">MHD's Provide Document Bundle transaction [ITI-65]</a>. It can be used store the metadata about a document and optionally store the document itself.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Assumptions and Prerequisites | ​Content                                                                                                                                                                                                                               | <p>​</p><ul><li>The appropriate trust agreements and processes have been put in place for the system sharing the document or the Document Generation Service to provide the documentation to the SHR or document repository.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Actors                        | ​Content                                                                                                                                                                                                                               | <p>​</p><ul><li>Point-of-Care or Document Generation Service (External System) - External system or Point-of-care system generating the document.</li><li>​<a href="https://app.gitbook.com/@openhie/s/arch-spec/~/drafts/-Mkm-SuMPjoXhLjciESU/openhie-component-specifications-1/openhie-interoperability-layer-iol">IOL</a> - The interoperability layer that secures and orchestrates the exchange of information (see OHIE Interoperability layer)</li><li>​<a href="https://app.gitbook.com/@openhie/s/arch-spec/~/drafts/-Mkm-SuMPjoXhLjciESU/openhie-component-specifications-1/openhie-shared-health-record-shr">SHR</a> / Document Repository (or Electronic Vaccination Registry) - The shared health record that serves as a centralized data store for patients’ longitudinal health record and or health documents</li></ul> |

‌

### Interaction Description <a href="#interaction-description" id="interaction-description"></a>

‌

The Interaction Description is stored in the ["Store Health Certificate"](https://worldhealthorganization.github.io/ddcc/transactions.html#store-health-certificate) in the WHO FHIR IG.

References:

* ​[WHO DDCC Workflows](https://worldhealthorganization.github.io/ddcc/workflows.html)​
* ​[Digitize Vaccine Event](https://worldhealthorganization.github.io/ddcc/workflows.html)​

​[PreviousQuery Patient-level Clinical Data Workflow](https://app.gitbook.com/@openhie/s/arch-spec/\~/drafts/-Mkm-SuMPjoXhLjciESU/introduction/shared-health-record/query-patient-level-clinical-data-workflow)[NextRetrieve Document](https://app.gitbook.com/@openhie/s/arch-spec/\~/drafts/-Mkm-SuMPjoXhLjciESU/introduction/shared-health-record/retrieve-document)\