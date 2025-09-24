# Lab Project 2: Sampson’s Monks

# Name: 

# Part 0

# For part 0 of the project, the task was to install and load the lda, igraph, and networkd3 packages to load the required data. 
# Part 1 - Visualizing the Network

Forming the desired matrix that would necessitate running dataframes of nodes and edges, as required by the networkD3. This was done by using the SAMPLK2 Network plot.

# We plot the graph using the Igraph
A Static Visualization of the Monks by using the igraph::plot.igraph() function.
![Image Alt](https://github.com/jameskamau646-debug/project/blob/408eda9c4b2783642c0d879da7d8d9a30f21a85f/Static_plot.png)

This chart shows that the overall structure of the monks is directed. The arrows indicate which monk is liked by another monk, and the density of the connections implies that the majority of the monks are interconnected. 
However, the ties are not evenly distributed. 
# For the second plot of part 1, the idea was first to create an adjacency matrix, then convert it to nodes and edges data frames that would help to visualize the data interactively.
# Plotting an Interactive plot using networkD3
An Interactive visualization of the Monks Using the networkD3::forceNetwork() function.

This shows interactive Monks 
# Part 2 - Summary Statistics
# Here are the Results
$degree_out
 ROMUL_10 BONAVEN_5 AMBROSE_9   BERTH_6   PETER_4  LOUIS_11  VICTOR_8   WINF_12    JOHN_1    GREG_2   HUGH_14 
        3         4         3         3         3         3         3         3         3         3         3 
  BONI_15    MARK_7 ALBERT_16  AMAND_13   BASIL_3  ELIAS_17   SIMP_18 
        3         3         4         4         3         3         3 
$degree_in
 ROMUL_10 BONAVEN_5 AMBROSE_9   BERTH_6   PETER_4  LOUIS_11  VICTOR_8   WINF_12    JOHN_1    GREG_2   HUGH_14 
        8         8         1         5         7         2         3         2         1         1         2 
  BONI_15    MARK_7 ALBERT_16  AMAND_13   BASIL_3  ELIAS_17   SIMP_18 
        4         2         2         2         2         2         3 
$average_
[1] 1.947368

From the degree analysis, we see that out-degrees are relatively balanced, with most nodes sending ties to 3 or 4 others, suggesting fairly even outward connectivity. 
However, in-degrees vary more widely, ranging from 1 to 8, indicating that some individuals, for instance, ROMUL_10, BONAVEN_5, are highly popular or central, while others receive few ties. 
The average degree of 1.9474 highlights a moderately sparse network overall, meaning most nodes are connected to only a small fraction of the group, 
reflecting selective or hierarchical relationships rather than widespread interaction. Overall, the average tie strength was 1.9474, and the most liked monk was ROMUL_10, while the least liked monk was AMBROSE_9.

# Part 3 - A Simple Model of a Social Network
For this part, a function was written to generate a random socio matrix. In this function, each monk is assigned likes at random. 
18 monks were used as n, and the probability of liking was set as default (0.3), and the maximum ti strength was also set. 




# Part 4 - Comparison: Model vs Observations
The Summary Statistics are as shown below. 
$degree_out2
 monk1  monk2  monk3  monk4  monk5  monk6  monk7  monk8  monk9 monk10 monk11 monk12 monk13 monk14 monk15 monk16 
     4      4      7      4      3      6      4      5      4      4      5      4      7      5      5      5 
monk17 monk18 
     1      7 
$degree_in2
 monk1  monk2  monk3  monk4  monk5  monk6  monk7  monk8  monk9 monk10 monk11 monk12 monk13 monk14 monk15 monk16 
     5      3      5      4      5      7      6      4      4      4      5      3      4      7      4      5 
monk17 monk18 
     5      4 
$average_2
[1] 1.988095

The results with the Monk network showed a clear structure for static and interactive plots. The results of the mean indicated that the tie strength was 1.947, and the most liked monk was ROMUL_10, 
while the least liked monk was AMBROSE_9. The degrees for the random model network were more evenly distributed. This means that no popular or unpopular monks stood out. 
Comparing them with the Sampson's monk structure, they had no strong community structures. Finally, on reflection, 
It was observed that the observed networks had meaningful patterns that were not clear in the generated monks. 

