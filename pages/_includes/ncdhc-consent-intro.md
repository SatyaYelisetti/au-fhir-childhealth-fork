**NCDHC Consent Profile**

This profile is used to represent various administrative and operational consent applicable to NCDHC program using [Consent] resource. The profile is at draft stage and under review by the Child Health Working Group. 

**Example Usage Scenarios:**

The following are example usage scenarios for the National Child Digital Health interactions
profile:

-   Query for Consent
-   Register Consent
-   Update Consent

##### Mandatory Data Elements and Terminology


The following data-elements are mandatory (i.e data MUST be present). These are presented below in a simple human-readable explanation.  Profile specific guidance and examples are provided as well.  The [**Formal Profile Definition**](#profile) below provides the  formal summary, definitions, and  terminology requirements.  

**Each Consent instance must have:**

1.  a status  
1.  a category
1.  a patient
1.  a date confirming when this Consent was created or indexed
1.  a policy reference or a policyRule reference SHOULD be provided.

**Profile specific implementation guidance:**

* Client System can only query 'active' Consents. Server will only provide the status of the Consent along with the Patient reference if the search is successful. No details about the actual Consent will be provided to the external system.
* Search can be performed only by providing the Consent category and the patient in context. 
* Optionally client system can provide reference to the 'consentor' and/or 'date' to perform more filtering on the search. 
* Server may provide the reference to the relevant Health Interaction instances using the Consent.data element. 'related ' SHALL be used as Consent.data.meaning.  


##### Consent Category
---
<table class="grid">  
  <tbody>
    <tr>
      <td>Defining URL:</td>  
	  <td>http://hl7.org.au/fhir/ch/v1/ValueSet/ncdhc-consent-category</td>		  
    </tr>
	<tr>
      <td>Name:</td> 
	  <td>NCDHC Consent Category Codes</td>  	  
    </tr>	
  </tbody>
</table>

The table below provides the details of the codes applicable to NCDHC system:
<table class="grid">
  <thead>
    <tr>
      <th>Code</th>
      <th>System</th>
      <th>Display</th>
      <th>Definition</th>	  
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>NBCR</td>
      <td>http://hl7.org.au/fhir/ch/v1/CodeSystem/ncdhc-consent-category</td>
      <td>Newborn Record Create Consent</td>
      <td>Consent for the creation of a Child Health record on the birth of a child. This will be held against the person having the parental responsibility of the child at birth, typically the mother</td>	  
    </tr>
	<tr>
      <td>CROPT</td>
      <td>http://hl7.org.au/fhir/ch/v1/CodeSystem/ncdhc-consent-category</td>
      <td>Child Digital Health Record Operation Consent</td>
      <td>Consent for a child to have a operative child digital health record</td>	  
    </tr>
  </tbody>
</table>

---



#### Examples

- [Consent from Expected Mother to have a record created when the child is born](Consent-expected-mother-for-child.html)
- [Child Consent](Consent-child.html)

[Consent]: http://hl7.org/fhir/STU3/consent.html
[extensible]: http://hl7.org/fhir/terminologies.html#extensible
[General Guidance Section]: definitions.html

