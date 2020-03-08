# SEIR_COV19
SEIR implementation of forecast epidemics

The SEIR models an infection on people between four states: susceptible (S), exposed (E), infected (I), and resistant (R). Each of those variables represents the number of people in those groups.  The parameters alpha and beta partially control how fast people move from being susceptible to exposed (alpha), from exposed to infected (beta), and from infected to quarantine (mu1) and hopefully recovered or again susceptible. This model has two additional parameters; one is the background mortality (mu2) which is unaffected by disease-state, while the other is vaccination which is not included at the moment.  
The SEIR differs from the SIR model in the addition of a latency period. Individuals who are exposed (E) have had contact with an infected person, but are not themselves infectious (the virus is more transmissible when people have symptoms).
 
<p align="center">
<img  align="center" src="https://github.com/alecrimi/SEIR_COV19/blob/master/information.png" height="250">
</p>
For more info on the theory: <a href="http://indico.ictp.it/event/7960/session/3/contribution/19/material/slides/0.pdf" target="_blank">SwissTPH material</a>,   the  <a href="https://ethz.ch/content/dam/ethz/special-interest/usys/ibz/theoreticalbiology/education/learningmaterials/701-1424-00L/sir.pdf" target="_blank">  ETH-tutorial on R </a>, or read O. Diekmann, H. Heesterbeek, and T. Britton, <a href="https://www.jstor.org/stable/j.cttq9530" target="_blank"> Mathematical Tools for Understanding Infectious Disease Dynamics. Princeton Series in Theoretical and Computational Biology </a>
 
Here is the effect of the lockdown in terms of recovery of the epidemic, I am using the SIR/SIER implementation of **Matt Ravenhall** & **Yran Jing**. You will need **Python3**, Pandas, Scipy, and Numpy (SIR/SIER of Yran Jing included). 

Before <a href="https://en.wikipedia.org/wiki/2020_Hubei_lockdowns"> curfew policy implementations </a>, and after. There is a t least a difference of 100 days more of epidemics regardless of the r0. 
Future works, cost effetive analysis on the curfew (opportunity cost and productivity loss) VS no-curfew (productivity loss due to illness and financial healthcare burden). The model does not take into account the weakening of the virus with the coming Spring/Summer.

![alt text](https://github.com/alecrimi/SEIR_COV19/blob/master/before.png) 
![alt text](https://github.com/alecrimi/SEIR_COV19/blob/master/after.png) 
 
The code also estimate R0. For Wuhan seems R0=2.9 for Italy R0=2.1 at the moment I writing this file. 

Change those variables to personalize

t = np.asarray([0, 42, 43, 44, 45, 46])  # time

I = np.asarray([1,198,218,320,478,639]) # number of official confirmed cases

To account for seasonal factor (as it has been hypothetized that the virus dies at 26-28 degree Celsius), the *beta* parameter show attenuated as in the equation 2 of <a href="https://www.hindawi.com/journals/complexity/2018/7191487/" target="_blank"> Rashidinia et al. 2018 </a>. To estimate this parameter you take inspiration by 
<a href="https://www.medrxiv.org/content/10.1101/2020.02.13.20022806v2" target="_blank"> Neher et al. 2020 </a>. 
