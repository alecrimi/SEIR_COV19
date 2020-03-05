# SEIR_COV19
SEIR implementation of forecast epidemics

The SEIR models an infection on people between four states: susceptible (S), exposed (E), infected (I), and resistant (R). Each of those variables represents the number of people in those groups. The parameters alpha and beta partially control how fast people move from being susceptible to exposed (beta), from exposed to infected (sigma), and from infected to resistant (gamma). This model has two additional parameters; one is the background mortality (mu) which is unaffected by disease-state, while the other is vaccination (nu). The vaccination moves people from the susceptible to resistant directly, without becoming exposed or infected. 
The SEIR differs from the SIR model in the addition of a latency period. Individuals who are exposed (E) have had contact with an infected person, but are not themselves infectious.

![alt text](https://github.com/alecrimi/SEIR_COV19/blob/master/CompartmentalModel.jpg) 
For more info on the theory: <a href="http://indico.ictp.it/event/7960/session/3/contribution/19/material/slides/0.pdf" target="_blank">SwissTPH material</a>, or the  <a href=" https://ethz.ch/content/dam/ethz/special-interest/usys/ibz/theoreticalbiology/education/learningmaterials/701-1424-00L/sir.pdf" target="_blank">  ETH-tutorial on R  
 https://ethz.ch/content/dam/ethz/special-interest/usys/ibz/theoreticalbiology/education/learningmaterials/701-1424-00L/sir.pdf" </a>
 
Here is the effect of the lockdown in terms of recovery of the epidemic, I am using the SIR/SIER implementation of Matt Ravenhall & Yran Jing.
Before <a href="https://en.wikipedia.org/wiki/2020_Hubei_lockdowns"> curfew policy implementations </a>, and after. There is a t least a difference of 100 days more of epidemics regardless of the r0. 
 
