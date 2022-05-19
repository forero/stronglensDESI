0. Start by doing visual inspection of the kind of systems that we are looking for.
   a. Looking at DESI data corresponding to SILO objects https://arxiv.org/abs/2007.09006
   b. Observed targets that have been classified as potential strong lenses in DESI 
       https://data.desi.lbl.gov/desi/users/kpotter/stronglens/everest_pix_99/

1. Grab the already trained convolutional neural netork
https://github.com/DESI-UR/stronglens/
/global/project/projectdirs/desi/science/gqp/stronglens

2. Feed DESI data to the network to get the probability of a being a strong lens.

3. For targets with a high probability (most are false positives), use their TARGETID and RA,Dec coordinates 
   to grab the target's information (from tractor) within a given search radius, specially their target type.

4. See whether we can actually use that target information to further discard candidates and increase purity.

5. Retrain the network on Fuji.

6. Rerun on all the data from Daily.
   
