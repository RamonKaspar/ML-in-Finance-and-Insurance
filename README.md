# ML-in-Finance-and-Insurance

Coding assignments of the "Machine Learning in Finance & Insurance" course at ETH Zürich (Fall 2024).

## Assignment 1: Pricing with linear regression

This project applies linear regression and regularization techniques (Ridge, Lasso, and Truncated Pseudoinverse) on the Housing dataset to predict house prices using both numerical and one-hot-encoded categorical features. We systematically compare model performances in terms of in-sample and out-of-sample metrics. Our analysis shows that _Lasso_ achieves the best generalization, while higher-order polynomial models suffer from significant overfitting.

## Assignment 2: Credit analytics

In this project, we conducted credit analytics for consumer loans using simulated data to estimate the risk profiles of loan applicants. Focusing on three key features – age, monthly income, and employment status – we generated synthetic datasets and applied logistic regression and Support Vector Machines (SVM) to predict the likelihood of borrowers repaying their loans. Our goal was to evaluate three different lending strategies based on these predictive models to maximize profitability while managing risk, which we tested through simulations of 50,000 market scenarios. The results showed that the SVM-based lending strategy achieved the highest expected profit in simulations.

<p align="center">
    <img src="02_Credit-Analytics/plots/FDR_TPR_curves.png" width="500">
</p>
<p align="center" style="color: gray; font-style: italic;">
    <em>FDR/TPR Curves for Different Models and Datasets – a flatter curve with smaller AUC is ideal, indicating minimized loss (low FDR) and maximized business volume (high TPR).</em>
</p>

![Profit Loss Scenario](02_Credit-Analytics/plots/profit_loss_scenarios.png)

<p align="center" style="color: gray; font-style: italic;">
    <em>Profit and Loss Distributions for Lending Strategies – Strategy 3 shows the highest profits and lowest risk, indicating it’s the most effective in balancing reward and stability.</em>
</p>

## Assignment 3: Deep hedging

This project implements and compares different approaches to hedge a European call option using deep learning. We developed three strategies: a neural network ensemble (one network per time step), a single network incorporating time as a feature, and the analytical Black-Scholes Delta hedging. Using 100,000 simulated price paths with daily rebalancing over one month, we trained the networks to minimize the variance of hedging errors.

Our deep learning models achieved comparable performance to the analytical solution ($\sigma \approx 0.009$), despite not having access to the true market dynamics. The single network architecture proved particularly efficient, achieving slightly better standard deviation (0.00898 vs 0.00915) with only 40% of the parameters (1,185 vs 2,910) and reduced training time (8.7 vs 15.7 minutes). The hedging strategies become increasingly similar to the analytical solution as we approach option maturity, demonstrating the models' ability to learn the underlying financial principles.

![](03_Deep-Hedging/plots/comparison_strategies_deep_vs_analytical.png)

<p align="center" style="color: gray; font-style: italic;">
    <em>Comparison of Hedging Strategies – The neural network learns to closely replicate the analytical Black-Scholes Delta hedging strategy, particularly as the option approaches maturity.</em>
</p>

## Assignment 4: Insurance claim prediction
