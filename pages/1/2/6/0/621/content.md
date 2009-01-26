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
     a^* &\otimes& a
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

#Examples#

* $C = Vect$ with its standard monoidal structure ([[tensor product]] of vector spaces): in this case tr(f) is the usual trace of a linear map;

* $C = SuperVect = (Vect_{\mathbb{Z}_2}, \otimes, b)$, the category of $\mathbb{Z}_2$-graded vector spaces with the _non_trivial symmetric braiding which is $-1$ on two odd graded vector spaces: in this case the above is the **supertrace** on supervectorspaces, $str(V) = tr(V_{even}) - tr(V_odd)$.


* $C = Span(Top^{op})$: here the trace is the [[co-span co-trace]] which can be seen as describing the gluing of in/out boundaries of [[cobordism]]s 
 
* $C = Span(Grpd)$: this reproduces the notion of trace of a linear map within the interpretation of spans of groupoids as linear maps in the context of [[groupoidification]] and [[geometric function theory]], made explicit at [[span trace]]

#References#

* Joyal, Street, and Verity, _Traced Monoidal Categories_  

* Dold, Albrecht and Puppe, Dieter, _Duality, trace, and transfer_


See also section 5 of

Peter Selinger, _A survey of graphical languages for monoidal categories_ ([pdf](http://www.mathstat.dal.ca/~selinger/papers/graphical.pdf))