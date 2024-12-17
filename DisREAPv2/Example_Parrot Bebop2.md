## Example: Parrot Bebop 2 Drone

The first example involves a Parrot Bebop 2 drone, whose continuous-time dynamical model is described in [Amiri et al., 2024](#amiri2024closed). The system includes six states and three control inputs, with the following constraints:

- **State constraints**:  
  - Upper bound: \( X.U.B = [10, 10, 2.57, 10, 10, 10]^\top \)  
  - Lower bound: \( X.L.B = [-10, -10, -10, -10, 0, -10]^\top \)  

- **Control input constraints**:  
  - Upper bound: \( U.U.B = [0.05, 0.05, 0.6]^\top \)  
  - Lower bound: \( U.L.B = [-0.05, -0.05, -0.6]^\top \)  

The system is discretized with a sampling period of \( \Delta T = 0.2 \), and the weighting matrices are defined as:  
- \( Q_x = \text{diag}\{5 \times I_4, 1000 \times I_2\} \)  
- \( Q_u = \text{diag}\{35, 20, 1\} \)

**Results**: Fig. 1 presents the results with the initial condition \( x(0) = [-0.48, 0, 0.46, 0, 1.08, 0]^\top \) and the reference equilibrium point \( \bar{x}_r = [0, 0, 0, 0, 1.5, 0]^\top \).

---

## System Dynamics

The linear dynamics are described in the form of Eq. (1) with the following matrices (this system has been discussed in [Amiri et al., 2024](#amiri2024closed)):

### Continuous-Time System Matrices

\[
A_c =
\begin{bmatrix}
0 & 1.0000 & 0 & 0 & 0 & 0 \\
0 & -0.0527 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 1.0000 & 0 & 0 \\
0 & 0 & 0 & -0.0187 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 1.0000 \\
0 & 0 & 0 & 0 & 0 & -1.7873
\end{bmatrix},
\quad
B_c =
\begin{bmatrix}
0 & 0 & 0 \\
-5.4779 & 0 & 0 \\
0 & 0 & 0 \\
0 & -7.0608 & 0 \\
0 & 0 & 0 \\
0 & 0 & -1.7382
\end{bmatrix},
\quad
C_c = I_6
\]

---

## Constraints and Parameters

- **State constraints**:  
  - Upper bound: \( X.U.B = [10, 10, 2.57, 10, 10, 10]^\top \)  
  - Lower bound: \( X.L.B = [-10, -10, -10, -10, 0, -10]^\top \)  

- **Control input constraints**:  
  - Upper bound: \( U.U.B = [0.05, 0.05, 0.6]^\top \)  
  - Lower bound: \( U.L.B = [-0.05, -0.05, -0.6]^\top \)  

- **Sampling period**: \( \Delta T = 0.2 \)

- **Weighting matrices**:  
  - \( Q_x = \text{diag}\{5 \times I_4, 1000 \times I_2\} \)  
  - \( Q_u = \text{diag}\{35, 20, 1\} \)

- **Initial state**: \( x_0 = [-0.48, 0, 0.46, 0, 1.08, 0]^\top \)  
- **Reference state**: \( \bar{x}_r = [0, 0, 0, 0, 1.5, 0]^\top \)
