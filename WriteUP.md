### Neila Miranda Write UP


In this file will hold my notes and explanation of my changes in the project


# generate_successors
In making the generate successors function I choose to have an elitism and tournament selection. Starting with the elitism selection, I get the best "genes" from the data for the next generation. Then in the tournament selection, picking two random parents and getting the better one; then getting a partner to crossover. this loops till for each child for the generation


After changing the "Individual = Individual_Grid" to equal "Individual_DE" the program crashed; after asking in office hours I found out that there are times where a parent of the generation could have been empty in a run so I had to add a check for empty parents in this function; if there was one thats empty the loop is exited as to not make generations from empty parents


# generate_children
In the generated children the crossover I choose to implement is a single point crossover. To get the data to switch between the parents. Getting each the generation to switch from the parents data, so each level generation flips from their parent data


# mutate
For the mutate function I choose to have a "change" in the generation at a rate of 0.02 or 2% for each tile. Meaning that each tile has a 2% chance of being mutated. In my first edition of the code I tried a 5% rate mutation.


For my added constraints I first added a limiter for pipes generating in the air, checking if there is a pipe or top of a pipe above an empty space; if there is we change the pipe to an empty space


Then there's a constraint on enemy generation, so that they stay near the ground. They are limited to the floor on y axis


Next there's a constraint on the many blocks, where they are limited to keep a jumpable height, where I set a jumaple setting of 2 - 6 blocks/tiles so that mario can jump them.


# Individual_DE
Looking into this class from what I understand the mutation I see that it's given a mutation rate of 10% then a random element is picked to be the mutation for each element. As the rest of the function goes into each element/block to be mutated. Rather than going by a grid mutation the element of the level is changed based on the element, so the loop goes through all the coin blocks to be mutated then goes to the next block.


Then in the generate_children function it starts by getting two parents at random with different design elements then it creates two splits of the parents gens to create each child; so making ga is made from a start of parent A then B, then gb is made first from parent B then A with a different split of the gen. Finally the two children are also called into the mutation function as "self" so that there is more of a difference of themselves then just being a parent copy.