# NTR Project - Adaptive Resource Optimization into 5G Radio Resource Management

## Project Overview
The main objective of this project was to develop a simulation to evaluate two different network resource allocation algorithms, namely MaxSNR and Round Robin, within the context of 5G Radio Resource Management. The simulation aimed to measure the throughput and latency experienced by simulated users connected to various access points, while considering different parameters such as the resource allocation algorithm, the number of network cells, the number of connected users, and the time slot duration.

## Simulation Structure
The simulation consisted of various key elements that interacted to mimic the behavior of a real-world 5G network:

Access Points and Resource Units: Each Access Point was responsible for allocating a fixed number of resource units, set at 128 in this simulation, to the connected users. Resource units were allocated in groups of 4 to enable users to transmit packets they wanted to emit.

Users and Packets: The users were divided into two groups - near users and far users. Near users had a higher mean throughput (6 units) compared to far users (3 units). Users attempted to generate packets of 100 bits randomly, with a 25% probability to generate one during each time slot. These packets were then stored in a buffer, awaiting transmission.

Resource Allocation Algorithms: The simulation supported modularity in designing resource allocation algorithms through an interface. Two algorithms, Round Robin and MaxSNR, were implemented in this version of the simulation.

## Parameters and Variations
The simulation allowed for the variation of four essential parameters:

Resource Allocation Algorithm: Researchers could choose between MaxSNR and Round Robin to study their impact on network performance.

Number of Network Cells: The simulation could be configured with either one or two network cells. In the case of two cells, peripheral users from each cell would interfere with each other.

Number of Connected Users: The number of users connected to each access point could vary from 2 to 192, providing insights into the system's scalability.

Time Slot Duration: Time slots were represented by a fixed time duration of 2ms, and the simulation was run for 200 iterations, capturing network performance over time.

## Build and Execution
To run the simulation, users could simply navigate to the project directory and execute the make command for building and then use make run to run the simulation.

Overall, the NTR Project provided a valuable tool for researchers and engineers to evaluate and compare the performance of different resource allocation algorithms within a 5G network. The simulation's modular design allowed for easy integration of new algorithms, potentially fostering further research and development in the field of 5G Radio Resource Management.