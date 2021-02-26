# SonicAI

This was made with GymRetro and NEAT python. 

Few things to keep in mind when using this repo

# For the Multiprocessing training model

pe = neat.ParallelEvaluator(1, eval_genomes)
Make sure that number is not too high since NEAT python does not utilize your GPU. Having the number too high (allocating CPU cores) will slow down your PC significantly 

I was not able to get the pickling to work for this so contact me on discord Bromine#8183 if you got it to work

There was also an odd issue where you you had to use a numpy version 1.19.3 or lower 
