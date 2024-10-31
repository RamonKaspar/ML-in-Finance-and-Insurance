# ML-in-Finance-and-Insurance

Coding assignments of the "Machine Learning in Finance & Insurance" course at ETH Zürich (Fall 2024).

## Assignment 1: Pricing with linear regression

This project applies linear regression and regularization techniques (Ridge, Lasso, and Truncated Pseudoinverse) on the Housing dataset to predict house prices using both numerical and one-hot-encoded categorical features. We systematically compare model performances in terms of in-sample and out-of-sample metrics. Our analysis shows that _Lasso_ achieves the best generalization, while higher-order polynomial models suffer from significant overfitting.

## Assignment 2: Credit analytics

In this project, we conducted credit analytics for consumer loans using simulated data to estimate the risk profiles of loan applicants. Focusing on three key features – age, monthly income, and employment status – we generated synthetic datasets and applied logistic regression and Support Vector Machines (SVM) to predict the likelihood of borrowers repaying their loans. Our goal was to evaluate three different lending strategies based on these predictive models to maximize profitability while managing risk, which we tested through simulations of 50,000 market scenarios. The results showed that the SVM-based lending strategy achieved the highest expected profit in simulations.

<div style="text-align: center;">
    <figure style="text-align: center;">
    <img align="center" src="02_Credit-Analytics/plots/FDR_TPR_curves.png" width="500">
    <figcaption style="color: gray; font-style: italic;">
        FDR/TPR Curves for Different Models and Datasets – a flatter curve with smaller AUC is ideal, indicating minimized loss (low FDR) and maximized business volume (high TPR).
    </figcaption>
    </figure>
    <figure style="text-align: center;">
    <img align="center" src="02_Credit-Analytics/plots/profit_loss_scenarios.png" width="500">
    <figcaption style="color: gray; font-style: italic;">
        Profit and Loss Distributions for Lending Strategies – Strategy 3 shows the highest profits and lowest risk, indicating it’s the most effective in balancing reward and stability.
    </figcaption>
    </figure>
</div>

## Assignment 3: Deep hedging

## Assignment 4: Insurance claim prediction
