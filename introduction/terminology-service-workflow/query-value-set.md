# Query Value Set

This transaction allows a PoS, or any OHIE component, to access terminological information in the terminology service to query for Value Sets.  A typical example would be to request the set of Value Sets defined by WHO.

Both external systems and systems inside the HIE may perform this transaction directly with the TS. The sequence diagram below shows the steps that occur for a system using this transaction.  &#x20;

1. Query ValueSets: What Value Sets have a publisher name that contains 'WHO'?

| Workflow Maturity             | <p><img src="https://lh5.googleusercontent.com/Vp6XBRGu-U_Dmd5EKNpCZvEEum0CxOcHOj9NgHh8UMMNLMlXHmLcUE_YWueDRr4uqWLzpPfzSBLJ2k33XQIelLypjQ4wyrD17-t33GtLa8fFxW9AYDvXhiJmBl4VaLgKDg" alt=""></p><p>   <strong>Mature</strong></p> | <p></p><ul><li><strong>One or more OpenHIE implementations of this workflow exist  in one or more countries</strong></li><li><strong>Workflow is defined and ARB approved</strong></li><li><strong>Workflow is supported by mature standards</strong></li></ul>                                                                                                                                                                                                                                                                                                                                                         |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Standards                     |                                                                                                                                                                                                                                 | <p>The FHIR Value Sets and supported search parameters are defined in: <a href="https://www.hl7.org/fhir/valueset.html">https://www.hl7.org/fhir/valueset.html</a>. Searching in FHIR is described in <a href="https://www.hl7.org/fhir/search.html">https://www.hl7.org/fhir/search.html</a>. HL7 FHIR Specifications v3.0 or higher support Value Set. The response is a Bundle of Value Set Resources satisfying the search parameters.</p><p>This workflow implements the IHE IT Infrastructure Technical Framework Supplement - Sharing Valuesets, Codes, and Maps (SVCM) Transaction: Query Value Set ITI-Y1.</p> |
| Assumptions and Prerequisites |                                                                                                                                                                                                                                 | The required ValueSets have been preloaded into the Terminology Service.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Actors                        |                                                                                                                                                                                                                                 | <p></p><ul><li>PoS - The point-of-service system  or other HIE component that is that is querying for Value Sets.   </li><li>TS - Stores the curated, official version of the Value Sets for the health system.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                               |

## Interaction Description&#x20;

The following is a description of the interaction steps.

![](https://lh6.googleusercontent.com/5w9uqajSsiAUJoBPuCBdcY9HTiQvLfb0Op-Xy78GJxS-TQK7i6\_fMvIEtqOAJ1\_bQkCgsVeWGX2FM--QUe5w0gqi41U80adN\_dGfNGzjU7YScpbF5gL9xCph45eKbC-vYw)

| # | Interaction              | Data                                                                                                                                         | Transaction Options    |
| - | ------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------- |
| 1 | Query Value Set request  | <p>The Value Set search request is triggered by a PoS or other HIE component.</p><p>Input: A set of FHIR search parameters.</p>              | FHIR ValueSet Resource |
| 2 | Query Value Set response | <p>The response is sent back to the requesting system. </p><p>Output: a Bundle of ValueSet Resources that satisfy the search parameters.</p> | FHIR ValueSet Resource |