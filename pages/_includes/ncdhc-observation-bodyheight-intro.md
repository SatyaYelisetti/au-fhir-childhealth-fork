To allow delivery by vendors in the POC timelines, an additional tactical profile for vital signs is built that only requires SCT – this will only be enabled on a vendor by vendor basis for the pilot with vendors encouraged to use the FHIR conformance profile unless not practical for the POC . On receipt of a measurement using this profile the data hub will enrich the message with the respective SNOMED code to ensure outbound messaging adheres to the FHIR conformance profiles. The use of this non conformance profile will be re-visited at the end of the POC.

#### Examples

- [Birth Length (SNOMED Only)](ncdhc-observation-bodyheight-example.html)