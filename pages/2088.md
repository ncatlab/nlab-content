Coquasitriangularity is dual property to [[quasitriangular bialgebra|quasitriangularity]]. 

A $k$-[[bialgebra]] (or, in particular, [[Hopf algebra]]) $(H, m,\eta,\Delta,\epsilon)$ is __coquasitriangular__ (or dual quasitriangular) if it is equipped with a $k$-linear map $R:H\otimes H\to k$ which is invertible in [[convolution algebra]] $Hom_k(H\otimes H,k)$ (with respect to the convolution-unit $\epsilon\otimes\epsilon$) with a convolution inverse denoted $\bar{R}$ such that the opposite multiplication $m_{H_{op}} := m\circ \tau$ is given by

$$
m_{H_{op}} = R\star m\star \bar{R}
$$

and the following two identities hold when applied on $H\otimes H\otimes H$:

$$
R(m\otimes id) = R_{13} R_{23}
$$

$$
R(id\otimes m) = R_{12} R_{23}
$$

with the subscript notation as explained in the $n$lab entry [[quasitriangular Hopf algebra]]. The main examples come from quantized function algebras (that is, roughly, dual of quantized [[enveloping algebra]]s). 