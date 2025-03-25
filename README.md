# SPOOF-DETECTION

A Proximal Policy Optimization (PPO) approach for detecting spoofing in algorithmic trading, with a focus on the LUNA flash crash of May 2022.

## Overview

TradeSentry implements a deep reinforcement learning model to identify market manipulation through spoofing tactics. The system analyzes Level 3 Limit Order Book (LOB) data to recognize patterns where traders place and rapidly cancel large orders to create artificial price movements.

## Technical Approach

The system consists of several key components:

1. **Data Preprocessing**: Handles Level 3 LOB data, extracting temporal patterns and order attributes. Implements robust error handling for real-world financial data.

2. **Feature Engineering**: Creates specialized features for spoofing detection:
   - Rolling statistics for price and size movements
   - Order flow imbalance metrics
   - Cancellation ratios
   - Time-sensitive features targeting spoofing behavior

3. **Market Simulation Environment**: Simulates trading conditions with:
   - Dynamic spoofing threshold adjustment
   - Realistic reward mechanisms
   - State representation capturing temporal patterns

4. **PPO Policy Network**: Implements a neural network architecture that:
   - Processes time-series market data
   - Outputs spoofing/non-spoofing classifications
   - Adapts to changing market conditions

5. **Training & Evaluation**: Includes mechanisms for:
   - Efficient experience collection
   - Robust advantage estimation
   - Protection against training instabilities

## Key Features

- **Adaptive Thresholds**: Dynamically adjusts spoofing detection thresholds based on recent anomaly scores
- **Crash Hour Analysis**: Special emphasis on peak volatility periods during flash crashes
- **Customized Reward Structure**: Addresses class imbalance in spoofing detection
- **Resilient Processing**: Robust error handling and timeout protections throughout the pipeline

## Performance Metrics

The system evaluates detection performance using:
- Precision, recall, and F1 score
- Confusion matrix analysis
- Hour-by-hour spoofing pattern identification
- Anomaly score distributions

## Usage

The main execution function accepts parameters for:
- Data path configuration
- Pre-trained model loading
- Training time limits
- Hyperparameter tuning options

Results are saved as:
- Detected spoofing instances CSV
- Trained model weights
- Performance visualizations

## Research Applications

This implementation is particularly relevant for:
- Market surveillance research
- Flash crash analysis
- Reinforcement learning in financial applications
- Market integrity studies
