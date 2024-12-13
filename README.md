Here is the English translation of the documentation:

Data Processing and Analysis Components
DataAccess: Performs dataset preprocessing, including time series interpolation for oil and gold futures, and generates dataset visualizations.

Find Epochs Line: Conducts continuous training and testing across epochs to collect average returns.

Correlation Analysis:
- Pearson: Calculates Pearson correlation coefficients between oil futures, gold futures, and S&P500
- Spearmanr: Computes Spearman rank correlation coefficients between oil futures, gold futures, and S&P500
- Kendalltau: Determines Kendall rank correlation coefficients between oil futures, gold futures, and S&P500

Optimization and Testing:
Bayesian: Performs Bayesian optimization for buy/sell hyperparameters and epochs number optimization.
TEST_Origin_DQN: Tests original DQN ROI for 2019 using S&P500, oil futures, and gold futures dataset.
TEST_Softmax_DQN: Tests Softmax DQN ROI for 2019 using S&P500, oil futures, and gold futures dataset.

Training and Testing Files
The repository contains 16 training and testing files, divided between 200 and 50 epochs, covering periods 2019 and 2010-2019.

File Naming Convention:
- Both: Dataset includes S&P500 + oil futures + gold futures
- Gold: Dataset includes S&P500 + gold futures
- WTI: Dataset includes S&P500 + oil futures
- SPY: Dataset includes only S&P500

Training Period 2010-2018, Testing Period 2019:
Files follow the naming pattern DL_SP500_SPY_10K-ActCount-2019-softmax2-[dataset]-[epochs], where [dataset] indicates the combination of assets used and [epochs] specifies either 200 or 50 epochs.

Training Period 2001-2010, Testing Period 2010-2019:
Files follow the naming pattern DL_SP500_SPY_10K-ActCount-2010-2019-softmax2-[dataset]-[epochs].

Q-Network NPZ Files
These files contain trained Q-Network parameters:
- Q_network_epoch_29-299.npz: Stored results from Find Epochs Line for Bayesian optimization
- Softmax_DQN.npz: Completed TEST_Softmax_DQN training file
- Origin_DQN.npz: Completed TEST_Origin_DQN training file

Additional NPZ files follow the naming convention:
[year]_[dataset]_[network type]_[model type].npz
Example:
- 2001_Both_ddqn_behavior_model.npz: Behavior Q-network for 2001-2010 training period using full dataset
- 2001_Both_ddqn_target_model.npz: Target Q-network for corresponding period and dataset
- 2019_Both_dqn_model: DQN network for 2010-2018 training period using full dataset 
