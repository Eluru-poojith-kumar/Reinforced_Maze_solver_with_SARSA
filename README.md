This project demonstrates how to solve a simple 4x4 grid maze using the SARSA (State-Action-Reward-State-Action) reinforcement learning algorithm. The agent starts at a defined position and aims to reach the goal while avoiding obstacles. The code uses Q-learning principles, implemented with an epsilon-greedy policy for exploration. The environment and the agent's progress are visualized after each episode and also at the end to showcase the learned policy.
Requirements
You can run the following Python code in Google Colab without any additional dependencies, except for matplotlib, which is used to visualize the maze.
bash
Copy
Edit
Install the required library (if not already available)
!pip install matplotlib
Files
maze_solver.py: The main Python script that defines the maze, the SARSA algorithm, and the functions to visualize the maze and agent's movement.
How to Run
Upload the code to Google Colab: Copy and paste the entire script into a new Python 3 notebook in Google Colab.
Run the cells: Once the script is uploaded, simply run the cells sequentially.
Visualization: After each training episode, the agent's path will be displayed on a 4x4 grid maze with the starting position marked as S and the goal as G. The agent's path during training will be highlighted with numbers representing the sequence of moves made.
Final Output: The agent will eventually reach the goal after exploring and learning the optimal policy. The final learned path will also be visualized.
How It Works
Maze Layout:
The maze is a 4x4 grid, with:
0 representing free space
1 representing obstacles
2 representing the starting position
3 representing the goal
Here's the layout:
Copy
Edit
2  0  0  0
0  1  1  0
0  0  1  0
0  0  0  3
SARSA Algorithm:
The agent explores the maze by moving in four possible directions: up, down, left, and right.
It updates its Q-values (expected future rewards) based on the SARSA update rule.
During training, the agent balances exploration (choosing random actions) and exploitation (choosing the action with the highest Q-value).
Over time, as the agent explores more, it learns to find the optimal path from the start to the goal.
Visualization:
The maze is plotted at the end of each episode, showing the agent’s path and the current state of the grid.
The path taken by the agent is marked with numbers showing the sequence of moves.
Training:
The agent is trained for 100 episodes.
After each episode, the epsilon value (which controls the exploration rate) is gradually reduced to favor exploitation as training progresses.
Final Policy:
After training, the learned policy is tested, and the agent will follow the optimal path from the start to the goal.
Code Explanation
Grid Layout: The maze is defined as a 4x4 grid with free spaces, obstacles, a start point, and a goal point.
SARSA Algorithm: The agent learns the best sequence of actions by updating the Q-values based on the reward received after each move.
Visualization: The state of the maze is displayed after each episode, and the agent’s path is traced.
Example Output
For each training episode, the agent's path will be shown along with a visualization of the current state of the maze. The output will show the following:
python-repl
Copy
Edit
Episode 1 finished.
Episode 2 finished.
Goal reached in 10 steps!
The visualizations will include:
A grid where S marks the starting point and G marks the goal.
The agent’s path during each episode will be displayed on the grid.
The learned path after the agent is trained will be shown at the end.
Final Notes
This project is a simple implementation of the SARSA algorithm for solving a maze. It can be extended to more complex environments and different algorithms, such as Q-learning or Deep Q Networks (DQN).
Feel free to modify the grid layout, the reward function, or the training parameters to experiment and see how it affects the agent’s learning process.
