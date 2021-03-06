
## GBM Performance

Performance of various open source GBM implementations on the airline dataset (1M and 10M records).

GBM: `100` trees, depth `10`, learning rate `0.1`


On r4.8xlarge (32 cores, 250GB RAM)

Tool     |  Version        | Time[s] 1M  |  Time[s] 10M  |   AUC 1M  |   AUC 10M
---------|-----------------|-------------|---------------|-----------|------------
h2o      |  cran 3.10.4.6  |   25        |    140        |   0.762   |   0.776
xgboost  |  cran 0.6-4     |   20        |    290        |   0.750   |   0.751
lightgbm |  github 97ca38d |    6        |     50        |   0.764   |   0.775


With GPU support on p2.xlarge (Tesla K80, 12GB)

Tool        |  Version               | Time[s] 1M  |  Time[s] 10M  |   AUC 1M  |   AUC 10M
------------|------------------------|-------------|---------------|-----------|------------
h2o xgboost |  deep water 3.11.0.266 |   20        |    180        |   0.715   |   0.708
xgboost     |  github 6776292        |   13        |    crash      |   0.735   |   crash
lightgbm    |  github 1d5867b        |   30        |    120        |   0.771   |   0.789





