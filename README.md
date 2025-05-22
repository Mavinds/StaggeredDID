# Staggered adoption matching approach
This code is for reproducing the Staggered Matching Approach proposed in the paper "Causal spillover effects of electric vehicle charging station placement on local businesses: a staggered adoption study" by M. Mavin De Silva, Callie Clark, Nakayama Tadachika, and Takahiro Yabe.

The following Jupyter notebooks are accompanied by synthetic datasets (Sample_TotalPOIsData_within400m.csv, DailyvisitsbyPOI.csv and Syntheticmatchedpairswithdistancebins.csv) to test the methods used in the study.

1. "Sample_TotalPOIsData_within400m.csv" contains synthetic data on POIs that are located within a 400-meter radius of an EVCS.    
2. "DailyvisitsbyPOI.csv" includes synthetic data on daily visits to POIs for the considered time period.    
3. "Syntheticmatchedpairswithdistancebins.csv" contains the output from the (C1-staggeredmatching.ipynb) notebook. This dataset includes matched pairs generated using the proposed staggered matching approach, with each pair annotated by distance bins. It is intended for use in the code DID analysis (C2-staggeredDID.ipynb) requiring matched samples and distance-based grouping. 

- C1-staggeredmatching.ipynb: inspects the POI data considering the staggered rollout of EVCS installations and 1) creates a set of candidate control POIs, 2) finds the best match for each treated POI using pre-intervention difference, and 3) prepares a dataframe that contains matched pairs for the Staggered Difference-in-Difference analysis code (Staggered_DID.ipynb). Typically runs within 5 minutes on a standard desktop computer.
- C2-staggeredDID.ipynb: runs the algorithm to calculate the average treatment effects of an EVCS and heterogeneous treatment effects using the staggered DID approach proposed in the paper. Typically runs within 3 minutes on a standard desktop computer.

# Software dependencies
- Python 3.12.7
- Numpy version 1.26.4
- Pandas version 2.2.2
- Matplotlib version 3.9.2
- Statsmodels version 0.14.2
- Geopandas version 1.0.1



