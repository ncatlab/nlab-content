We use the IIA/B Clifford matrices from _[[geometry of physics -- supersymmetry]]_ _[Example: Spinors in dimensions 11, 10 and 9](geometry+of+physics+--+supersymmetry#InDimensions11And10And9)_.

(...)

Define the following elements in $CE(\mathfrak{string}_{IIA})$: (def. \ref{TheMembraneAndStringCocycles})

$$
  \begin{aligned}
    C_2
      & \coloneqq
    \left(\overline{\psi} \wedge \Gamma^{10} \psi\right)
    \\
    C_4
      & \coloneqq
    \tfrac{i}{2}
    \left(
       \overline{\psi}
         \Gamma_{a_1 a_2}
       \psi
    \right)
    \wedge  
     e^{a_1}
     \wedge
     e^{a_2}
     \\
    C_6
      & \coloneqq
    \tfrac{1}{4!}
    \left(
       \overline{\psi}
         \Gamma_{a_1 \cdots a_4}
         \Gamma_{10}
       \psi
    \right)
    \wedge
     e^{a_1}
     \wedge
     \cdots
     \wedge
     e^{a_4}
     \\
    C_8
      & \coloneqq
    \tfrac{i}{6!}
    \left(
       \overline{\psi}
         \Gamma_{a_1 \cdots a_6}
       \psi
    \right)
    \wedge
     e^{a_1}
     \wedge
     \cdots
     \wedge
     e^{a_6}
     \\
    C_{10}
      & \coloneqq
    \tfrac{1}{8!}
    \left(
       \overline{\psi}
         \Gamma_{a_1 \cdots a_8}
         \Gamma_{10}
       \psi
    \right)
    \wedge
     e^{a_1}
     \wedge
       \cdots
     \wedge
     e^{a_8}
     \\
    C_{12}
      & \coloneqq
    \tfrac{i}{10!}
    \left(
       \overline{\psi}
         \Gamma_{a_1 \cdots a_{10}}
       \psi
    \right)
    \wedge
     e^{a_1}
     \wedge
       \cdots
     \wedge
     e^{a_{10}}
  \end{aligned}
$$

Then set

$$
  C_{IIA}
  \;\coloneqq\;
  \underset{i}{\sum}
  C_{2i}
$$

and for $p \in \{2,4,6, \cdots, 10\}$

$$
  \mu_{D p}
    \;\coloneqq\;
  [\exp(f_2) \wedge C_{IIA} ]_{p+2}
$$

where

1. $f_2$ is the extra generator in $CE(\mathfrak{string}_{IIA})$;

1. $\exp(f_2) \coloneqq \underset{k}{\sum} \tfrac{1}{k!} \underset{k \text{ factors}}{\underbrace{f_1 \wedge \cdots \wedge f_2}} $

1. $[-]_{p+2}$ denotes the summand of homogeneous degree $p+2$.

Similarly, define the following elements in $CE(\mathfrak{string}_{IIB})$ (def. \ref{TheMembraneAndStringCocycles}):

$$
  \begin{aligned}
    C_3 
      & \coloneqq
    i 
    \left(
      \overline{\psi}  
        \wedge
        \Gamma^B_{a} \Gamma_{10}
      \psi
    \right)
    \wedge
    e^a
    \\
    C_5
      & \coloneqq
    \tfrac{1}{3!}
    \left(
      \overline{\psi}
        \wedge
        \Gamma^B_{a_1 \cdots a_3} \Gamma_{9} \Gamma_{10}
      \psi
    \right)
    \wedge
    e^{a_1}
      \wedge
      \cdots
    e^{a_3}
    \\
    C_7
      & \coloneqq
    \tfrac{i}{5!}
    \left(
      \overline{\psi}
        \wedge
        \Gamma^B_{a_1 \cdots a_5} \Gamma_{9} 
      \psi
    \right)
    \wedge
    e^{a_1}
      \wedge
      \cdots
    e^{a_5}
    \\
    C_9
      & \coloneqq
    \tfrac{1}{7!}
    \left(
      \overline{\psi}
        \wedge
        \Gamma^B_{a_1 \cdots a_7} \Gamma_{9} \Gamma_{10}
      \psi
    \right)
    \wedge
    e^{a_1}
      \wedge
      \cdots
    e^{a_7}
    \\
    C_{11}
      & \coloneqq
    \tfrac{i}{9!}
    \left(
      \overline{\psi}
        \wedge
        \Gamma^B_{a_1 \cdots a_9} \Gamma_{9} 
      \psi
    \right)
    \wedge
    e^{a_1}
      \wedge
      \cdots
    e^{a_9}
  \end{aligned}
$$

Then set

$$
  C_{IIB}
  \;\coloneqq\;
  \underset{i}{\sum}
  C_{2i+1}
$$

and for $p \in \{1,3,5, \cdots 9\}$ 

$$
  \mu_{D p}
    \;\coloneqq\;
  [\exp(f_2) \wedge C_{IIB} ]_{p+2}
  \,.
$$
