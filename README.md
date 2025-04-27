

# Project Title:
Cooperative Genetic Algorithm and Deep Q-Learning for Simulated Indoor Cleaning Robots

# Project Idea:
This project is part of a graduation project at the Computer Science Department, College of Al-Jumum, Umm Al-Qura University, Kingdom of Saudi Arabia. The project aims to develop more flexible and efficient learning strategies for indoor cleaning robots by integrating two advanced techniques: Reinforcement Learning (RL), specifically Deep Q-Learning (DQL), and Genetic Algorithms (GA).

The project addresses the challenges faced by intelligent robots in adapting to dynamic environments and performing tasks efficiently under unexpected conditions, such as cleaning areas with obstacles and uneven waste distribution.

The proposal leverages the exploration strength of reinforcement learning in navigating various environments and its flexible decision-making, combined with the optimization power provided by genetic algorithms to improve performance and stability. The proposed solutions were experimentally tested and demonstrated significant improvements in efficiency and performance compared to traditional methods, enhancing the robots' ability to perform indoor cleaning tasks with greater efficiency and stability.

The project includes designing an innovative architecture that replaces the traditional gradient-based update mechanism (such as Adam Optimization) with a genetic process based on random mutations, selecting the best models based on their performance in the environment. It also includes a comparative analysis between traditional Deep Q-Learning and the hybrid model (DQL-GA) through training metrics such as rewards, episode lengths, and Q-value stability.

# Project Objective:
This project aims to develop an intelligent indoor cleaning robot using artificial intelligence techniques by combining Deep Q-Learning with Genetic Algorithms. This integration helps improve the robot’s decision-making efficiency, accelerate learning, and increase stability during training, enabling it to navigate smartly in environments with obstacles and waste, and clean them effectively and efficiently.

# Methodology:
The methodology focuses on developing a hybrid approach that integrates Deep Q-Learning (DQL) with Genetic Algorithms (GA) to enhance the performance of indoor cleaning robots in dynamic environments. The goal is to address the shortcomings of traditional DQL, such as training instability, slow convergence, and getting stuck in local optima.

- Deep Q-Learning (DQL):
  The environment is represented as a grid with waste and obstacles. The robot uses an ε-greedy policy to select actions, with a reward system that gives points for cleaning (+25 to +30 depending on the type of waste) and penalties for collisions (-2) or unnecessary movements (-1). Training is stabilized using experience replay and a target network.

- Integration with GA:
  Traditional Adam optimization is replaced with random genetic mutations to update neural network weights. Mutated models are evaluated based on their performance (fitness score), and a new model is accepted if it exceeds the previous by a threshold (+δ) to ensure significant improvements.

- Implementation:
  The robot is trained in a simulated environment (Gymnasium Environment), and performance is compared between DQL and DQL-GA based on rewards, training stability, and convergence speed.

# How It Works:
This section outlines the practical steps followed by the robot to implement the methodology in the simulation environment, as shown in diagrams (e.g., Flowchart and Sequence Diagram):

1. Initialization:
   Load the pre-trained Q-Network model and initialize the environment with randomly distributed waste and obstacles.

2. Observation:
   The robot observes its surroundings to collect data about its position and nearby obstacles.

3. Decision Making:
   Retrieve improved Q-values to select the optimal action based on the current state.

4. Execution:
   Move the robot according to the selected action.

5. Cleaning and Reward Evaluation:
   - If waste is detected, the robot cleans it and receives a reward (+25 for organic, +30 for glass, +20 for plastic, +15 for paper).
   - If a collision occurs, a penalty of -2 is applied.
   - +5 points are given for efficient movement, and a time penalty of -0.001 × number of steps is applied.

6. Update:
   Update the environment state and Q-values after each step.

7. Repeat:
   Repeat the process until the environment is fully cleaned.

8. Genetic Optimization:
   Periodically, mutations are applied to the model weights, and the best-performing model is selected based on performance.

# Technologies Used:
- Programming Language:
  Python
- Algorithms:
  - Deep Q-Learning
  - Genetic Algorithms
- Simulation Environment:
  Custom internal simulation based on the Gym framework
- Concepts:
  Neural network programming and reinforcement learning
- Training Framework:
  Interactive training environment utilizing Q-Network architecture and Replay Buffer
# Results:
1. The hybrid model (DQL-GA) outperformed traditional DQL:
   The hybrid model showed better performance in terms of stability, learning speed, and avoiding suboptimal solutions.
2. Increased learning stability:
   The reward and training curves showed less fluctuation, indicating more stable learning.
3. Improved Q-values and decision-making:
   The hybrid robot maintained higher and more accurate Q-values, leading to more effective decisions during navigation and cleaning.
4. Faster convergence to optimal solutions:
   The hybrid model required fewer training episodes to reach effective performance compared to DQL.
5. Sample efficiency:
   The hybrid model learned faster using fewer experiences, making it more time- and resource-efficient.
6. Better robustness to environmental changes (Noise Robustness):
   The model's performance remained stable despite changes and randomness in the environment, unlike traditional DQL which was more affected.

| Attempt | #1    | #2    |
| :---:   | :---: | :---: |
| first | https://github.com/user-attachments/assets/8039f091-b8a5-4dd4-94ba-2dfa845f6ea8 | https://github.com/user-attachments/assets/59bd245a-7755-42a0-83e7-83358c4a6baa |
| Seconds |  https://github.com/user-attachments/assets/39970be2-1167-48f7-9297-94c3a38805ec |  https://github.com/user-attachments/assets/12288d06-9cad-4800-9239-f17e055fd561 |
| third |  https://github.com/user-attachments/assets/2c71032a-ab37-4eab-9b8e-4a8ace049fe8 |  https://github.com/user-attachments/assets/bb40eb90-2b03-4e78-b9f0-7d1d1538ab31 |
| fourth |  https://github.com/user-attachments/assets/958abacc-aaea-42e8-9952-29d829eda269 | https://github.com/user-attachments/assets/407c360f-db18-4997-9fcd-9dd224d3ced1 |

# Future Work:
To further improve the smart robot's performance and system development, the following points can be implemented:

1. Advanced evolutionary strategies:
   Dynamically adjust mutation rates based on performance to enhance learning.
2. Hierarchical learning:
   Apply a multi-level decision-making system to increase behavior efficiency in complex tasks.
3. Multi-agent collaboration:
   Extend the model to include multiple robots working collectively to clean larger spaces.
4. Real-world deployment:
   Test the system in real scenarios like homes or offices to evaluate effectiveness beyond simulation.
5. Adding short- or long-term memory:
   Enable the robot to remember cleaned areas to reduce redundancy and improve efficiency.
6. Interaction with dynamic environments:
   Enhance the robot's ability to adapt to changes such as moved furniture or newly added obstacles.
# Conclusion:
At the end of this project, we successfully designed and developed an efficient model for an intelligent cleaning robot using modern techniques that combine reinforcement learning and genetic algorithms. The results showed that the hybrid model offers higher efficiency, better stability, and greater adaptability to changing environments. We hope this work contributes to the development of smarter and more effective robotic systems in the future.
