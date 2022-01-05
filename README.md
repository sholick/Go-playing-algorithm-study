# Go-playing-algorithm-study

A research project started for the Advanced Algorithm course in 2020.
In the literature review, various go playing algorithms were studied, including the game's complexity and existing research conducted by researchers in the past.

In the experiment part, a simplified game of Go was programmed, and agents using strategies like minimax tree search, iterative deepening search and Monte-Carlo approaches were coded and played against each other. The brief results were recorded and analysed. Due to limitations in time and space, various ceilings have to be respected in these algorithms.

## Expected Value calculation
A demo of expanding the game tree and then displaying the estimated value of playing in each position.
The agent attempts to expand from the current state by playing into different positions on the board, assuming the opponent plays optimally.
This is in essence the minimax method, minimizing your opponent's gain and maximizing yours.
A discount rate is applied for every step into the future.<br/><br/>
<img src="https://github.com/sholick/Go-playing-algorithm-study/blob/main/minimax-tree.PNG" width="400" >
<br/>(image from jupyter notebook)

## Monte Carlo Simulation
From the current state, an agent plays many random games, every step at random, and record the wins/losses of playing that move.
The average rate is caluclated in a few batches, and the final rate is adjusted according to the variation of these numbers.
A final "goodness" value of that move is calculated.<br/><br/>
The 4 steps of a standard MCTS:
<img src="https://github.com/sholick/Go-playing-algorithm-study/blob/main/mcts.png" width="600" >
<br/>(image obtained from David Silver et al. "Mastering the game of Go with deep neural networks and tree search", Nature, 2016)

<br/>In theory, the more imaginary games simulated, the more accurate the value becomes. This can help the agent make a more educated guess of which move is better.
<br/>
<img src="https://github.com/sholick/Go-playing-algorithm-study/blob/main/MCTS_winrate_plot.PNG" width="400" >
<br/>(image from report)
