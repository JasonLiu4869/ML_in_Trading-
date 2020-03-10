# MachineLearningStocks in python: a starter project and guide

MachineLearningStocks is designed to be an **intuitive** and **highly extensible** template project applying machine learning to making stock predictions. My hope is that this project will help you understand the overall workflow of using machine learning to predict stock movements and also appreciate some of its subtleties. And of course, after following this guide and playing around with the project, you should definitely **make your own improvements** – if you're struggling to think of what to do, at the end of this readme I've included a long list of possiblilities: take your pick.

Concretely, we will be cleaning and preparing a dataset of historical stock prices and fundamentals using `pandas`, after which we will apply a `scikit-learn` classifier to discover the relationship between stock fundamentals (e.g PE ratio, debt/equity, float, etc) and the subsequent annual price change (compared with the an index). We then conduct a simple backtest, before generating predictions on current data.

While I would not live trade based off of the predictions from this exact code, I do believe that you can use this project as starting point for a profitable trading system – I have actually used code based on this project to live trade, with pretty decent results (around 20% returns on backtest and 10-15% on live trading).

This project has quite a lot of personal significance for me. It was my first proper python project, one of my first real encounters with ML, and the first time I used git. At the start, my code was rife with bad practice and inefficiency: I have since tried to amend most of this, but please be warned that some minor issues may remain (feel free to raise an issue, or fork and submit a PR). Both the project and myself as a programmer have evolved a lot since the first iteration, but there is always room to improve.

# Overview

The overall workflow to use machine learning to make stocks prediction is as follows:

1. Acquire historical fundamental data – these are the *features* or *predictors*
2. Acquire historical stock price data – this is will make up the dependent variable, or label (what we are trying to predict).
3. Preprocess data
4. Use a machine learning model to learn from the data
5. Backtest the performance of the machine learning model
6. Acquire current fundamental data
7. Generate predictions from current fundamental data
