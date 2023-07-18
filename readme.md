# Disease Symptoms and Patient Profile for FCA processing  

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Hyrlos/Disease-Symptoms-and-Patient-Profile-Processing/HEAD?labpath=FCA%20for%20disease.ipynb)

# Readme
- **Goal**: Leverage the Formal Concept Analysis to explore diseases symptoms.  
The data came from a kaggle dataset: https://www.kaggle.com/datasets/uom190346a/disease-symptoms-and-patient-profile-dataset  
- [**Outputs**](https://github.com/Hyrlos/Disease-Symptoms-and-Patient-Profile-Processing/edit/master/readme.md#output)

## Dependancy
- Python/notebook
- Pandas
- graphviz

## Repository  
- [FCA for disease.ipynb](https://github.com/Hyrlos/Disease-Symptoms-and-Patient-Profile-Processing/blob/master/FCA%20for%20disease.ipynb): a notebook used to clean the dataset et run FCA  
   - Age threshold  
   - Blood Pressure  
   - Cholesterol Level  
   - remove Negative Outcome Variable  
   - Remove no homogeneous disease  
- [Dataset/disease-symptoms-and-patient-profile-dataset](https://github.com/Hyrlos/Disease-Symptoms-and-Patient-Profile-Processing/blob/master/dataset/Disease_symptom_and_patient_profile_dataset.csv): [the dataset from kaggle](https://www.kaggle.com/datasets/uom190346a/disease-symptoms-and-patient-profile-dataset) 
- [aocDiseaseFULL.jpg](https://github.com/Hyrlos/Disease-Symptoms-and-Patient-Profile-Processing/blob/master/output/aocDiseaseFULL.dot.jpg): an AOC-Poset with all the intents and extends  
- [aocDisease.jpg](https://github.com/Hyrlos/Disease-Symptoms-and-Patient-Profile-Processing/blob/master/output/aocDisease.dot.jpg): a reduced AOC-Poset  
  
## Formal Concept Analysis 

The Formal Concept Analysis (FCA) is a mathematical framework used for analyzing and organizing data based on the concept of formal concepts. It provides a way to discover relationships between objects and attributes within a given dataset.   
  
At the core of FCA is the concept of a formal context. A formal context consists of a set of objects, a set of attributes, and a binary relation between the objects and attributes. The binary relation indicates whether an object possesses a certain attribute or not. It establishes a connection between objects and attributes based on their presence or absence.  
  
A formal context can be represented as a two-dimensional table, known as a formal context matrix. The rows of the matrix represent the objects, the columns represent the attributes, and the entries indicate the presence (1) or absence (0) of attributes for each object. This matrix serves as the basis for further analysis in FCA.  
  
Using the formal context, FCA aims to identify formal concepts. A formal concept is a pair consisting of a set of objects and a set of attributes. It represents a subset of objects that share a common set of attributes and vice versa. Formally, a formal concept (A, B) is defined as follows  
  
- A subset of objects: A ⊆ O, where O is the set of all objects.  
- A subset of attributes: B ⊆ A, where A is the set of all attributes.  
  
A formal concept can be understood as a generalization or abstraction that captures the common characteristics shared by a group of objects. It provides a way to organize and classify data based on these shared properties.  
  
The set of all formal concepts within a given formal context can be structured into a partially ordered set, known as the concept lattice or the AOC (Attribute-Object-Concept) Poset. The AOC Poset represents the hierarchy of formal concepts based on the inclusion relationship between them. In other words, it captures the subset relationships between formal concepts, where one concept is more general (higher) than another if it includes a larger set of objects and attributes.  
  
The AOC Poset is often visualized as a lattice diagram, with each node representing a formal concept and the edges representing the inclusion relationship between concepts. This lattice structure provides a systematic way to explore the relationships and dependencies among concepts within a formal context.  
  
In summary, Formal Concept Analysis (FCA) is a mathematical framework that uses formal contexts to analyze and organize data. Formal contexts consist of objects, attributes, and a binary relation between them. FCA aims to identify formal concepts, which are pairs of sets representing subsets of objects and attributes that share common properties. The set of all formal concepts can be organized into a partially ordered set called the AOC Poset or concept lattice, which represents the hierarchy of concepts based on their inclusion relationships.  
  
## How to read the AOC-Poset 

- The top node of the AOC Poset represents the most general concept. It encompasses all diseases and symptoms in the formal context.  
- Each lower node represents a more specialized concept that captures a subset of diseases and symptoms  
- These symptoms are common to the diseases within that concept  
- If concept A is higher in the hierarchy than concept B, it means that concept A includes a broader range of diseases and symptoms than concept B.   
- The edges in the lattice represent this hierarchical relationship.  

## Credits

Wrote by [Thomas GEORGES](https://hyrlos.github.io/)  



## OUTPUT  

![output](https://github.com/Hyrlos/Disease-Symptoms-and-Patient-Profile-Processing/blob/master/output/aocDiseaseFULL.dot.jpg)  
![output](https://github.com/Hyrlos/Disease-Symptoms-and-Patient-Profile-Processing/blob/master/output/aocDisease.dot.jpg)  

