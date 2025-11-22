
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


\tableofcontents


## Idea

Given an [[endomorphism]] $f\colon A\to A$ in a [[traced monoidal category]] $\mathscr{C}$ there is a natural notion of its _trace_ $\tr(f) \colon 1\to 1$, where $1$ denotes the [[tensor unit]]. 

When $\mathscr{C}$ is a $\mathbb{C}$-linear category for which the tensor unit (e.g. a [[fusion category]]), we can canonically identity $\tr(f)$ with a [[complex number]]. 

That is, the trace of $f$ is the unique [[scalar]] $\lambda \in End(1)$ such that

$$
  \tr(f)
    \,=\,
  \lambda 
    \cdot 
   \text{id}_1 
  \mathrlap{\,.}
$$


In the case that $f$ is a [[linear map|linear]] [[endomorphism]] of a [[finite number| finite]] [[dimension | dimensional vector space]], this recovers the usual notion of trace from [[linear algebra]].

## Definition


The idea of the trace operation is easily seen in [[string diagram]] notation: essentially one takes an endomorphism 
$f: A\xrightarrow{}A$, and "closes the loop".

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
     \downarrow^{\mathrlap{Id_{a^*}}} && \;\;\downarrow^f
     \\
     a^* &\otimes& a
     \\
     & \downarrow^{\mathrlap{b_{a^*, a}}} 
     \\
     a &\otimes& a^*
     \\
     & \downarrow
     \\
     & 1     
  }
$$

This definition makes sense in any [[braided monoidal category]], but often in non-symmetric cases one wants instead a slightly modified version which requires the extra structure of a [[balanced monoidal category|balancing]].

The trace of the identity $1_a:a \to a$ is called the **[[dimension]]** or [[Euler characteristic]] of $a$.


## Examples

* [[Vect|$C = Vect_k$]] with its standard monoidal structure ([[tensor product of vector spaces]]): in this case $tr(f)$ is the usual trace of a linear map. Indeed, suppose $f$ is an [[endomorphism]] on a [[finite dimensional vector space|finite dimensional $k$-vector space]] $V$. Then, the trace $tr(f) \colon k\to k$ is given by the following composition.
\[k\xrightarrow{\eta} V\otimes V^\ast\xrightarrow{f\otimes id}V\otimes V^\ast\xrightarrow{\varepsilon} k\]
Here $\varepsilon$ is the standard [[evaluation]]-pairing. The map $\eta$ is obtained from the [[dual linear map]] of $\varepsilon$ by applying the following isomorphisms, see ([Dold & Puppe 1978](#DoldPuppe1978)).
\[k\cong k^\ast,\qquad (V\otimes V^\ast)^\ast\cong(V^\ast)^\ast\otimes V^\ast\cong V\otimes V^\ast\]
One can then compute that
\[\eta(\lambda)=\sum_{i=1}^n\lambda (e_i\otimes e_i^\ast),\]
where $\{e_1,\ldots,e_n\}$ is a [[linear basis]] of $V$ and $\{e_1^\ast,\ldots,e_n^\ast\}$ is the [dual basis](dual+vector+space#dual_bases). Now, if $f$ is given in this basis by a matrix $(a_ij)$, then
\[(f\otimes id)(\eta(\lambda))=\lambda\sum\begin{pmatrix}a_{1i}\\\vdots\\a_{ni}\end{pmatrix}\otimes e_i^\ast.\]
Finally, $(tr(f))(\lambda)$ is obtained by applying the pairing on this tensor: $(tr(f))(\lambda)=\lambda\sum a_{ii}$.

* $C = SuperVect = (Vect_{\mathbb{Z}_2}, \otimes, b)$, the category of $\mathbb{Z}_2$-graded vector spaces with the _non_trivial symmetric braiding which is $-1$ on two odd graded vector spaces: in this case the above is the **[[supertrace]]** on supervectorspaces, $str(V) = tr(V_{even}) - tr(V_odd)$.


* $C = Span(Top^{op})$: here the trace is the [[co-span co-trace]] which can be seen as describing the gluing of in/out boundaries of [[cobordism|cobordisms]].
 
* $C = Span(Grpd)$: this reproduces the notion of trace of a linear map within the interpretation of spans of groupoids as linear maps in the context of [[groupoidification]] and [[geometric function theory]], made explicit at [[span trace]].

* In the [[symmetric monoidal (infinity,1)-category of spectra]], the trace on the identity on a [[suspension spectrum]] of a [[manifold]] $X$ is the [[Euler characteristic]] of $X$ (see there).

## Generalizations

### Vertical categorification

See [[trace of a category]].

### Horizontal categorification

See [[trace in a bicategory]].

### Partial trace

Let $V \in C$ be a dualizable object, and $W$ any object. From an endomorphism $f$ of $V \otimes W$, one can produce an endomorphism $tr_V(f)$ of $W$, by applying the duality data of $V$. In terms of string diagrams, this is "bending along" the strand representing $V$.

+--{: .query}
TO DO: Draw the diagram just described.
=--

#### Matrix representation

Suppose $V$, $W$ are finite-dimensional vector spaces over a field, with dimensions $m$ and $n$, respectively. For any space $A$ let $L(A)$ denote the space of linear operators on $A$. The __partial trace__ over $W$, Tr$_{W}$, is a mapping

$$
  T \in L(V \otimes W) \mapsto Tr_{W}(T) \in L(V).
$$

+-- {: .un_defn}
###### Definition
Let $e_{1}, \ldots, e_{m}$ and $f_{1}, \ldots, f_{n}$ be bases for $V$ and $W$ respectively.  Then $T$ has a matrix representation $\{a_{k l,i j}\}$ where $1 \le k,i \le m$ and $1 \le l,j \le n$ relative to the basis of the space $V \otimes W$ given by $e_{k} \otimes f_{l}$.  Consider the sum

$$
  b_{k,i} = \sum_{j=1}^{n}a_{k j,i j}
$$

for $k,i$ over $1, \ldots, m$.  This gives the matrix $b_{k,i}$.  The associated linear operator on $V$ is independent of the choice of bases and is defined as the partial trace.
=--

#### Example

Consider a quantum system, $\rho$, in the presence of an environment, $\rho_{env}$.  Consider what is known in [[quantum information theory]] as the CNOT gate:

$$
  U={|00\rangle}{\langle 00|} + {|01\rangle}{\langle 01|} + {|11\rangle}{\langle 10|} + {|10\rangle}{\langle 11|}.
$$

Suppose our system has the simple state ${|1\rangle}{\langle 1|}$ and the environment has the simple state ${|0\rangle}{\langle 0|}$.  Then $\rho \otimes \rho_{env} = {|10\rangle}{\langle 10|}$.  In the quantum operation formalism we have

$$
  T(\rho) = \frac{1}{2}Tr_{env}U(\rho \otimes \rho_{env})U^{\dagger}
          = \frac{1}{2}Tr_{env}({|10\rangle}{\langle 10|} + {|11\rangle}{\langle 11|})
          = \frac{{|1\rangle}{\langle 1|}{\langle 0|0\rangle} + {|1\rangle}{\langle 1|}{\langle 1|1\rangle}}{2}
          = {|1\rangle}{\langle 1|}
$$

where we inserted the normalization factor $\frac{1}{2}$.

## Related concepts

* [[relation between trace and determinant]]

* [[traced monoidal category]]

* [[Euler characteristic]]

* [[bicategorical trace]], 
 
  * [[Reidemeister trace]]

* [[higher trace]]

* [[Dennis trace]], [[cyclotomic trace]]

* [[trace of horizontal to round chord diagrams]]



## References

The categorical notion of trace in a monoidal category is due to

* {#DoldPuppe1978} [[Albrecht Dold]],  and [[Dieter Puppe]], _Duality, trace, and transfer_ In Proceedings of the Inter-
national Conference on Geometric Topology (Warsaw, 1978), pages 81{102, Warsaw, 1980.
PWN.

and

* [[Max Kelly]] M. L. Laplaza, _Coherence for compact closed categories_  J. Pure Appl. Algebra, 19:193{213, 1980.

Surveys include

* [[Peter Selinger]], _A survey of graphical languages for monoidal categories_ ([pdf](http://www.mathstat.dal.ca/~selinger/papers/graphical.pdf)), Section 5


* [[Kate Ponto]], [[Mike Shulman]], _Traces in symmetric monoidal categories_ ([pdf](http://arxiv.org/pdf/1107.6032v1.pdf)).

Generalization of this to [[indexed monoidal categories]] is in 

* [[Kate Ponto]], [[Mike Shulman]], _Duality and traces for indexed monoidal categories_, Theory and Applications of Categories, Vol. 26, 2012, No. 23, pp 582-659 ([arXiv:1211.1555](http://arxiv.org/abs/1211.1555))

and to [[bicategories]] in 

* [[Kate Ponto]], [[Mike Shulman]], _Shadows and traces in bicategories_, JHRS, ([arXiv:0910.1306](https://arxiv.org/abs/0910.1306))

Further developments are in

* [[Andre Joyal]], [[Ross Street]], and [[Dominic Verity]], _Traced Monoidal Categories_  

* [[David Ben-Zvi]], [[David Nadler]], _Nonlinear traces_ ([arXiv:1305.7175](http://arxiv.org/abs/1305.7175))
 {#BenZviNadler13}

For the notion of partial trace, particularly its application to [[quantum mechanics]], see:

* Nielsen and Chuang, _Quantum Computation and Quantum Information_


[[!redirects traces]]

[[!redirects partial trace]]
[[!redirects partial traces]]
