# Session at ISI WSC 2021: Formal privacy methods in NSO: Challenges and Solutions

![ISI 2021 logo](isi2021.png)

## Time and Location

Fri July 16, 2021, 14:00-15:30 (BST, UTC+1)

Virtual. Link to recording coming.

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

## Presentation Abstracts and Slides

### Speaker: Dr. Joseph Chien (Australian Bureau of Statistics)

#### Title: Pufferfish differential privacy in agriculatural statistics

#### Abstract

The ABS is conducting research to maximise data utility while providing privacy protection to data providers. Under the Census and Statistics (Information Release and Access) Determination 2018, the ABS provides passive confidentiality which protects data providers who can demonstrate that the release of an ABS statistical output would be likely to allow their identification. These data providers are called passive claimants. 

The current confidentiality method for protecting passive claimants is suppression; an aggregate statistic (e.g. a total) is not published if a passive claimant’s value that contributes to the statistic is sensitive. One suppression leads to more suppressions to prevent the calculation of the original suppressed value based on related statistics and this becomes very time intensive to resolve. This limits the ABS’s ability to provide timely data and meet an increasing user demand for more granular business statistics including greater regional data. In addition,the ABS is moving towards the use of alternative data sources to reduce respondent burden and improve the timeliness and granularity of statistics. This means that much more statistical outputs will need be protected to varying degrees. 

A privacy method that the ABS is currently investigating is log-Laplace multiplicative perturbation that fits within a form of Pufferfish differential privacy (DP framework. This technique would allow more detailed statistics to be safely published compared to suppression, as it perturbs the passive claimant’s value before it is used to produce aggregate statistics. Our form of Pufferfish DP offers a privacy protection guarantee by connecting the p% rule with the Pufferfish DP framework. The p% rule is widely used at the ABS and other national statistical offices to determine if a passive claimant’s value requires privacy protection. The p% rule is defined as follows; if a passive claimant’s value can be estimated to within p% of its reported value, then it requires protection. In our form of Pufferfish DP, “secrets” are statements that take a form of “passive claimant A’s reported value is within p% of the value x”. Log-Laplace multiplicative perturbation protects these “secrets” by ensuring users of our statistical outputs cannot confidently estimate a passive claimant’s sensitive value to within p% of its reported value. 

We use Agriculture Statistics as a test case because of the need to protect the privacy of specific data providers but also because the agriculture program is moving to use alternative data sources that will demand a different approach to data privacy. Preliminary results showed that log-Laplace multiplicative perturbation provides more data utility than suppression. Research is underway to explore how the approach can be used in the Agriculture Statisticsproduction process.

- [Slides](ABS_Pufferfish.pdf)

### Speaker: Prof. Gerome Miklau (Tumult Labs)

#### Title: Negotiating the privacy-accuracy trade-off in a differentially private release of earnings statistics

#### Abstract

This talk will describe the privacy technologyused to safely report on the earnings distributions of studentsafter graduation. These earnings statistics are publicly released by the U.S. Department of Education in order to increase the transparency and accountabilityof educational programs.  I will describe the differentially private algorithms used to support these ongoing data releases, along with the process of negotiation betweendata curator and end-userusedto arrive at an acceptable balance of privacy risk and fitness-for-use.

- [Slides](ISI-workshop-MIKLAU.pdf)

### Speaker: Prof. Jörg Drechsler (Institut für Arbeitsmarkt- und Berufsforschung der Bundesagentur für Arbeit, Germany)

#### Title: Differential Privacy for Geocoded Data

#### Abstract

In this talk we evaluate if the concept of differential privacy can be used to disseminate detailed geocoding information without compromising the confidentiality of the individuals included in the database. To enable the release of detailed geographical information we propose a differentially private procedure based on a micro-aggregation algorithm with a fixed minimal cluster size.We evaluate whether meaningful results can be obtained with this approach using administrative data gathered by the German Federal Employment Agency.  Detailed geocoding information has been added to this database recently and plans call for making this valuable source of information available to the scientific community. We generate differentially private microdata using different levels of geographical detail to identify the most detailed level that still provides acceptable analytical validity while offering strong differential privacy guarantees.

- [Slides](ISI_2021_Drechsler.pdf)

### Speaker: Dr. Andrew Foote (US Census Bureau)

#### Title: Differential Privacy in the Post-Secondary Employment Outcomes

#### Abstract 

The US Census Bureau has published earnings and employment outcomes for post-secondary graduates based on matches to earnings records found in the Unemployment Insurance wage records. However, many outside parties have access to a partial match of the population under study, since many states have matched their graduate records to unemployment insurance wage records within the state. This outside data access meant that legacy confidentiality methods would not sufficiently protect the microdata, and had the potential to expose other methods in the process. Formal privacy methods were implemented to release both earnings and employment outcomes, and the method developed to protect the earnings method allows for flexibility in which moments of a distribution an agency can release, as well as straightforward aggregations of categories. I discuss how the formal privacy system was implemented, how to apply it to different settings, and how it performs compared to other candidate protection systems. 


### Speaker: John M. Abowd, Chief Scientist and Associate Director for Research and Methodology, U.S. Census Bureau

#### Title: Differential Privacy and the 2020 Census in the United States

#### Abstract

The talk will focus on the implementation of differential privacy used to protect the data products in the 2020 Census of Population and Housing. I present a high-level overview of the design used for key data products, known as the TopDown Algorithm. I focus on the high-level policy and technical challenges that the U.S. Census Bureau faced during the implementation including the original science embodied in that algorithm, implementation challenges arising from the production constraints, formalizing policies about privacy-loss budgets, communicating the effects of the algorithms on the final data products, and balancing competing data users' interests against the inherent privacy loss associated with detailed data publicati

- [Slides](2021-0716-Abowd-IPS-161-WSC.pptx)
