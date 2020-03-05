# SEIR_COV19
SEIR implementation of forecast epidemics

The SEIR models the flows of people between four states: susceptible (S), exposed (E), infected (I), and resistant (R). Each of those variables represents the number of people in those groups. The parameters alpha and beta partially control how fast people move from being susceptible to exposed (beta), from exposed to infected (sigma), and from infected to resistant (gamma). This model has two additional parameters; one is the background mortality (mu) which is unaffected by disease-state, while the other is vaccination (nu). The vaccination moves people from the susceptible to resistant directly, without becoming exposed or infected.

The SEIR differs from the SIR model in the addition of a latency period. Individuals who are exposed (E) have had contact with an infected person, but are not themselves infectious.
