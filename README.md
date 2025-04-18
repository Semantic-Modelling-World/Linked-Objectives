# Linked Objectives

**Linked Objectives – The transparent, semantic OKR tool**

An open-source OKR tool based on Linked Data and semantic models, enabling data-driven, connected, and transparent goal management.

---

## Key Features

- **Semantic OKRs** – Connect objectives and key results in a structured, meaningful knowledge graph  
- **Data-Centric & Interoperable** – Leverages Linked Data and open standards for seamless integration into existing data landscapes  
- **Full Transparency** – Understand how personal goals contribute to company objectives  
- **Minimalist & Intuitive** – A clean, user-friendly interface makes OKRs accessible, even for beginners

> With Linked Objectives, everyone can see how their goals align with the bigger picture.

---

## Project Vision

- The project is designed as an open and collaborative initiative, allowing future students and contributors to extend its capabilities.
- It aims to make OKRs accessible to beginners while serving as a practical application of Linked Data and Semantic Web principles.
- The tool functions as a "goal navigation system" within organizations, helping teams and individuals understand decision-making processes and how their contributions align with high-level objectives and vision.

---

## Technical Requirements

- **Data Access**: All data is accessed via a SPARQL endpoint, ensuring compatibility with Linked Data principles.
- **Metamodels**: All metamodels are provided as OWL (Web Ontology Language) models.
- **User Authentication**: Users must be able to sign up, log in, and manage their accounts.
- **Test Data**: Both user test data and OKR test data are provided in RDF format.

---

## Visual OKR Editing

The tool includes an interactive diagram editor (e.g., Excalidraw integration) that supports:

- A palette of existing OKRs from the metamodel
- Drag & Drop functionality for intuitive OKR canvas creation
- Custom diagrams referencing existing OKRs
- Automatic rendering of relationships between OKRs
- Adjustable layout and appearance of connections while maintaining logical integrity

---

## Using Triple Stores

Linked Objectives is compatible with free and open-source triple stores such as Ontotext GraphDB, Apache Jena Fuseki, and others. These tools allow you to load, query, and manage the RDF data provided in this project. Follow these steps to get started:

1. **Install a Triple Store**:
   - Download and install a triple store of your choice (e.g., [Ontotext GraphDB](https://www.ontotext.com/products/graphdb/), [Apache Jena Fuseki](https://jena.apache.org/documentation/fuseki2/)).

2. **Load RDF Data**:
   - Import the RDF files from the `data` directory into your triple store.
   - Ensure that the namespaces and prefixes are correctly resolved.

3. **Run SPARQL Queries**:
   - Use the SPARQL endpoint provided by the triple store to query the data.
   - Example query:
     ```sparql
     SELECT ?objective ?keyResult
     WHERE {
       ?objective a <https://data.sick.com/voc/sam/objectives-model/Objective> ;
                  <https://data.sick.com/voc/sam/objectives-model/hasKeyResult> ?keyResult .
     }
     ```

4. **Explore and Extend**:
   - Use the triple store's interface to explore the data and test the provided SHACL shapes for validation.

For more details, refer to the documentation of your chosen triple store.

---

## Maintainers

This project is developed and maintained by **[SICK AG](https://sick.com)**.  
It was initiated by **Burkhard Weber**, Head of Linked Data at SICK AG  
([@weberbuSICKAG](https://github.com/weberbuSICKAG)), and is actively supported by the internal team.

We welcome contributions from students, researchers, and the broader community interested in **Linked Data, OKRs, the Semantic Web**, and **open knowledge systems**.

---

## License

This project is licensed under the MIT License. See [LICENSE](./LICENSE) for details.
