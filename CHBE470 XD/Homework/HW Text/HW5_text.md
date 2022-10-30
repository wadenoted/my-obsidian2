Assigned Sunday, October 2, 2022
Homework due Friday, October 7 by 5:00 PM

# Problem 1-10 points
Problem $7.5$ in Marlin.

# Problem 2 - 10 points
Using Matlab Simulink, create a block diagram for the three-tank mixing process of example $7.2$ and 8.1. This is also the problem discussed in class. For simplicity, set $\tau=K_p=K_d=$ $K_v=1$. Answer the following questions:

&nbsp; &nbsp; i) For $K_c=0$ (no control) what are the roots of the characteristic polynomial? Is the system unstable or stable? Is the system underdamped or overdamped? The roots of the characteristic polynomial can be found using the Matlab function 'roots([a b c d])' where $a, b, c$, and $d$ are the coefficients of the characterisic polynmial, e.g. $a s^3+b s^2+c s+d$. Alternatively, you can plot the output using Simulink. You do not need to provide the plot with your solution.

&nbsp; &nbsp; ii) How does the response change for $K_c=1$ ? Is the response stable or unstable, overdamped or underdamped?

&nbsp; &nbsp; iii) How does the response change for $K_c=10$ ? Is the response stable or unstable, overdamped or underdamped?

&nbsp; &nbsp; iv) It is surprising and counter-intuitive that feedback control can change a process that is initially stable and overdamped to one that is underdamped and in some cases unstable. For the cases where the output is stable, what advantages does feedback control provide? In other words, what is the advantage of using a feedback control system with $K_c=1$ relative to the system with no control?
