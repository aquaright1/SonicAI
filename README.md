# SonicAI

This was made with GymRetro and NEAT python. 

Few things to keep in mind when using this repo

There was also an odd issue where you you had to use a numpy version 1.19.3 or lower 

# For the Multiprocessing training model

pe = neat.ParallelEvaluator(1, eval_genomes)
Make sure that number is not too high since NEAT python does not utilize your GPU. Having the number too high (allocating CPU cores) will slow down your PC significantly 

I was not able to get the pickling to work for this so contact me on discord Bromine#8183 if you got it to work

# To run a previous checkpoint of Sonic
There should be a line like this near the bottom

p = neat.Checkpointer.restore_checkpoint('neat-checkpoint-215')
Change the number to whatever checkpoint you would like to restore 

p.add_reporter(neat.Checkpointer(10))
This changes how often it saves ex.this saves every 10 generations
