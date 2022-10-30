Assigned Sunday, September 25, 2022
Homework due Friday, September 30 by 5:00 PM

Read Sections 4.0 - 4.4, 4.6, 5.1, 5.2, 5.4, 5.5, 5.7, and 5.8 in the textbook and answer the following questions:

# Problem 1 - 10 points Problem 4.10 in Marlin.

# Problem 2 - 10 points Problem 5.4

# Problem 3 - 10 points
Using Matlab Simulink, create a block diagram for the process in problem 5.4. Use a value of $\tau=5$ and $K=5$ for each block. Plot the output for a step change of $C_{A o}^{\prime}$ of magnitude 1 and answer the following questions:

i) What is the final steady state value of $C_{A 4}^{\prime}$ after the step change?
ii) What is $\tau_{63}$ ? Use the overall transfer function to determine this by summing all of the time constants in each transfer function together.
iii) Use your plot to determine how long it actually takes for $C_{A 4}^{\prime}$ to reach $63 \%$ of the final steady state value. How does this compare with the value of $\tau_{63}$ ?

To open Simulink, simply click on the 'Simulink' button from the main Matlab window. From there, you can click on "Library Browser" to add blocks to your simulation. Some that you need may be under "commonly used blocks." If not listed there, the Step block is in "Sources", Transfer Fcn block is in "Continuous", the Mux block (used to plot multiple signals on a single plot) is in "Signal Routing", and Scope is in "Sinks." You can also use the search function to search for blocks by name. To create a block diagram, simply drag each block into your simulation window, double click to modify values, and then connect by connecting arrows between blocks.
