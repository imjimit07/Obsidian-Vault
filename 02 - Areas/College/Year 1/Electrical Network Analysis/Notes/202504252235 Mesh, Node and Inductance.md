---
date: 2025-04-25T22:35
tags:
  - Electrical
cssclasses:
  - center-images
  - page-manila
  - center-titles
---
# MESH CURRENT AND NODE VOLTAGE NETWORK ANALYSIS

## Kirchhoff’s Laws

### Voltage Law i.e. Loop Law

_The algebraic sum of all the potential difference along a closed loop in a circuit is zero._

![[Voltage Law.png]]

> When we are going opposite to the current, voltage is added and when we are going with the current we subtract.

### Current Law i.e. Junction Law

_The sum of all the currents directed towards a point in a circuit is equal to the sum of all the currents directed away from the point._

> The algebraic sum of all the currents directed towards a point is zero

![[Loop Law.png]]

## Nodal and Mesh Analysis

### Nodal Analysis

In this method, a node (junction) is taken as **ground** (reference point/node), so we will assume it has 0 V. Out of _N_ nodes that are there in the circuit, there are now _N - 1_ nodes left. Using the **Ground** node, we assign different variable to the left _N - 1_ nodes to solve the _**Voltage Law**_. We can also use the _N - 1_ nodes to solve _**Junction Law**_.

> In a resistor only circuit, there will be **N - 1** equations for each N - 1 nodes in the circuit.

After the solving the equations, we get the voltages of the nodes. Using this, we can obtain the current and voltage of anything in the circuit.

In this circuit the lower 2 nodes are the same so I merged them into the circuit on the right.
![[circuit1.png]]

Lets make the equations of Node 1 and Node 2.
$$
\begin{align*}
(G_1 + G_2)v_1 - G_1v_2 = i_1 \\
- G_1v_1 + (G_1 + G_3)v_2 = -i_2
\end{align*}
$$

The above equations can also be written as a matrix: 
$$
\begin{bmatrix}
G_1 + G_2 & -G_1 \\
-G_1 & (G_1 + G_3)
\end{bmatrix}
\begin{bmatrix}
v_1 \\
v_2
\end{bmatrix}
=
\begin{bmatrix}
i_1 \\
-i_2
\end{bmatrix}
$$
where 
**`[v]`** = vector of node voltages
**`[G]`** = node admittance matrix, whose
$$
\begin{align*}
\sum \ a_{ij} = \sum admittances \ of \ the \ node
\end{align*}
$$
Using this equation, we can find the current and voltage.

### Mesh Analysis

In this method, we make meshes i.e. loops in the circuit. We also assign a variable for the current in each mesh such as i<sub>1</sub> and i<sub>2</sub> in the circuit below.

![[circuit2.png]]

> It is better to keep the meshes clockwise to avoid errors.

Then we write the equations based on _**Loop Law**_ assuming that all components in the circuit are voltage sources.

For the above circuit:
Mesh 1:
$$
\begin{align*}
R_1i_1 + R_3(i_1 - i_2) + v_b - v_a = 0
\end{align*}
$$
Mesh 2:
$$
\begin{align*}
R_3(i_2 - i_1) + R_2i_2 + v_c - v_b = 0
\end{align*}
$$

After rearranging the equations, we get this:
$$
\begin{align*}
(R_1 + R_3)i_1 - R_3i_2 = v_a - v_b \\
-R_3i_1 + (R_2 + R_3)i_2 = v_b - v_c
\end{align*}
$$

Using this, we can find the voltages and currents. Matrix method can also be used.
$$
[R][i] = [v]
$$
Where,
`[R]` = mesh resistance (impedance)
sum of a<sub>ij</sub> = Sum of all resistances in the loop

## Inductance

### Self Inductance

_When current runs in the circuit, a magnetic field is produced. This field has its flux through the area of the loop. When current changes, flux also changes and an **emf** is induced in the loop. This is called self-induction._


$$
\phi = Li
$$
where L is self-inductance and,
	  Φ is the magnetic flux.

When current changes the induced emf produced is
$$
\mathcal{E} = \frac{-d\phi}{dt}
$$
which is also equal to
$$
\mathcal{E} = -L\frac{di}{dt}
$$

### Mutual Inductance

_When two calls are wound on a common core or placed close to each other, a part of the flux produced by one coil also links the other coil. This is called mutual inductance._

$$
\phi = Mi
$$
where M is mutual inductance.

$$
\mathcal{E} = \frac{-d\phi}{dt}
$$
which is also equal to
$$
\mathcal{E} = -M\frac{di}{dt}
$$
