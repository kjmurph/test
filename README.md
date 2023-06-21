# Prydz_Bay_mizer

`Adding fishing catch.rmd` is the current markdown to explore IWC catch data and the initial efforts to estimate effort.
There is also a small chunk where krill catch for the Prydz Bay region has been estimated from the hisotrical fishing effort FishMIP output.

`model_setup_v0.Rmd` includes attempts to achieve steady state

`model_setup_v2.Rmd` has a lot of the same setup, but can skip to line 318 where a near-steady state model, that includes salps is loaded.
Then the attempts to upgrade to a therMizer object

For the initial time-averaged steady state model I've been tryign to achieve, there is only catch data for minke whales and baleen whales, as they are the only whaling catch data from the time period that the Ecopath model we're basing this model on
Krill catch in this region from FishMIP hist effort is only available from 1974-1996, nothing beyond 1996 in this region according to the hist effort.

Fishing effort/catch for the fish (i.e., toothfish and other demersal fish have not been included yet)

Note of caution.
Some param files contain 15 functional groups, but I have created a newer version with salps. I used `addSpecies()` to do this and so they are stuck onto the end of the species_params list, not in the max size order
