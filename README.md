# AutomationML Ontology-Design Pattern

## Introduction

The development of software functionalities, or applications in general, that monitor and analyze manufacturing related data in order to improve, support or automate processes, is becoming increasingly important in industry. These applications require several information from different data sources in their context. An application that is planning a maintenance workers daily schedule for instance, requires several information about machine statuses, production plans and inventory, which resides in different systems likes Programmable Logical Controllers (PLC) or Structured Query Language (SQL) databases. Furthermore, manufacturing companies usually run machines and software systems from different vendors or of different ages. The schemata used in such systems do therefore not follow a certain standard, i.e. they are very heterogeneous in their semantics. When building such applications, accessing, searching and understanding the data sources is becoming a very time intensive, manual and error prone procedure that is repeated for every newly build application and for every newly introduced data source. To allow for an eased access, searching and understanding of these heterogeneous data sources, an ontology can be used to integrate all heterogeneous data sources in one schemata. 

This repository contains an ontology of AutomationML. We maintain a whole list of standard-based ontologies, check out these links:
 - [VDI 2206](https://github.com/hsu-aut/IndustrialStandard-ODP-VDI2206)
 - [VDI 2860](https://github.com/hsu-aut/IndustrialStandard-ODP-VDI2860)
 - [VDI 3682](https://github.com/hsu-aut/IndustrialStandard-ODP-VDI3682)
 - [DIN 8580](https://github.com/hsu-aut/IndustrialStandard-ODP-DIN8580)
 - [DIN EN 61360](https://github.com/hsu-aut/IndustrialStandard-ODP-DINEN61360)
 - [WADL](https://github.com/hsu-aut/IndustrialStandard-ODP-WADL)
 - [DIN EN 62264-2](https://github.com/hsu-aut/IndustrialStandard-ODP-DINEN62264-2)
 - [OPC UA](https://github.com/hsu-aut/IndustrialStandard-ODP-OPC-UA)
 - [ISO 22400-2](https://github.com/hsu-aut/IndustrialStandard-ODP-ISO22400-2)
 


## AutomationML

AutomationML (Automation Markup Language) is an open, XML-based standard designed for the comprehensive representation of engineering data in the field of industrial automation. It was developed to address the challenge of integrating heterogeneous engineering tools used throughout the lifecycle of automated production systems.
It offers advantages in numerous aspects: 
 - Interoperability: Different engineering tools from various vendors often use proprietary data formats, making integration difficult. AutomationML aims to standardize data exchange formats to facilitate seamless interoperability between these tools.
 - Data Consistency: Ensuring consistent and error-free data across various engineering phases (e.g., design, implementation, operation) is crucial. AutomationML provides a structured way to maintain data consistency throughout the entire system lifecycle.
 - Complexity Management: Modern automated systems are highly complex, involving numerous components and subsystems. AutomationML helps manage this complexity by offering a clear and standardized method to represent and interconnect different system elements.
 - Flexibility and Extensibility: AutomationML is designed to be flexible and extensible, allowing it to adapt to future requirements and incorporate new technologies and methodologies as they emerge.

This ontology builds upon and extends a previous AutomationML-Ontology, that can be found at https://github.com/i40-Tools/AutomationMLOntology/tree/master.
A preprint describing the design principles and choices can further be found at https://www.semantic-web-journal.net/system/files/swj1855.pdf. 
However, since the inception of the original AutomationML-ontology, the AutomationML standard underwent continuous and significant development, which caused the ontology to become outdated. 
The provided ontology significantly extends the coverage of the previous version and introduced numerous changes to align the ontology to the vocabulary of AutomationML/CAEX v3. 


## Usage

If you want to this ontology design pattern, the easiest way is to directly import it into your ontology via `owl:imports` statements. Make sure to reference a fixed release version so that you can't get surprised by future changes. To do so, click on the branch selection right below the number of commits and select a tag from the dropdown, e.g. v1.4.2. Then navigate to the .owl-file and open the raw file. For this example it would be https://raw.githubusercontent.com/hsu-aut/IndustrialStandard-ODP-AutomationML/v1.0.0/AutomationML.owl. You can use this URL in an `owl:imports` statement of your ontology. If you're having trouble using this URL in a tool like Protégé, try opening your ontology with a text editor and simply inserting your imports manually.
An example of an imports section looks like this:

```xml
<owl:Ontology rdf:about="http://www.hsu-ifa.de/ontologies/capability-model#">
    <owl:versionIRI rdf:resource="http://www.hsu-ifa.de/ontologies/capability-model/1.0.0#"/>
    <owl:imports rdf:resource="https://raw.githubusercontent.com/hsu-aut/IndustrialStandard-ODP-AutomationML/v1.0.0/AutomationML.owl"/>
</owl:Ontology>
```
Of course you can also clone or download this repository and import an ODP from a local copy. The advantage of the first approach is that tools like Protégé or TopBraid Composer will directly use the ontologies from the internet and you can simply increase the version number in case you want to use a newer version of our ODPs.


