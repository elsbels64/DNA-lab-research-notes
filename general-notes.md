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

# 2/20/26
- make sure we're documenting stuff. it doesn't need to be crazy.
- the centimorgan positions in pedsim are different than hapibd because pedsim uses a sex-specific map. the physical position is the same though.
- tbpwt - called "phased ibd" at 23 and me. compare to hapibd.
  - read ped-sim seg file
  - read [ibd caller] sets
  - for all ped-sim segs longer than (5 centimorgans(make this a parameter)?) find overlapping inferred segments and
    - calculate number of segments
    - distance from start and end

-  later on we can try an ibd caller that analyzes unphased data
