# vep_compare


This repository contains some tests that were run to compare visco-elastic-plastic rheololgy implementations in the Underworld2 and ASPECT codes.

In particular, I suspected there were mistakes in the original APSECT (circa mid 2019) visco_elastic_plastic material model. This mainlty relasted to the ordering to the implementation that goes back to Moresi et al., 2003, J. Comp. Phys.

The different orderings are implemented in Underworld2 (which allows very versatile assembly of different rheological models) in the directory `uw_order_compare`

In the root level of this directory are two models which are set up to compatre a VEP bending beam in ASPECT and Underworld2 respectively. I have tried to ensure that these models have similar setups, but have not quantitatively compared the output.

NOTE that as of November 2019, the necessary changes in the ASPECT visco_elastic_plastic material model are not yet merged with the mainline. See John Naliboff's branch called `vep_reorder`. John has also integrated teh elasticity into the existing visco_plastic material model, currently residing in a branch called `vp_elasticity`.
