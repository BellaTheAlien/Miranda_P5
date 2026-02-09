### Neila Miranda Wrtie UP

In this file will hold my notes and explanation of my changes in the project

# generate_successors
In making the generate successeors function I choose have a elistism and tournament selection. Starting with the elistism selction, I get the best "genes" from the data for the next generation. Then in the tourmament selection, picking two random parents and getting the better one; then gettting a partner to crossover. this loops till for each child for the generation

# generate_children
In the generate children the crossover I choose to implement is a single point crossover. To get the the data to switch between the parents. Getting each the genration to switch from the parents data, so each level genration flips from thier parent data 

# mutate
For the mutate function I choose to have a "changed" in the generation in a rate of 0.02 or 2% for each tile. Meaning that each tile has a 2% changce of being mutated. In my first addtion of the code I tryied a 5% rate mutation.

For my added constraints I first added a limater for pipes generating in the air, checking if there is a pipe or top of a pipe adove an empty space; if there is we change the pipe to an empty space

Then theres a constraint on enemy genration, so that they stay near the ground. They are limited to the floor on y axies

Next theres a constraint on the many blocks, where they are limited to keep a jumpable hieight, where I set a jumaple setting of 2 - 6 blocks/tiles so that mario can jump them.