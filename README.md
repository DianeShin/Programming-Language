# my-project

<Explanation for simulateGame>
This function works by reading board/moves and converting to the inner data structures, checking if the board/move is valid, then processing the move. I made 'Board', 'Move', and 'Card' structures for simulateGameAux.

<Explanation for generateGame>
This function works by generating a random board containing random cards/number of pawns/pawn location, then reversing the board. In the ‘turn’ component, I save the ‘last player’ instead of ‘who is supposed to play’. To simplify the task, I assumed the winning situation occurs by a master pawn ending up to the opposite side.

<Explanation for countGames>
Starting from a high level image where you use nested loops by applying all combinations of pawn/card/move on a board n times, I changed the loops into a recursive form.

1. totalBoardCalculation implements calculating all possible situations of the board. It uses recursion to proceed one move by own move.
2. pawnRecursion, cardRecursion, moveRecursion goes through all possible situations via recursion. It's the same representation as if moveRecursion is the most inner loop, then cardRecursion, lastly the pawnRecursion being the outer loop. To proceed the board, I reused simulateGameAux function. However, considering that  
3. After calculating all possible board scenarios, I extract the information needed to print the result. I used length to know all possible scenarios, then checked the win flag as well as who won to print the number of winning scenarios.

<Explanation for non 100% coverage on expressions used>
I scanned through the expressions that aren't being covered and discovered these can never be covered.

1. negative integers
2. arbitrary values for boards which are only there for the object construction

<Main challenges and how I overcame>

1. Since it's my first time programming without loops, thinking about a high level image of simulateGame was easy yet changing it to a recursive manner was a challenge. Though thinking about single loop conversion to recursive manner, increasing the number of loops one by one, I was able to convert nested loops into recursion.
2. Random functions were quite hard to apply. Especially since generateGame was a pure function. I went all the journey of using randomRIO, realizing pure and impure functions are not recommended to mix, discovering randomR exists, then facing syntax issues, mixing up all the example codes online, then getting something out of it. It was quite challenging since haskell lacks examples and prior questions, it was pretty much trial and error.

<Explanation for the server log>
just mentioning since the server told me that my attempt was logged(I was just changing the submission numbers from the url), it was out of curiosity since I noticed the url is made very straight forward, and wanted to see what happens if I scan through. Will not do it again though.

