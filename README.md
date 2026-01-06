# AutomationML Ontology Design Pattern

## Overview

AutomationML (Automation Markup Language) is an open, XML-based standard (IEC 62714) designed for the comprehensive representation of engineering data in the field of industrial automation. It was developed to address the challenge of integrating heterogeneous engineering tools used throughout the lifecycle of automated production systems.

AutomationML offers advantages in numerous aspects:
 - **Interoperability**: Different engineering tools from various vendors often use proprietary data formats, making integration difficult. AutomationML aims to standardize data exchange formats to facilitate seamless interoperability between these tools.
 - **Data Consistency**: Ensuring consistent and error-free data across various engineering phases (e.g., design, implementation, operation) is crucial. AutomationML provides a structured way to maintain data consistency throughout the entire system lifecycle.
 - **Complexity Management**: Modern automated systems are highly complex, involving numerous components and subsystems. AutomationML helps manage this complexity by offering a clear and standardized method to represent and interconnect different system elements.
 - **Flexibility and Extensibility**: AutomationML is designed to be flexible and extensible, allowing it to adapt to future requirements and incorporate new technologies and methodologies as they emerge.

![AutomationML Ontology Overview](figures/automationml-overview.svg)

## Ontology Information

- **Namespace**: `https://w3id.org/hsu-aut/AutomationML#`
- **Preferred Prefix**: `aml:`
- **Standard**: IEC 62714

## Usage

### Importing the Ontology

If you want to use this ontology design pattern, the easiest way is to directly import it into your ontology via `owl:imports` statements using the permanent w3id.org URI.

**Import URI**: `https://w3id.org/hsu-aut/AutomationML`

This permanent URI automatically resolves to the latest version of the ontology. The w3id.org service is registered to redirect to the GitHub repository, ensuring long-term availability.

An example of an imports section looks like this:

```xml
<owl:Ontology rdf:about="http://www.hsu-ifa.de/ontologies/capability-model#">
    <owl:versionIRI rdf:resource="http://www.hsu-ifa.de/ontologies/capability-model/1.0.0#"/>
    <owl:imports rdf:resource="https://w3id.org/hsu-aut/AutomationML"/>
</owl:Ontology>
```

If you're having trouble using this URL in a tool like Protégé, try opening your ontology with a text editor and simply inserting your imports manually.

You can also clone or download this repository and import the ontology from a local copy if needed.

### Converting AutomationML Files to OWL

To convert AutomationML files to OWL format based on this ontology, you can use our [aml2owl conversion tool](https://github.com/hsu-aut/aml2owl). This tool enables the automatic transformation of AutomationML/CAEX files into OWL individuals that conform to this ontology, facilitating graph-based queries and validation.

## Citation

The content of this ontology and exemplary use cases are described in the following preprint:

**Westermann, T., Ramonat, M., Hujer, J., Gehlhoff, F., & Fay, A. (2025).** *Automatic Mapping of AutomationML Files to Ontologies for Graph Queries and Validation.* arXiv preprint arXiv:2504.21694. https://arxiv.org/abs/2504.21694

```bibtex
@article{Westermann2025,
  author = {Westermann, Tom and Ramonat, Malte and Hujer, Johannes and
            Gehlhoff, Felix and Fay, Alexander},
  title = {Automatic Mapping of {AutomationML} Files to Ontologies for
           Graph Queries and Validation},
  journal = {arXiv preprint arXiv:2504.21694},
  year = {2025},
  eprint = {2504.21694},
  archivePrefix = {arXiv},
  primaryClass = {cs.AI},
  doi = {10.48550/arXiv.2504.21694}
}
```

## License

This work is distributed under a [Creative Commons Attribution 3.0 License](http://creativecommons.org/licenses/by/3.0/).

## Related Industrial Standard Ontology Design Patterns

This ontology is part of a larger collection of industrial standard-based ontology design patterns developed and maintained by HSU-HH. These ontologies enable semantic integration of heterogeneous engineering data sources:

### Process and Manufacturing Standards
- **[VDI 3682](https://github.com/hsu-aut/IndustrialStandard-ODP-VDI3682)** - Formalized process descriptions
- **[DIN 8580](https://github.com/hsu-aut/IndustrialStandard-ODP-DIN8580)** - Manufacturing processes taxonomy (with English translation)
- **[ISO 22400-2](https://github.com/hsu-aut/IndustrialStandard-ODP-ISO22400-2)** - Key performance indicators for manufacturing operations management
- **[ISA-88.01](https://github.com/hsu-aut/IndustrialStandard-ODP-ISA88.01)** - Batch control standard

### System Architecture and Design
- **[VDI 2206](https://github.com/hsu-aut/IndustrialStandard-ODP-VDI2206)** - Design methodology for mechatronic systems
- **[VDI 2860](https://github.com/hsu-aut/IndustrialStandard-ODP-VDI2860)** - Assembly and handling functions
- **[VDI 5100](https://github.com/hsu-aut/IndustrialStandard-ODP-VDI5100)** - System Architecture for Intralogistics (SAIL)
- **[DIN EN 62264-2](https://github.com/hsu-aut/IndustrialStandard-ODP-DINEN62264-2)** - Enterprise-control system integration (ISA-95)

### Data Exchange and Communication
- **[OPC UA](https://github.com/hsu-aut/IndustrialStandard-ODP-OPC-UA)** - OPC Unified Architecture information model and nodesets
- **[WADL](https://github.com/hsu-aut/IndustrialStandard-ODP-WADL)** - Web Application Description Language

### Data Modeling and Semantics
- **[DIN EN 61360](https://github.com/hsu-aut/IndustrialStandard-ODP-DINEN61360)** - Standard data element types with associated classification scheme
- **[VDI/VDE/NAMUR 2658](https://github.com/hsu-aut/IndustrialStandard-ODP-VDIVDENAMUR2658)** - Automation Engineering information model
- **[UNECE Units of Measure](https://github.com/hsu-aut/IndustrialStandard-ODP-UNECE-UoM)** - UN/ECE Recommendation 20 units of measure

### Machine Behavior and Control
- **[PackML](https://github.com/hsu-aut/IndustrialStandard-ODP-PackML)** - Packaging machinery state machine standard

### Robotics
- **[IEEE 1872-2](https://github.com/hsu-aut/IndustrialStandard-ODP-IEEE1872-2)** - Autonomous robotics ontology
