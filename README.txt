Supplementary data and code for "Mutualistic microbes linked with broader niches but reduced diversification"


###############################################################################
####### All R scripts and analyses were conducted using R version 4.4.3 #######
###############################################################################

### Maxent_models.Rmd ### 
Code for generating Niche models for each species using predicts_0.1-19. This is a massive loop and takes several days to complete the models. 
rgbif_3.8.1 and CoordinateCleaner_3.0.1 were used to download and clean occurrence records. Records were further cleaned using known distributions following Plants of the World Online. Niche model output and performance metrics are provided in table S4,

### Hypervolumes.Rmd ###
Code for estimating hypervolumes, using hypervolume_3.1.5
spatial analyses also use enmSdmX_1.2.12, sf_1.0-21, and terra_1.8-60.
Output from this is available in table S4.


### brms_logistic_regression.Rmd ###
Code for the Bayesion phylogenetic logistic regression. ape_5.8-1 was used for the phylogenetic effect and brms_2.22.0 was used.

### INLA_models_priortests_rangesize.Rmd ###
This is the script testing the influence of endophytes on range size. This goes over different phylogenetic priors, meshes, and spatial priors. The exact same models were also run for our other niche breadth variables: range on the primary niche axis and hypervolume. 
These models were also used to test how environmental variables structure endophyte presence - this is the same script (tested the same priors and meshes) but those models use a binomial family. 
Data is available in table S4.
This code uses INLA_24.12.11, ape_5.8-1


### PGLS.Rmd ###
Code for repeating pgls models, using ape_5.8-1 and nlme_3.1-168. Data is available in table S4.


############################################################################
####### All revbayes scripts were run using RevBayes version (1.2.4) #######
############################################################################

### MuSSCRat.Rev ###
This takes a very long time to run, a minimum of 500,000 generations were run to achieve convergence. These models were repeated testing different priors which is made as a note in the script. These scripts are based on the revbayes tutorial available at: https://revbayes.github.io/tutorials/cont_traits/state_dependent_bm.html
The reference for this model is: May M., Moore B.R. 2020 A Bayesian approach for inferring the impact of a discrete character on rates of continuous-character evolution in the presence of background-rate variation. Syst Biol 69, 530-544. (doi:10.1093/sysbio/syz069).


### HiSSE.Rev ###
Code for the hidden state dependent speciation and extinction model. This is executed using revbayes.


