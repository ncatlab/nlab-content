If $a$ is a [[dualizable object]] in a [[symmetric monoidal category]] $C$, there is a notion of the _trace_ of an [[endomorphism]] $f:a \to a$, which reproduces the ordinary notion of trace of a linear map of finite dimensional vector spaces for the case that $C = Vect$.

The idea of the trace operation is easily seen in [[string diagram]] notation: essentially one takes the endomorphism 
$a \stackrel{f}{\to} a$, "bends it around" using the duality and the symmetry and connects its output to its input.

$$
 \array{
   1 
   \\
   \;\;\;\downarrow^{tr(f)}
   \\
   1
 }
  \;\;\;
  :=
  \;\;\;
  \array{
     & 1
     \\
     & \downarrow
     \\
     a^* &\otimes& a
     \\
     \;\;\;\downarrow^{Id_{a^*}} && \;\;\downarrow^f
     \\
     a^* && a
     \\
     & \downarrow^{b_{a^*, a}} 
     \\
     a &\otimes& a^*
     \\
     & \downarrow
     \\
     & 1     
  }
$$

This definition makes sense in any [[braided monoidal category]], but often in non-symmetric cases one wants instead a slightly modified version which requires the extra structure of a [[balanced monoidal category|balancing]].

The trace of the identity $1_a:a \to a$ is called the **dimension** or [[Euler characteristic]] of $a$.

#References#

* Joyal, Street, and Verity, _Traced Monoidal Categories_  

* Dold, Albrecht and Puppe, Dieter, _Duality, trace, and transfer_
