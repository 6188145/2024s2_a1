# Student Information

**Course:** COMP90054 AI Planning for Autonomy

**Semester:** Semester 2, 2024

**Student:**

Yilin Chen - 1239841 - YILINC6

**Collaborated With:**

Wenda Zhang -1126164 - URL: https://github.com/COMP90054-2024s2/a1-WendaZhang08

# Self Evaluation

## Part 1

#### Self Evaluated Marks (3 marks):

3

Passed all tests

#### Code Performance 

|  Type                   | ManhattanDistance | ManhattanDistance MST | Maze Distance |
|-------------------------|-------------------|-----------------------|---------------|
| Local test Performance  | 8892              | 5217                  | 719           |

I tried three methods, namely: the simplest one uses Manhattan distance as a heuristic function; MST for Manhattan distance also uses Maze distance. Finally, it was found that only when using Maze distance can the requirement of less than 4200 expanded nodes with a full score be met.

#### Learning and Challenges
#### Ideas That Almost Worked Well
(I think these two should be combined together)

At first, I tried Manhattan distance as a simple heuristic function because I thought it was the most common solution. However, I didn't expect to find that Task 1 had requirements on the expanded node later. So, I started to try optimizing the function, including using MST and pruning the algorithm. However, I found that 4200 was a very difficult threshold, and even though I thought it had been optimized well, it still couldn't meet the requirements. This is what I think is the most difficult point in Task 1.
Later, after discussing with Wenda Zhang and searching for information, we believe that Maze distance may be the solution to this problem.
The most difficult method among them should be the implementation of Maze distance, because this method has never been used before, but it was eventually implemented, which excites me.

#### Comparison with sample solution
As expected, Task 1 in the final answer also uses Maze distance, which indicates that our idea is correct and I feel very satisfied.


#### New Tests Shared @ ED
Nothing

#### Justification
I passed all the hidden tests


## Part 2

#### Self Evaluated Marks (4 marks):

4

Passed all tests

#### Code Performance
*** Search time: 0:00:00.018552
*** PASS: marking/part2/cbs_test.test
*** Search time: 0:00:02.151439
*** PASS: marking/part2/hidden_cbs_test_1.test
*** Search time: 0:00:02.779104
*** PASS: marking/part2/hidden_cbs_test_2.test
*** Search time: 0:00:02.944159
*** PASS: marking/part2/hidden_cbs_test_3.test
*** Search time: 0:00:03.598111
*** PASS: marking/part2/hidden_cbs_test_4.test

Very good performance, no more than five seconds of running test

#### Learning and Challenges
I have encountered many challenges and learned many lessons on this issue. The main challenge is the issue of code execution timeout. When the search problem is complex, code execution will time out. I didn't spend too much time on the initial implementation of the code. I spent a lot of time trying to improve the efficiency of the algorithm. Finally, these improvements have indeed shortened the execution time of the code. I understand the importance and difficulty of writing efficient code. At the same time, it is important to carefully examine where the problem lies in different conflicts. Later, Wenda and I discovered that even if our code is optimized well, there is a timeout issue. This is due to the difference in new_comtrants. In the vertex conflict, both pacman appends are (pos1, pos2), but in the swap scenario, they need to swap positions.

Sometimes, the code passes through test cases and prompts that the solution has not found the optimal path. In this solution, each reagent is stopped at the food location. In fact, agents can move forward after eating food. I didn't consider this case, so I found a longer solution. Finally, I realized this issue.

#### Ideas That Almost Worked Well

When collaborating with Wenda on code, her ideas were very inspiring. Later, I improved my original code (which I had written before working with Wenda that couldn't pass many hidden tests) and submitted it to Git. The code ideas I implemented in collaboration with Wenda were almost the same, except for some structural optimizations,

#### Comparison with sample solution
Fortunately, there is not much difference in approach compared to the sample solution, both are implementations of CBS, with only some differences in code structure

#### New Tests Shared @ ED
Nothing

#### Justification
I passed all the hidden tests