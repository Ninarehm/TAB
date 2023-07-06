# Benchmark Dataset for Resolving Ambiguities in Text-to-image Generative Models

This benchmark dataset covers different types of linguistic as well as fairness ambiguities (in the form of under-specification) to evaluate faithful generation in text-to-image generative models in the existence of prompt ambiguities. This dataset covers 1200 ambiguous prompts and 4690 visual scenes (possible interpretations for existing prompts in this dataset). Our dataset on a high level covers six main types of ambiguities that can be visually traced including: 
1. Syntax Prepositional Phrase (Example: **The girl approaches the shelf with a green plate.** It is possible that 1. the green plate is with the girl or 2. the green plate is on the shelf.)
2. Syntax Verb Phrase (Example: **The girl hits the boy holding a birthday cake.** It is possible that 1. the girl is holding the birthday cake or 2. the boy is holding the birthday cake.)
3. Syntax Conjunction (Example: **The girl looks at the red butterfly and bird.** It is possible that the bird is red or 2. the bird is not red.)
4. Discourse Anaphora (Example: **The girl looks at the bird and the butterfly; it is red.** It is possible that 1. the bird is red or 2. the butterfly is red.)
5. Discourse Ellipsis (Example: **The wolf eats the rabbit. Also the cat.** It is possible that 1. the wolf eats both the rabbit and the cat or 2. the wolf and the cat eat the rabbit.)
6. Fairness (Example: **An image of a doctor.** 1. Is the doctor male? 2. Is the doctor female? 3. What is the racial category of the doctor? 4. What age category?)


Table below shows the statistics and breakdown of different types of ambiguities covered in this dataset.

| Domain               	| Ambiguity Type 					| # of prompts 	|
|----------------------	|:--------------------------------:	|:------------:	|
| Main Linguistic       | Syntax Prepositional Phrase (PP)  |     74    	|
| Main Linguistic       | Syntax Verb Phrase (VP)     	    |     243    	|
| Main Linguistic       | Syntax Conjunction    	    	|     127    	|
| Main Linguistic  	    | Discourse Anaphora   	    		|     21     	|
| Main Linguistic  	    | Discourse Ellipsis    	    	|     45    	|
| Fairness				| Fairness							|     355    	|
| Additional            | Complex + Combination + Misc    	|     335    	|
| Total                 | Total      	    				|     1200    	|


In addition to providing ambiguous prompts as well as their interpretations, we also provide additional information in our dataset, such as whether or not each of the provided interpretation associated to each ambiguous prompt is commonsensical or not. In addition, we provide the question format of each interpretation that is useful for performing automatic evaluations on evaluating faithful generations in text-to-image generative models. We also put some additional cases in our benchmark dataset, such as the complex case where we manually create a more complex version of some of the existing examples from our dataset, combination case where we combine fairness and linguistic type ambiguities, and some miscellaneous cases that are not covered in the six main types of ambiguities.


# Getting Started

Download a copy of the dataset in the benchmark/data folder. Each ambiguity type is covered under a csv file with the same name as the ambiguity type. The total.csv file contains all the ambiguities in one place. Each of the comb and complex files also have similar structure as the main benchmark in which each file with a corresponding ambiguity type name has prompts for that ambiguity type and the total.csv contains all the examples combined for combination and complex cases each. 


# License

![alt text] (https://i.creativecommons.org/l/by-sa/4.0/88x31.png)
The dataset is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License] (http://creativecommons.org/licenses/by-sa/4.0/).


# How to Cite

Coming soon!

# Acknowledgment

We created this benchmark with [LAVA](https://web.mit.edu/lavacorpus/) as reference and modified and extended it. The original LAVA corpus covers 237 ambiguous sentences (prompts) and 498 visual setups (possible interpretations for each ambiguous sentence). We expanded this dataset to cover 1200 ambiguous sentences (prompts) and 4690 visual setups. 
