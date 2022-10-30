Assigned Sunday, September 11, 2022
Homework due Friday, September 16 by 5:00 PM

Read Section 4.1 in the textbook and answer the following questions:

# Problem 1 - 10 points
Problem 3.5 in Marlin. There is no need to provide a numerical answer, just provide the expression for the outlet concentration. The expression below will be useful:

$$
\int \exp (t / \tau) \sin (\omega t) d t=\left[\frac{\tau \sin (\omega t)-\omega \tau^2 \cos (\omega t)}{1+\omega^2 \tau^2}\right] \exp (t / \tau)+I
$$

Set $A=1$ and $\tau=1$ and plot both the disturbance in the inlet concentration and the deviation in the outlet concentration for three different cases: i) $\omega=10$ which corresponds to $\omega \tau>1$, ii) $\omega=1.5$ which corresponds to $\omega \tau \approx 1$, and iii) $\omega=0.1$ which corresponds to $\omega \tau<<1$. For the plot, you can ignore the decaying term in the solution, e.g. assume that $t>>\tau$. Note that when you prepare these plots, you will have to adjust the total time plotted.

Explain in words how the deviation in the outlet concentration differs between the three cases.

# Problem 2 - 10 points
Problem 3.4 in Marlin. Note that this is a dynamic problem, but it does not involve a disturbance and so you will not use deviation variables.

Hint: When the tank is being filled, the volume of liquid is not constant. The left hand side of your conservation equation should be

$$\frac{\text{d} (VC_A)}{\text{d}t}$$
and
$$V=Ft$$

By expanding the derivative and grouping terms as we have done in class, you can solve the differential equation using an integrating factor. Note that the integrating factor will be different than the examples we have seen in class. Also, there is no flow of liquid out of the reactor during filling. You will also have to apply L’Hopital’s rule when applying the initial condition to solve for a constant in the final expression. The initial condition is $C_A = C_{A0}$

# Problem 3 - 10 points
In this problem, you will analyze an underdamped isothermal reactor. This problem is discussed briefly in section 3.6 of the textbook, and we discussed it in class. The coolant flow rate is the disturbance variable.

I created a Matlab script which plots the approximate solution to the non-linear differential equations by using Euler’s method (see Eq. 3.72 in the textbook). This script is available in Canvas and you will need it to complete this problem. The filename is ’UnderdampedReactor.m’.

The script models the temperature and concentration in the nonisothermal reactor after a step change in the coolant flow rate. The initial coolant flow rate is 0.5, and after 100s there is a disturbance. The magnitude of the disturbance is given by the variable ’deltafc’ which is an input to the script. The script will plot the temperature and concentration as a function of time (out to 500 seconds) and also outputs the final values of concentration and temperature (’CAn’ and ’tn’, respectively). Use the script to answer the questions below.

You do not need to provide plots, just use the code to analyze the reactor behavior and answer the questions below:

1) The script can be used to find the steady-state values of concentration and temperature for a specific set of conditions. For example, set ’deltafc’ equal to 1. What are the values of temperature and concentration for the new steady state? Does the reactor temperature and concentration CA increase or decrease due to the change in deltafc? Are these results reasonable? The initial steady state values for temperature and concentration are approximately 471.45 and 0.0488. These can be found by setting ’deltafc’ equal to 0.

2) Increase ’deltafc’ further, in increments of 1 up to at least 20. Also, test values between 0.1 and 1. Over what range of disturbance values do you see periodic behavior? Explain why the periodic behavior disappears at very high or very low values of deltafc.

3) The disturbance can also be in the negative direction. Test values of ’deltafc’ below 0 to -0.49. 0.5 is the initial coolant flow rate, so ’deltafc’ should not be -0.5 or lower. Is there periodic behavior for negative values of ’deltafc’? Why or why not?

4) The heat of reaction can be modified by changing the ’DH’ parameter. Set the value of ’DH’ equal to zero. Is there any non-periodic behavior? Why or why not? What is the effect of setting ’DH’=0 on the conversion of A?

Note: you will have to recalculate the initial steady state values of T and CA after you change ’DH’. To do this, after setting ’DH’ equal to 0, first run the script for ’deltafc’ equal to zero. The final values for temperature and concentration are the initial steady state for ’DH’ equal to 0. Modify the script by inserting these values for ’TAs’ and ’CAs’, then run the script for positive and negative values of ’deltafc’ and answer the questions above.

# Problem 4 - 10 points
Repeat Problem 1, except include a first-order chemical reaction ($r_A = -kC_A$) and use the Laplace Transform to solve the ordinary differential equation. The Laplace transform and inverse Laplace transform are provided in Table 4.1 of the textbook.