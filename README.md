# Waste Optimization

Numerical analysis is the study of algorithms that use numerical approximation (as opposed to symbolic manipulations) for the problems of mathematical analysis. Various field of sub disciplines are applied in solving the problems. Some of the major ones are Root Finding, Function Optimization, Approximation and Interpolation and Fitting. This notebook presents an analysis of waste optimization using numerical methods. The problem being addressed is how to optimize the amount of waste burn to maximize profit while satisfying certain constraints, and also create a function such that the mayor can control the amount of waste burn by adjusting the tax.

The first part of the problem is to optimize the net profit by adjusting the amount of waste to burn. The following equation describes the net profit of the company and is plotted along with the cost and earnings of the company. 

<p align="center">
<img width="369" alt="image" src="https://user-images.githubusercontent.com/85885666/233915272-f7df39c8-6250-4f2b-9f6b-9e236a834332.png">
</p>
<p align="center">
<img width="405" alt="image" src="https://user-images.githubusercontent.com/85885666/233915460-c7f8a4e6-542d-47a8-a7c7-e46ffc5db637.png">
</p>

A function is created such that the net profit equation becomes a root finding equation when the function takes in the desired tax that the mayor wants to set it as. In the first part of the solution, we are using a root-bisect numerical method to solve it. 

The second part of the problem is to then derive a Newton-Raphson function that does not require us to compute the derivative manually but instead, approximate the derivative to solve the root problem. Finally, we then talk about the constraints and problem faces by the method that we derive in part two such as when the gradient of the function that we are finding varies rapidly, things will start to get weird as the Newton-Raphson keeps overshooting every step, making the method unstable, thus achieving NaN with some input values. Also, this method cannot differentiate more than one solution as seen when the xpos is set at 0.6. The Newton-Raphson method will keep iterating until the gradient is 0, thus it will be stuck at the local solution nearest to the xpos stated.


<p align="center">
<img width="409" alt="image" src="https://user-images.githubusercontent.com/85885666/233917324-76e6972b-574a-4ee3-8950-8c73654a2824.png">
</p>

## Requirements
To run this notebook, you need to have Python 3 installed on your machine, as well as the following packages:
<ol>
  <li>numpy</li>
  <li>scipy</li>
  <li>matplotlib</li>
</ol>

You can install these packages by running the following command using pip:
<code>pip install numpy scipy matplotlib</code>

# Usage
To use this notebook, you can either download it directly from the repository or clone the entire repository to your local machine. Once you have the notebook, you can open it using Jupyter Notebook or JupyterLab. 

To run the notebook, you can execute each cell in sequence. The notebook includes detailed explanations of each step and how it uses numerical methods to solve the different parts of the problem.

## License
The code in this repository is licensed under the MIT License. See [LICENSE.md](LICENSE.md) for more information.


