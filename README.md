# AI for Tic-Tac-Toe
The traditional board game Tic-Tac-Toe, also known as Noughts and Crosses or Xs and Os, is played by two players, designated by the letters X and O, who alternately mark the squares on a 3 by 3 grid. Whoever successfully arranges three of their markers in a row—horizontal, vertical, or diagonal—is the winner.

I've used the minimax algorithm in this code to direct the computer's next step and let it crack the challenge.This programme combines the minimax approach with alpha-beta pruning.

# Combinatorics 
Combinatorics - There are only 138 terminal board positions when only the state of the board is taken into account, together with rotations and reflections on the board. A combinatorial analysis of the game reveals that when "X" always makes the initial move, the game is won as follows:

- 91 distinct positions are won by (X)
- 44 distinct positions are won by (O)
- A "cat's game" is played in which three separate positions are drawn.

# Minimax Algorithm Visualisation

# Pseudocode
```
function minimax(node, depth, isMaximizingPlayer, alpha, beta):

    if node is a leaf node :
        return value of the node
    
    if isMaximizingPlayer :
        bestVal = -INFINITY 
        for each child node :
            value = minimax(node, depth+1, false, alpha, beta)
            bestVal = max( bestVal, value) 
            alpha = max( alpha, bestVal)
            if beta <= alpha:
                break
        return bestVal

    else :
        bestVal = +INFINITY 
        for each child node :
            value = minimax(node, depth+1, true, alpha, beta)
            bestVal = min( bestVal, value) 
            beta = min( beta, bestVal)
            if beta <= alpha:
                break
        return bestVal
        
// Calling the function for the first time.
minimax(0, 0, true, -INFINITY, +INFINITY)

```
