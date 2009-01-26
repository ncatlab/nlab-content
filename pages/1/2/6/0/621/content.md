
Every braided [[monoidal category]] $C$ with duals has a notion of _trace_ of an [[endomorphism]], which reproduces the ordinary notion of trace of a linear map of finite dimensional vector spaces for the case that $C = Vect$.

The idea of the trace operation is easily seen in [[string diagram]] notation: essentially one takes the endomorphism 
$a \stackrel{f}{\to} a$, "bends it around" using the duality and the braiding and connects its output to its input.

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

#References#

* Joyal, Street, and Verity, _Traced Monoidal Categories_  
