# 📋 QuantZ Week 2 (Game Day) Documentation

**Developed by Shashank Raj and used by QuantZ**

## Table of Contents
1. [Introduction](#1-introduction)
2. [Games Overview](#2-games-overview)
   - [QuantZ Options (Simplified Edition) Game](#21-quantz-options-simplified-edition-game)
   - [Monte Carlo Lottery Game](#22-monte-carlo-lottery-game)
3. [Game Setup](#3-game-setup)
   - [Installation](#31-installation)
   - [Running the Games](#32-running-the-games)
4. [QuantZ Options (Simplified Edition) Game Mechanics](#4-quantz-options-simplified-edition-game-mechanics)
   - [Game Objective](#41-game-objective)
   - [Game Rules](#42-game-rules)
   - [Game Parameters](#43-game-parameters)
   - [Scoring System](#44-scoring-system)
   - [Player Interactions](#45-player-interactions)
   - [Key Strategies](#46-key-strategies)
5. [Monte Carlo Lottery Game Mechanics](#5-monte-carlo-lottery-game-mechanics)
   - [Game Objective](#51-game-objective)
   - [Game Rules](#52-game-rules)
   - [Game Parameters](#53-game-parameters)
   - [Scoring System](#54-scoring-system)
   - [Player Interactions](#55-player-interactions)
6. [Visualizations](#6-visualizations)
7. [License and Author](#7-license-and-author)
8. [Conclusion](#8-conclusion)

---

## 1. Introduction

This documentation provides a detailed overview of the interactive games developed by **Shashank Raj** and used by **QuantZ** to enhance students’ understanding of quantitative finance and probability concepts. The games provide a unique learning experience, integrating financial simulations and interactive widgets to explore various trading and probability scenarios.

The Week 2 games are designed to enable players to engage with financial derivatives like options, simulate trading scenarios, and understand the probability of winning in lotteries through Monte Carlo simulations. The games covered in this documentation are:

1. **QuantZ Options (Simplified Edition) Game** 🎲 - An interactive trading simulator that allows players to buy, sell, or hold options over several rounds.
2. **Monte Carlo Lottery Game** 🎰 - A probability-based lottery game where players bet on numbers and observe the outcomes of simulated lottery draws.

## 2. Games Overview

### 2.1. QuantZ Options (Simplified Edition) Game 🎲

The **QuantZ Options (Simplified Edition) Game** is a trading simulator that allows players to buy, sell, or hold options based on dynamically generated option chains. Each round simulates the movement of the underlying stock price, affecting the value of options in the market.

#### Key Features:
- **Dynamic Price Movements:** Each round simulates price fluctuations based on a specified volatility.
- **Options Trading:** Players can buy or sell options with varying strikes, expiries, and premiums.
- **Portfolio Management:** The game tracks the player's portfolio over multiple rounds, handling option expiries and payouts.

### 2.2. Monte Carlo Lottery Game 🎰

The **Monte Carlo Lottery Game** is designed to illustrate probability concepts through a lottery betting system. Players bet on a number between 1 and 10, and the game simulates a random draw, showing how well players perform over multiple rounds.

#### Key Features:
- **Randomized Lottery Draws:** Each round generates a random winning number between 1 and 10.
- **Betting System:** Players can adjust their bet amount and chosen number each round.
- **Probability and Rewards:** The game rewards players for hitting the exact number or being close to the winning number.

## 3. Game Setup

### 3.1. Installation

To run the games in a Jupyter Notebook environment, ensure that the following packages are installed:

```bash
pip install -q ipywidgets matplotlib pandas numpy
jupyter nbextension enable --py widgetsnbextension --sys-prefix --quiet
```
### 3.2. Running the Games

After installing the required packages, simply run the cells containing the game code in your Jupyter Notebook. Each game will display an interactive interface with buttons and sliders for user inputs. Use these controls to play through the games.

## 4. QuantZ Options (Simplified Edition) Game Mechanics

### 4.1. Game Objective

The objective of the **QuantZ Options (Simplified Edition) Game** is to build an options trading strategy, track the performance of your portfolio, and end the game with as much capital as possible. Players can buy, sell, or hold options each round, reacting to changes in the underlying stock price.

### 4.2. Game Rules

1. **Starting Capital:** Each player starts with an initial capital of $10,000.
2. **Options Trading:** Players can buy or sell Call and Put options, each with different strikes and expiries.
3. **Price Fluctuation:** The underlying stock price fluctuates each round based on a predefined volatility.
4. **Portfolio Management:** Expired options are settled automatically, adding payoffs or deducting losses from the player's capital.
5. **Game Rounds:** The game consists of 20 rounds in total.

### 4.3. Game Parameters

| Parameter            | Description                                                       |
|----------------------|-------------------------------------------------------------------|
| `initial_capital`    | Initial capital provided to the player ($10,000).                  |
| `underlying_price`   | Initial stock price ($100), updated dynamically each round.        |
| `volatility`         | Volatility of the underlying asset (set to 5% per round).          |
| `time_steps`         | Total number of rounds in the game (20 rounds).                    |
| `option_chain`       | Options available each round, with varying strikes and premiums.   |

### 4.4. Scoring System

| Performance Metric                   | Points / Penalties                          |
|--------------------------------------|--------------------------------------------|
| Portfolio Value Increase > $5000     | "Trading Genius 🤑"                          |
| Portfolio Value Increase > $2000     | "Market Maverick 🚀"                         |
| Portfolio Value Increase > $0        | "Profit Pioneer 💰"                          |
| Portfolio Value Decrease = $0        | "Break-even Bandit 😐"                       |
| Portfolio Value Decrease < -$2000    | "Learning Trader 📘"                         |
| Portfolio Value Decrease < -$5000    | "Risky Businessman 💣"                       |

### 4.5. Player Interactions

- **Buy / Sell Options:** Select the desired option index and specify the quantity before executing trades.
- **Next Round:** Proceed to the next round, updating the portfolio based on the new stock price and option premiums.
- **End Game:** The game ends after 20 rounds, displaying the final capital and rating based on the performance.

### 4.6. Key Strategies

- **Leverage Options:** Use Call and Put options to hedge against price movements or speculate on future stock prices.
- **Monitor Option Expiry:** Track option expiries to avoid losing capital on worthless options.
- **Adjust to Price Fluctuations:** Adapt your strategy based on the simulated stock price movements.

## 5. Monte Carlo Lottery Game Mechanics

### 5.1. Game Objective

The objective of the **Monte Carlo Lottery Game** is to maximize your balance by placing strategic bets on lottery numbers. Players can choose a number each round and place a bet, winning varying amounts based on the proximity to the drawn number.

### 5.2. Game Rules

1. **Initial Balance:** Each player starts with $1,000.
2. **Betting:** Players can choose a number between 1 and 10 and place a bet amount for each round.
3. **Winning Numbers:** Each round, a random number between 1 and 10 is drawn.
4. **Payouts:** Players win 10x the bet amount for hitting the exact number, 2x for a close guess, and lose the bet amount otherwise.
5. **Game Rounds:** The game consists of 10 rounds in total.

### 5.3. Game Parameters

| Parameter            | Description                                                     |
|----------------------|-----------------------------------------------------------------|
| `initial_balance`    | Initial balance provided to the player ($1,000).                 |
| `bet_amount`         | Amount wagered each round.                                      |
| `winning_number`     | Random number between 1 and 10, generated for each round.        |
| `balance_history`    | Player's balance history over the course of the game.            |

### 5.4. Scoring System

| Performance Metric                   | Rating                                          |
|--------------------------------------|-------------------------------------------------|
| Balance Increase > $500              | "🎖️ Lottery Legend 🏆"                           |
| Balance Increase > $200              | "🍀 Lucky Gambler 🍀"                            |
| Balance Increase > $0                | "😊 Ahead Player 😊"                             |
| Balance Increase = $0                | "😐 Break-even Player 😐"                        |
| Balance Decrease < $0                | "😕 Unlucky Player 😕"                           |
| Balance Decrease < -$500             | "😞 Down on Luck 😞"                             |

### 5.5. Player Interactions

- **Place Bets:** Use the slider widgets to select the bet amount and

 chosen number.
- **Play Round:** Click the "Play Round" button to simulate the lottery draw and determine the winnings.
- **End Game:** The game ends after 10 rounds, displaying the final balance and rating based on performance.

## 6. Visualizations

Both games include visualizations to help players track their performance:

- **Capital Over Time:** Line chart displaying the player's capital/balance over the rounds.
- **Portfolio and Bet Histories:** Textual summaries of options held and bets placed each round.

## 7. License and Author

### License

MIT License

Copyright (c) 2024 Shashank Raj

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

**Acknowledgment:**  
This project makes use of Google's Gemini AI to refine parts of the notebook and generate some questions. Please note that while efforts have been made to ensure the accuracy of these questions and solutions, accuracy cannot be fully guaranteed due to the AI-generated nature of some content. Users should verify results independently where critical accuracy is required.

**Disclaimer:**  
The author, Shashank Raj, shall not be held responsible for any errors, inaccuracies, or unintended consequences arising from the use of this content, particularly from AI-generated questions and solutions. Use the content at your own risk, and the author disclaims all liability for any damages or losses arising from reliance on the content provided in this project.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES, OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT, OR OTHERWISE, ARISING FROM, OUT OF, OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

### Author

**Shashank Raj**  
Developer and Quantitative Finance Enthusiast  
President and Controller at QuantZ, Michigan State University  

## 8. Conclusion

The Week 2 games—**QuantZ Options (Simplified Edition)** and **Monte Carlo Lottery Game**—are designed to provide students with an interactive platform to explore options trading and probability concepts. By engaging with these games, players can gain a deeper understanding of financial derivatives and probabilistic outcomes. Enjoy the games, and may your trades and bets be ever in your favor!

