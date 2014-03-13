# Conjoint Analysis
Considering features / attributes to be considered jointly
"For example, a typical large luxury car provides superior performance, safety, and size, but it also costs more and has low gas mileage. Conjoint analysis is used to study these tradeoffs."
"Conjoint analysis is primarily used to quantify the trade-off structure of preferences for multi-attribute objects."

- Purposes of Conjoint Analysis:
 - It is used to measure the relative importance of features or attributes for individual customers or segments
 - To optimize product design
 - To simulate and assess the impact of changes in own and competitors’ market offerings 
 - To predict choices and market shares 
 - To help perform benefit segmentation 

- Rules for choosing attribute levels
 - independent of each other
 - don't have too many
 - avoid multi-collinearity
- Levels
 - Should be mutually exclusive
 - Should not be vague or ambiguous
 - Do not include too many levels for any one attribute (3-5 per attribute)
 - Balance the levels across attributes

There are several remedies to reduce multi-collinearity between factors: 
 - Create super attributes (combine the correlated attributes into one and create levels with realistic amounts of both attributes) (e.g., instead of HP and mileage, use “PERFORMANCE”) 
 - Prohibited pairs (restrictions in designs): It is complex, creates a poor design and will affect part worth estimates. You still use restrictions but make sure that you take into account the correlation of factors during its interpretation. 
 - You generate another fractional factorial design and assess the acceptability of its profiles/treatments (many profiles are possible). 

*Price and Brand always interact*

Validating the model
- Only run the model with the efficient design dataset. Have a few additional treatment which are used as a hold-out, so that you can validate your model.

Output of Conjoint Analysis
- gives output for every single subject
- you can always look at the within-attribute variation
- output gives you importance by attribute
