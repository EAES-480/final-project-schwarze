Analyzing Relationships between Microbial Communities in the Serengeti and the Environment
================
by AnaBelle Schwarze

## Introduction

The data used in this project comes from a study done in Serengeti National Park in Tanzania. This experiment involved the observation of bacterial and archaeal communities in the soil after the removal of mammalian herbivores for 13 years. Shifts in the community structure were measured using 31 amplicon sequence variants (ASVs), in which their abundance was correlated to soil texture, several minerals, rainfall, pH, and soil organic matter (SOM). Overall, there are 11 variables in the data set and 50 sets of observations. 

My work on this project was to evaluate which environmental conditions shaped the microbial communities in this experiment the most, and at which level of taxonomy this was the most observable. The research questions I strived to answer when analyzing the data are as follows:

- How do microbial communities in the Serengeti react to the environment?

- Which conditions appear to affect them the most?

- Is there a difference between individual phyla or kingdoms?

## Methodology

In order to properly analyze the data, I had to create a new variable that differentiated between the bacteria and archaea kingdoms, titled `kingdom`, as well as a variable that separated the individual phyla. This is because the original dataset held the microbial taxonomic classifications within a single string. After processing the data this way, I calculated the mean correlations for each environmental variable, including soil texture (sand, silt, clay), mineral nutrients (phosphorus, calcium, iron, nitrogen), rainfall, soil organic matter (SOM), and pH. This was sent through a pivot longer to be run through ANOVA tests and used to create visualizations.

I ran several ANOVA tests on the data to determine which variables had the strongest correlation to the microbes and which level of taxonomy exhibited the most variation. The first ANOVA evaluated whether microbial kingdom influenced correlations with environmental variables. Results showed a highly significant kingdom effect (F = 32.78, p < 0.001), indicating that archaea and bacteria respond differently to environmental conditions, aligning with preconceived differentiation of organisms at a kingdom level. The second ANOVA tested for phylum-level differences and also found significant variation among phyla (F = 4.74, p < 0.001). However, the effect size was smaller than the kingdom-level effect. To determine which environmental variables were most influential, separate ANOVA tests were conducted for each environmental factor. 

Several visualization techniques were explored to examine relationships between microbial groups and environmental variables. Initial plots included broad phylum-level comparisons across all variables, but these were refined to focus only on statistically significant environmental drivers. Final visualizations highlighted correlations between microbial phyla and the strongest environmental variables while distinguishing between bacteria and archaea using separate color schemes. 

## Results 

From running the ANOVA tests, it was determined the strongest and most statistically significant drivers were phosphorus (P), calcium (Ca), clay, iron (Fe), sand, and silt. Rainfall showed a weaker but still slightly significant effect. Soil organic matter (SOM), pH, and nitrogen (N) were not statistically significant predictors of microbial variation in this dataset and were therefore not used in further exploration of the data. The findings from the initial two ANOVA tests suggest that upper-level taxonomic identity explains a large proportion of microbial-environment relationships, while finer-scale ecological specialization occurs within kingdoms at the phylum level. 

Using the information derived from the statistical analysis, I created a final, polished bar chart that plotted each phyla’s relationship to the most correlated environmental variables. This visualization demonstrated that bacteria and archaea respond differently to environmental conditions with archaea being the most influenced across the board.

## Conclusion

Overall, this project and its analysis demonstrates that microbial communities exhibit strong taxonomic differences in their responses to environmental gradients, especially amongst the kingdom-level, suggesting these differences are a main driver of diversity within microbial communities in the Serengeti. Additionally, it suggests that soil type and mineral nutrients are also dominant ecological drivers within this dataset. These results contribute to a broader understanding of how microbial ecology is structured by environmental heterogeneity and emphasize the importance of considering both taxonomic identity and soil properties when evaluating microbial-environment relationships.

## Presentation

Our presentation can be found [here](presentation/presentation.html).

## Data

Stevens, Bo; Sonderegger, Derek; Johnson, Nancy (2020). Microbial community structure across grazing treatments and environmental gradients in the Serengeti [Dataset]. Dryad. https://doi.org/10.5061/dryad.hhmgqnkf6

## References

Stevens, Bo; Sonderegger, Derek; Johnson, Nancy (2020). Microbial community structure across grazing treatments and environmental gradients in the Serengeti [Dataset]. Dryad. https://doi.org/10.5061/dryad.hhmgqnkf6
