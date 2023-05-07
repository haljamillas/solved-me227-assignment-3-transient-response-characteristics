Download Link: https://assignmentchef.com/product/solved-me227-assignment-3-transient-response-characteristics
<br>
This past week in class we looked at the transient response characteristics of the bicycle model with linear tires. The conclusions reached from this simple model can be extrapolated to many more complicated vehicle dynamics problems so it makes sense to get some familiarity with the model and, in particular, what it means for pole locations and response characteristics.

<h1>Instructions</h1>

This and following homework assignments will be submitted using two different tools, Gradescope and MATLAB Grader. Throughout the assignment, each prompt will be marked with either <strong>Gradescope </strong>or <strong>MATLAB Grader </strong>to make it clear where you should be submitting the answer to that problem. MATLAB Grader questions will also be shown in <strong>Blue </strong>to make them easy to see.

All written portions must be turned in through Gradescope. See the Piazza post on homework guidelines for more instructions on the different homework resources available to you. Whatever format you decide to use, please <strong>BOX </strong>all of your final answers.

Some problems will make use of the MATLAB Grader suite discussed in class. These problems are available directly from Canvas by clicking on each individual question. You are allowed to submit code to MATLAB Grader as many times as you want before the due date without penalty. In this way you can be sure each function or script passes all of the assesments that go along with it before moving on to the next problem. We encourage you to write your own test cases as well to ensure your code is working as expected.

1

<h1>Problem 1 – Weight Distribution and Cornering Stiffness</h1>

Both tire corning stiffness and weight distribution play a role in determining the car’s understeer gradient. While some properties depend only upon the understeer gradient, other properties of the response depend upon the specific combination of weight balance and cornering stiffnesses that produced that understeer gradient. Let’s look at how cars with the same understeer gradient can vary in transient performance.

<h2>Question 1.A – Understanding Components of the Understeer Gradient (Gradescope)</h2>

Which of the following properties depend only on the understeer gradient and the wheelbase of the vehicle and which depend upon the manner in which the understeer gradient was achieved (specific cornering stiffnesses and mass distribution): stability, steady-state yaw rate, critical or characteristic speed, natural frequency, damping ratio? Select either Option 1 (Only K and/or L) or Option 2 (Components of K).

<em>Select the correct answer for each property.</em>

<strong>Stability:</strong>

Option 1: Only <em>K </em>and/or <em>L</em>

Option 2: Components of <em>K</em>

<strong>Steady-state Yaw Rate:</strong>

Option 1: Only <em>K </em>and/or <em>L</em>

Option 2: Components of <em>K</em>

<strong>Critical or Characteristic Speed:</strong>

Option 1: Only <em>K </em>and/or <em>L </em>Option 2: Components of <em>K</em>

<strong>Natural Frequency:</strong>

Option 1: Only <em>K </em>and/or <em>L </em>Option 2: Components of <em>K</em>

<strong>Damping Ratio:</strong>

Option 1: Only <em>K </em>and/or <em>L </em>Option 2: Components of <em>K</em>

<h2>Question 1.B – Calculating the Understeer Gradient (Gradescope)</h2>

Consider the following vehicles:

<table width="356">

 <tbody>

  <tr>

   <td width="155"> </td>

   <td width="100">Car A</td>

   <td width="100">Car B</td>

  </tr>

  <tr>

   <td width="155">Wheelbase</td>

   <td width="100">2.4 m</td>

   <td width="100">2.4 m</td>

  </tr>

  <tr>

   <td width="155">Mass</td>

   <td width="100">1600 kg</td>

   <td width="100">1600 kg</td>

  </tr>

  <tr>

   <td width="155"><em>I<sub>z</sub></em></td>

   <td width="100">2200 kg· m<sup>2</sup></td>

   <td width="100">2200 kg· m<sup>2</sup></td>

  </tr>

  <tr>

   <td width="155">Weight Distribution</td>

   <td width="100">60/40</td>

   <td width="100">65/35</td>

  </tr>

  <tr>

   <td width="155">Tire Cornering Stiffness</td>

   <td width="100">100,000 N/rad</td>

   <td width="100">150,000 N/rad</td>

  </tr>

 </tbody>

</table>

Verify that both cars have the same understeer gradient. Converting to degrees/g, where does the value of understeer gradient fall in a range of 0-3 deg/g with 0 representing a neutral steering car and 3 representing a fairly high degree of understeer?

<em>Show your work verifying that the two cars have the same understeer gradient. Write that understeer gradient below and answer where the understeer gradient falls in that range.</em>

<h2>Question 1.C – Calculating Dynamic Properties (Gradescope)</h2>

For each vehicle, calculate the characteristic speed and then the steady-state yaw gain, natural frequency and damping ratio at a speed of 65mph (be sure to convert to m/s first). The properties are given again below:

<table width="356">

 <tbody>

  <tr>

   <td width="155"> </td>

   <td width="100">Car A</td>

   <td width="100">Car B</td>

  </tr>

  <tr>

   <td width="155">Wheelbase</td>

   <td width="100">2.4 m</td>

   <td width="100">2.4 m</td>

  </tr>

  <tr>

   <td width="155">Mass</td>

   <td width="100">1600 kg</td>

   <td width="100">1600 kg</td>

  </tr>

  <tr>

   <td width="155"><em>I<sub>z</sub></em></td>

   <td width="100">2200 kg· m<sup>2</sup></td>

   <td width="100">2200 kg· m<sup>2</sup></td>

  </tr>

  <tr>

   <td width="155">Weight Distribution</td>

   <td width="100">60/40</td>

   <td width="100">65/35</td>

  </tr>

  <tr>

   <td width="155">Tire Cornering Stiffness</td>

   <td width="100">100,000 N/rad</td>

   <td width="100">150,000 N/rad</td>

  </tr>

 </tbody>

</table>

<strong>Hints:</strong>

<ul>

 <li><strong>Make sure your understeer gradient, </strong><em>K</em><strong>, is in units of rad/m/s</strong><sup>2</sup><strong>. </strong>• <strong>You can use Matlab online (matlab.mathworks.com) to write reusable functions to reduce the risk of algebra mistakes.</strong></li>

</ul>

<em>Calculate the characteristic speed, steady state yaw gain, natural frequency, and damping ratio. Put your final solutions below.</em>

<h2>Question 1.D – Comparison to the Kinematic Model (Gradescope)</h2>

For each vehicle, you calculated the steady-state yaw gain. Calculate the steady-state yaw gain predicted by the kinematic model at 65mph (hint: it is the same for both vehicles). You can use a small angle assumption. The properties are given again below:

<table width="356">

 <tbody>

  <tr>

   <td width="155"> </td>

   <td width="100">Car A</td>

   <td width="100">Car B</td>

  </tr>

  <tr>

   <td width="155">Wheelbase</td>

   <td width="100">2.4 m</td>

   <td width="100">2.4 m</td>

  </tr>

  <tr>

   <td width="155">Mass</td>

   <td width="100">1600 kg</td>

   <td width="100">1600 kg</td>

  </tr>

  <tr>

   <td width="155"><em>I<sub>z</sub></em></td>

   <td width="100">2200 kg· m<sup>2</sup></td>

   <td width="100">2200 kg· m<sup>2</sup></td>

  </tr>

  <tr>

   <td width="155">Weight Distribution</td>

   <td width="100">60/40</td>

   <td width="100">65/35</td>

  </tr>

  <tr>

   <td width="155">Tire Cornering Stiffness</td>

   <td width="100">100,000 N/rad</td>

   <td width="100">150,000 N/rad</td>

  </tr>

 </tbody>

</table>

How do the steady-state yaw gains predicted by each model compare?

<em>Calculate the kinematic model gain. Explain how it is different from the gains you calculated. Put your answers below.</em>

<h2>Question 1.E – Understanding Components of the Understeer Gradient (Gradescope)</h2>

Let’s see if we can understand the relationships between the physical properties of cornering stiffness and weight distribution and the car’s natural frequency. First, if we <strong>keep the understeer gradient constant</strong>, does stiffening the tires increase or decrease natural frequency? Similarly, for a <strong>constant understeer gradient</strong>, does placing more of the weight of an understeering car on the front axle increase or decrease the natural frequency?

<em>Circle your answers below.</em>

Stiffening the tires will                                    the natural frequency:

( Increase / Decrease )

Placing more weight on the front wheel will                                     the natural frequency:

( Increase / Decrease )

<h1>Problem 2 – Simulating Vehicles with Different Responses</h1>

In this problem, you will implement a simulation to compare the two cars we have looked at in response to a step steering input. Step inputs are common ways to characterize dynamic systems (both open and closed loop).

<h2>Question 2.A – Simulation (MATLAB Grader)</h2>

One way to think about the handling characteristics of a car is that a better handling car more closely tracks the driver’s steering input. Follow the prompt in MATLAB Grader to simulate the response of both of these vehicles to a steep steer of 1 degree at 65mph using the simulation you developed last week with the linear tire model and small angle approximations for 4 seconds and plot the yaw rate.

<h3>Question 2.B – Analysis (Gradescope)</h3>

Which car seems to track the step response more closely? How can you tell?

<em>Write your answers below.</em>

<h1>Problem 3 – Stabilizing the Oversteering Car</h1>

While an oversteering car can become unstable beyond its critical speed, a driver can stabilize it. We’ll see if a simple feedback law involving the driver can prove this mathematically. Assume that the driver is trying to track a desired yaw rate and can sense the actual yaw rate. Assume also that the driver can respond without delay and turns the wheels in proportion to the difference between the desired and actual yaw rates, using the gain, <em>K</em><sub>driver</sub>. In other words, the driver input as a function of time looks like:

<em>δ</em>(<em>t</em>) = <em>K</em>driver(<em>r</em>des(<em>t</em>) − <em>r</em>(<em>t</em>))

Or, Laplace transforming, our model of the ”perfect” driver can be written as:

∆(<em>s</em>) = <em>K</em>driver(<em>R</em>des(<em>s</em>) − <em>R</em>(<em>s</em>))

<h2>Question 3.A – Closed Loop Transfer Function (Gradescope)</h2>

Eliminate the steering angle and show that the closed-loop transfer function of the driver and vehicle combined from desired yaw rate to yaw rate is:

<em>Hint: </em>You can make the algebra simpler on yourself by writing the transfer function as

and doing the algebra before subbing the coefficients back in.

<em>Derive the closed loop transfer function given above.</em>

<h2>Question 3.B – How Good Should a Driver Be? (Gradescope)</h2>

Given a speed, <em>U<sub>x</sub></em>, the wheelbase, <em>L</em>, and an understeer gradient, <em>K</em>, what is the value of <em>K</em><sub>driver </sub>that stabilizes the car? You should be able to find an expression that uses only these terms.

<em>Show an expression for K</em><em><sub>driver </sub></em><em>using only these terms.</em>

<h2>Question 3.C – Pole/Zero Locations (Gradescope)</h2>

Assume you have an oversteering car with a mass of 1800 kg, 40/60 weight distribution, wheelbase of 2.6 m, moment of inertia of 2600 kg·m<sup>2 </sup>and cornering stiffness front and rear of 100,000 N/rad. For this parameter set, calculate pole and zero locations for a speed of 30 m/s and then sketch the root locus corresponding to the controller in part A. It should align with your result in part A.

<em>Make a root/locus plot (can be hand-sketched and scanned or made using MATLAB/Python) and include it along with pole and zero locations below.</em>

<h1>Problem 4 – Lateral Velocity as a Function of Speed (Gradescope)</h1>

The lateral velocity can be a little harder to understand intuitively than the yaw rate (which is just angular velocity). In a steady corner, the lateral velocity describes the orientation of the vehicle centerline relative to the circular path the vehicle is taking. This can be important to understand for automated vehicles since sensors are often attached to the vehicle and if the vehicle is not pointing straight along the path, we will need to compensate in some way. In the last assignment, you noticed that the lateral velocity of the vehicle changes sign as the speed increases. Let’s look at this in a little more detail.

The transfer function for lateral velocity with respect to steer angle is given by:

The denominator of this transfer function is the same as the yaw rate transfer function we covered in class. This should make sense, given the relationship between steer angle and these state. In this problem you will use this function to relate lateral and longitudinal speed.

Please answer the following questions:

<ul>

 <li>What is the steady-state lateral velocity for a step steer input of magnitude <em>δ</em>?</li>

 <li>At what longitudinal speed does the vehicle produce a zero lateral velocity?</li>

 <li>If the vehicle is in a left hand turn (positive steer angle), what sign does the lateral velocity have below this speed?</li>

 <li>What sign does it have above this speed?</li>

</ul>

You should see a similarity between the low speed behavior and the kinematic model behavior you derived on the first homework assignment. At higher speeds, slip angles become important and the dynamic model differs from the kinematic model in terms of the vehicle’s orientation relative to the path.

<em>Write your answers to the questions below.</em>

<h1>Problem 5 – Simulation of Lateral Velocity</h1>

In this problem, you will simulate the vehicles from the last problem at different speeds. We will investigate how the lateral velocity changes at these speeds.

<h2>Question 5.A – Zero Lateral Velocity Speed (Gradescope)</h2>

Calculate the speed at which Car A from Problem 1 has a zero lateral velocity in steady-state.

<em>Enter your answer below.</em>

<h2>Question 5.B – Simulation (MATLAB Grader)</h2>

Following the prompt in MATLAB Grader, simulate 1 degree step steer inputs for Car A at

<ul>

 <li>The speed you just calculated</li>

 <li>Twice that speed</li>

 <li>Half that speed</li>

</ul>

over a time period of 4 seconds. Plot the lateral velocity for each of these three speeds on the same plot.

<h3>Question 5.C – Analysis of Plot (Gradescope)</h3>

How do the shapes of these responses reflect your results from Question 4?

<em>Enter your answer below.</em>