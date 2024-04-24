Brief Summary (Problem Statement and Solution): The problem entails optimizing a System on a Chip (SoC) architecture, focusing on its Network on Chip (NOC). The goal is to design an efficient NOC that ensures minimal latency, achieves 95% of maximum bandwidth, supports 90% buffer occupancy, and throttles only 5% of the time based on power thresholds. The setup includes a simulator with APIs for controlling buffer size, arbiter weights, and throttling. The NOC connects CPU, IO peripherals, and memory, with traffic patterns influenced by workload types. Efficient design is crucial to balance area, power, and performance for target workloads. The solution for this problem statement assumes that after each read and write operation there will be a token released by the system in the form of “Data” followed by the address of the memory address upon which the read or write instruction has been implemented. The solution aims to average out the write and read latency over time by evaluating the read count and write count and then evaluating latency by adding the difference in timestamps when token is received and the timestamp when instruction was received. Similarly, the code evaluates the bandwidth by evaluating how many bytes are being used for each instruction i.e, evaluating total bytes over total cycles.

For Reinforcement Learning, we need to define the MDP, which includes the states, actions, rewards and the transition model.
 
We want to achieve optimal values for Buffer Occupancy values for each buffer, arbitration rates for each arbiter,read and write latency for CPU and IO, Bandwidth of CPU and IO and the power threshold status

The transition model would be deterministic, changing the values of the state parameters as exactly defined by the actions.
The action space and state space would be continuous as well.
Considering the complexity and dynamic nature of the problem, an algorithm like Deep Q-Network (DQN) could be suitable for this RL framework. DQN is capable of handling complex state spaces and continuous actions, making it suitable for optimizing the NOC design parameters.





