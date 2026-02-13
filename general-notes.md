# to-do:
- double check that I merged the plink.GRCh37.map.zip file into one file correctly


# 2/13/26
- look at paper  where they take raw output and try to find the true endpoints
  - they use a genetic map where you map:
    - chromosome "physical position" "centimorgan"
    - in a region of one morgan is a region in which on average, a person transmits one crossover
    - poisson model -- what's the probability that at least one thing happens in a given interval
    - poisson probabilty that you get an odd number of crossovers in a given region  
  - take the true breakpoints. mine the ibd data and cacluate the deltas (differences from the true breakpoint) and find out how far are the breakpoints. calculate the mean distance from the tru breakpoints off all 4 variances.
    - write code for it
  - 
