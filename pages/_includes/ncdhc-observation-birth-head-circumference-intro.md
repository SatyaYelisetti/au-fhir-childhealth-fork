**NCDHC Birth Head Circumference Observation Profile**

This profile defines  how to represent birth head circumference in FHIR using a standard SNOMED CT AU code. The profile uses UCUM units of measure. It identifies which core elements, extensions, vocabularies and value sets **SHALL** be present in the resource when using this profile. 
The profile is at draft stage and under review by the Child Health Working Group. 

**Example Usage Scenarios:**

The following are example usage scenarios for the National Child Digital Health interactions
profile:

-   Query for Birth Head Circumference of the baby patient
-   Record Birth Head Circumference of the baby patient


##### Mandatory Data Elements and Terminology


The following data-elements are mandatory (i.e data MUST be present). These are presented below in a simple human-readable explanation. Profile specific guidance and examples are provided as well.  The [**Formal Profile Definition**](#profile) below provides the  formal summary, definitions, and  terminology requirements.  

**Each Observation must have:**

1.  a status  
1.  a code (indicating what was measured)
1.  a subject ([Patient])
1.  a time (indicating when the details were taken)
1.	a performer (detailing who has recorded the details)
1.  a numeric result value and standard UCUM unit (applicable units are defined in the ValueSet: http://hl7.org/fhir/ValueSet/ucum-bodylength)
    -   Note: A reason needs to be supplied in-case there is no numeric result value.

#### Examples

- [Birth Head Circumference ](ncdhc-observation-birth-head-circumference-example.html)


[Patient]: http://build.fhir.org/ig/hl7au/au-fhir-childhealth/StructureDefinition-ncdhc-patient-baby.html