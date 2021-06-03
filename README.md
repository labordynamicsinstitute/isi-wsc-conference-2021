# Session at ISI WSC 2021: Formal privacy methods in NSO: Challenges and Solutions

## Chair

Dr. Lars Vilhuber (Cornell University)

## Authors

- Dr. Joseph Chien (Australian Bureau of Statistics)
- Prof. Gerome Miklau (Tumult Labs)
- Prof. Jörg Drechsler (Institut für Arbeitsmarkt- und Berufsforschung der Bundesagentur für Arbeit, Germany)
- Dr. Andrew Foote (US Census Bureau)
- Prof. John Abowd (US Census Bureau)

## Brief description

Statistical agencies and tech giants are rapidly adopting formal privacy models, including differential privacy, which make the tradeoff between privacy and data quality precise. These methods have offered the promise of greater ability to release detailed data, while providing better control over the privacy loss associated with any data publication. These methods are novel, and as with any novel technology, implementation can be challenging. NSOs have spent decades refining and applying traditional disclosure limitation methods. The papers in this session report on practical implementations of formal privacy methods, the challenges faced, the advantages and disadvantages assessed.

## Presentation Abstracts

### Speaker: Dr. Joseph Chien (Australian Bureau of Statistics)

pending

### Speaker: Prof. Gerome Miklau (Tumult Labs)

#### Title: Negotiating the privacy-accuracy trade-off in a differentially private release of earnings statistics

#### Abstract

This talk will describe the privacy technologyused to safely report on the earnings distributions of studentsafter graduation. These earnings statistics are publicly released by the U.S. Department of Education in order to increase the transparency and accountabilityof educational programs.  I will describe the differentially private algorithms used to support these ongoing data releases, along with the process of negotiation betweendata curator and end-userusedto arrive at an acceptable balance of privacy risk and fitness-for-use.

### Speaker: Prof. Jörg Drechsler (Institut für Arbeitsmarkt- und Berufsforschung der Bundesagentur für Arbeit, Germany)

pending

### Speaker: Dr. Andrew Foote (US Census Bureau)

#### Title: Differential Privacy in the Post-Secondary Employment Outcomes

#### Abstract 

The US Census Bureau has published earnings and employment outcomes for post-secondary graduates based on matches to earnings records found in the Unemployment Insurance wage records. However, many outside parties have access to a partial match of the population under study, since many states have matched their graduate records to unemployment insurance wage records within the state. This outside data access meant that legacy confidentiality methods would not sufficiently protect the microdata, and had the potential to expose other methods in the process. Formal privacy methods were implemented to release both earnings and employment outcomes, and the method developed to protect the earnings method allows for flexibility in which moments of a distribution an agency can release, as well as straightforward aggregations of categories. I discuss how the formal privacy system was implemented, how to apply it to different settings, and how it performs compared to other candidate protection systems. 


### Speaker: John M. Abowd, Chief Scientist and Associate Director for Research and Methodology, U.S. Census Bureau

#### Title: Differential Privacy and the 2020 Census in the United States

#### Abstract

The talk will focus on the implementation of differential privacy used to protect the data products in the 2020 Census of Population and Housing. I present a high-level overview of the design used for key data products, known as the TopDown Algorithm. I focus on the high-level policy and technical challenges that the U.S. Census Bureau faced during the implementation including the original science embodied in that algorithm, implementation challenges arising from the production constraints, formalizing policies about privacy-loss budgets, communicating the effects of the algorithms on the final data products, and balancing competing data users' interests against the inherent privacy loss associated with detailed data publicati

