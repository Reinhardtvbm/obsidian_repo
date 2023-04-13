### Modeling in the Time Domain
Concept | Understanding | Method | Extra
--------|---------------|--------|------
Frequency vs. Time Domain| Time Domain models allow for non-zero initial conditions and also allow one to represent non-linear systems | 
State-Space Representation | The set of first-order differential equations that describe a system | $$ \dot{x} = Ax + Bu $$ $$ y = Cx + Du $$ where the vector $x$ is the vector of states, $u$ is the vector of inputs and $y$ is the vector of outputs
 Number of states in a state-space representation| The minimum number of states is equal to the order of the differential equation that descibes the system
 Converting Transfer Functions into State-Space | If we take the $\mathcal{L}^{-1}$ of the transfer function equation, the a differential equation is obtained. This can then be transformed into state space like any other DE | Get the DE: $$ y^{(n)}(t) + a_{n-1}y^{(n-1)}(t) + ... + a_0y(t) = b_0u(t) $$ then the state-space (as derived in the textbook) is as follows: $$ \dot{x} = \begin{bmatrix} 0 & 1 & 0 & ... & 0 \\ 0 & 0 & 1 & ... & \vdots \\ 0 & 0 & 0 & ... & 1 \\ -a_o & -a_1 & -a_2 & ... & -a_{n-1} \end{bmatrix}x + \begin{bmatrix} 0 \\ 0 \\ \vdots \\ b_0\end{bmatrix}u $$ | for a non-const numerator in transfer function: $$ y = [b_n ... b_0]x $$
 
 
 