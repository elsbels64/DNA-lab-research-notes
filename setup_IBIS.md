What if we also run the above analysis on IBIS segments? ibis is in the group bin directory. You would need to convert the VCF to plink .bed,.bim,.fam format. You can do that like this (plink 1.9 is also in the lab bin):
plink1.9 --vcf [input.vcf] -out [filename_prefix] --make-bed
Another thing that would be nice to do is:
Get a list of SAMAFS individuals that are unrelated. You can use PRIMUS for this -- specifically the IMUS piece. It may not be in the right file format and it doesn't list all pairs (we can create a file that does if needed) but /grphome/grp_hapidna/data/samafs/ibis/safs_filter2_geno0.02_mind0.1-ibis-1.20.6.coef contains the relatives in the SAMAFS data and their coefficient of relatedness.
Simulate again but use the SAMAFS data as input to Ped-sim instead of HapMap.
 for step 2, we'd subset the SAMAFS to the unrelated individuals

Hmm... it looks like downloading PRIMUS isn't working. We'll find another way.
Plink has a --rel-cutoff option that should work, but we should read here.
.... and PRIMUS is now available on the cluster in the lab bin as run_PRIMUS.pl. The documentation is here. I believe we want to run it with --no_PR (so only IMUS runs).
