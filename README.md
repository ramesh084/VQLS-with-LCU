# VQLS-with-LCU
Quantum Machine Learning: Solving Linear Systems of Equations. Re-Implementation of Variational Ansatz for Solving Linear Systems from paper 
[Bravo-Prieto et al.,Variational Quantum Linear Solver. (2020)](https://arxiv.org/pdf/1909.05820.pdf)


### Background

Linear systems of equations are fundamental in mathematics and have wide-ranging applications across several fields, including physics, engineering, economics, and computer science. This kind of equation can be found when solving numerically differential equations, analyzing electrical circuits, or performing 3D transformations in computer vision. Additionally, linear systems are critical in statistical analysis, particularly in regression models, which are used to find the best-fit line for data. Their importance lies in their simplicity, versatility, and ability to provide solutions in many practical scenarios.

Considering this, solving a linear system that grows in size becomes more difficult using classical computing techniques. In particular, Carlos Bravo-Prieto et al.'s paper "Variational Quantum Linear Solver" Ref[1] shows a solution to this problem using quantum machine learning methods.

### Detailed Challenge Description

In this challenge, your goal is to reproduce the implementation of the quantum algorithm displayed in the Sec. 2.3 of the paper Ref [1], i.e. solve the following system of linear equations:

 $$\textbf{A}\vec{x}= \vec{0}$$

 $$A = \sum_{i=1}^{10} X_i  + 0.1\sum_{i=1}^{9} Z_i Z_{i+1} +I,$$


Where $X_i$, adn $Z_i$ are the respective Pauli matrices, acting over the Qubit with index $i$.
The submitted solution to this challenge consists of a quantum program written with Classiq that includes:

	1) A correct cost function and quantum ansätze 
	2) A single execution of the quantum algorithm, using the state-vector simulator
	3) The quantum program’s CX-gate count
