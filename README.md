# Soil Knowledge Graph 

Welcome to the Soil Knowledge Graph repository! We are excited to present our work on constructing a comprehensive knowledge graph for soil-related information. Our knowledge graph (https://w3id.org/def/soil) or for graph parsing (https://naeima.github.io/soil/index.ttl) is built with the Forest Observatory Ontology (FOO) (https://w3id.org/def/foo/), which serves as the foundation for organising and representing soil data. We used YARRRML's Matey (https://rml.io/yarrrml/matey/) to construct the Soil Knowledge Graph.

The Soil Knowledge Graph aims to provide a deep understanding of soil by interconnecting various aspects such as soil properties, composition, classification, and ecological relationships. By leveraging the power of the Forest Observatory Ontology, we ensure that complex relationships are captured and different sources of soil data can be integrated seamlessly.

Our primary objective is to enhance data interoperability, foster knowledge sharing, and enable advanced analyses in soil science. The Soil Knowledge Graph is valuable for researchers, practitioners, and stakeholders. It allows them to explore and uncover valuable insights about soil health, ecosystem dynamics, and effective land management practices.

We invite you to dive into our repository, contribute to developing the Soil Knowledge Graph, and use it as a powerful tool to expand our understanding of soils and their crucial role in ecological systems. 

# Soil Sensor Data
The data consist of soil characteristics and nutrients for tropical forests in Sabah, Malaysia, both unlogged and logged. Soil properties (ID, Site, LandUse, PlotName, Subplot, Horizon, pH, TotalC, TotalN, TotalP, inorganicP, C-N, Sand, Silt, Clay) extracted from buried ion exchange membranes and soil nutrients (Identifier, Site, LandUse, PlotName, Subplot, NO3N, NH4N, TotalN, Ca, Mg, K, P, Fe, Mn Cu, Zn, B This data is a contribution from the BALI collaboration, which is financed by the UK’s Natural Environment Research Council (NERC). Modelled datasets in this study can be found at (https://github.com/Naeima/Forest-Observatory-Ontology/releases/tag/Soil-Data-v1.0.0).



# Soil Data RDF Conversion

This repository contains a script for converting CSV data related to soil measurements into an RDF graph using the `rdflib` library in Python. The script leverages an ontology for structuring the data within the RDF format, enabling semantic querying and integration with other datasets.

## Requirements

- Python 3.x
- `rdflib`

Ensure you have Python installed on your system. You can install `rdflib` using pip:

```bash
pip install rdflib

## Usage
 Prepare Your Data and Ontology Files
Ensure you have your CSV data file (SoilNu.csv) and the Turtle file (foo.ttl) containing your ontology in the project's root directory.

## Customize the Script
Please look over the script to make sure the column mappings and the namespace URIs match your CSV structure and ontology.

## Run the Script
Execute the script with Python. It reads the CSV data, converts it into RDF triples based on the mappings and the ontology provided, and saves the output as an RDF XML file (SoilKG.rdf).

python convert_to_rdf.py

Ensure your CSV file matches the structure expected by the script, or adjust the script to fit your CSV format.

## Customizing the Script
The script contains placeholders for namespaces and ontology terms. You should adjust these to fit your ontology:

namespace and namespace1 are placeholders for the ontology namespaces. Replace them with the actual namespaces used in your ontology.
Predicates like namespace, site, namespace, Land_Use, etc., should be replaced with the actual predicates from your ontology that correspond to your data columns.
Output

The script generates an RDF XML file (SoilKG.xml) containing the RDF representation of your CSV data according to the mappings defined in the script and structured by your ontology.



