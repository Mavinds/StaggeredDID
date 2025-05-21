# Staggered adoption matching approach
This code is for reproducing the Staggered Matching Approach proposed in the paper "Causal spillover effects of electric vehicle charging station placement on local businesses: a staggered adoption study" by M. Mavin De Silva, Callie Clark, Nakayama Tadachika, and Takahiro Yabe.

The following Jupyter notebooks are accompanied by Placer.Ai data (TotalPOIs_within400m.csv and CityMatchedPOIsCleanedforDID.csv) to test the methods used in the study.

- C1-staggeredmatching.ipynb: inspects the POI data considering the staggered rollout of EVCS installations and 1) creates a set of candidate control POIs, 2) finds the best match for each treated POI using pre-intervention difference, and 3) prepares a dataframe that contains matched pairs for the Staggered Difference-in-Difference analysis code (Staggered_DID.ipynb). Typically runs within 6 hours on a standard desktop computer.
- C2-staggeredDID.ipynb: runs the algorithm to calculate the average treatment effects of an EVCS and heterogeneous treatment effects using the staggered DID approach proposed in the paper. Typically runs within 5 minutes on a standard desktop computer.

# Software dependencies
- Python 3.12.7
- Numpy version 1.26.4
- Pandas version 2.2.2
- Matplotlib version 3.9.2
- Statsmodels version 0.14.2
- Geopandas version 1.0.1



