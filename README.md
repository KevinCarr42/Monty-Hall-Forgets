# Monty Hall Forgets

Like the normal Monty Hall paradox, but this time he can't remember where the car is. This is based on a conditional probability question on Brilliant.org. I didn't think the answer was correct, so I coded it in Python. I got the answer I expected based on conditional probabilities using simulation.

## Original Question (from Perplexing Probabilities at Brilliant.org):

Suppose again that there are 33 doors and 11 car, but now Monty Hall forgets which door the car is behind. Thus, after you choose your door, Monty Hall opens 11 of the 22 remaining doors at random. (This means that he might accidentally open the door with the car behind it, in which case you would have to start the game over.)

Assume that Monty Hall is equally likely to place the car behind any of the 33 doors, and, after you have chosen your door, he is equally likely to open either of the 22 remaining doors (even if the car is behind one of them).

If the door that Monty Hall opens has a goat behind it, what is the probability that you win if you switch?
* 1 / 3
* 1 / 2
* 2 / 3

ANSWER: 1 / 2

## Explanation:
![alt text](https://github.com/KevinCarr42/MontyHallForgets/blob/main/MontyHallForgets-Solution.png)

## Why I Disagree

In the above solution, the situations where Monty reveals the car by accident are impossible. From above, "he might accidentally open the door with the car behind it, in which case you would have to start the game over." Therefore the cases where Monty accidentally reveals the car do not count towards the odds; the game resets. 

Therefore, forgetful Monty is functionally equivalent to the Monty who knows where the car is because the game cannot possibly include situations where he chooses incorrectly. Logically, the odds should be 2/3 as in the original paradox (if you switch), not 1/2.

Here is an alternate way of considering the logic: There is a 1/3 chance you initially picked the car, so the remaining doors must contain the remaining 2/3 odds. If the Monty shows you a goat, the entire 2/3 odds collapses to the remaining door.

To confirm my logic, I calculated everything algorithmically using Python. My simulation shows 2/3, not the 1/2 as claimed by Brilliant.

## Conclusion

Please let me know if I am missing something. I asked Brilliant and they stick by their 1/2, but I just can't see it.
