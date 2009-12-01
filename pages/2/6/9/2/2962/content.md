#Idea

While abelian Lie algebra cohomology is obtained from the study of Chevalley-Eilenberg complex, some nonabelian generalizations are known in low dimensions. The coefficients are not now in a Lie algebra module (which is viewed here as an abelian Lie algebra with action of another Lie algebra), but an arbitrary Lie algebra with something what is action of another Lie algebra up to an inner automorphism. 

For example the problem of extensions of Lie algebras by nonabelian Lie algebras leads to 1,2,3 nonabelian cocycles; 2-cocycles are analogues of factor systems.

#Nonabelian 2-cocycles

Let $F$ be a field. **Lie algebra factor system** (or a **nonabelian 2-cocycle**) on a $F$-Lie algebra $\mathfrak{b}$ with coefficients in $F$-Lie algebra $k$ is a pair $(\chi,\psi)$ where $\chi: \mathfrak{b}\wedge \mathfrak{b}\to\mathfrak{k}$ and $\psi:\mathfrak{b}\to Der(\mathfrak{k})$ are $F$-linear maps satisfying

$$
\chi([b_1,b_2]\wedge b_3)-\chi(b_1\wedge [b_2,b_3])+\chi(b_2\wedge[b_1,b_3])=\psi(b_3)(\chi(b_1\wedge b_2))-\psi(b_1)(\chi(b_2\wedge b_3))+\psi(b_2)(\chi(b_1\wedge b_3))
$$

for all $b_1,b_2,b_3\in B$ and

$$
[\psi(a),\psi(b)]=\psi([a,b])+ad_{\mathfrak{k}}(\chi(a\wedge b))
$$

where $a,b\in B$ and $ad_{\mathfrak{k}}:\mathfrak{k}\to Int(\mathfrak{k})$ is the canonical map into inner automorphisms $k\mapsto [k,]$. 

#Schreier's theory for Lie algebras

[[Otto Schreier]] (1926) and Eilenberg-Mac Lane (late 1940-s) developed a theory of nonabelian extensions of abstract groups leading to the low dimensional nonabelian group cohomology. For Lie algebras, the theory can be developed in the same manner. One tries to classify extensions of Lie algebras

$$ 0\to \mathfrak{k}
\overset{i}\to \mathfrak{g}\overset{p}\to\mathfrak{b}\to 0$$

**Theorem.** To every Lie algebra extension as above, and a choice of $F$-linear section $\sigma:\mathfrak{b}\to\mathfrak{g}$ of $p$, one can assign a nonabelian 2-cocycle (factor system) on $\mathfrak{b}$ with values in $\mathfrak{k}$ as follows: set 

$$\chi(b_1\wedge b_2):=-\sigma([b_1,b_2])+[\sigma(b_1),\sigma(b_2)]$$ 

and define $\phi:\mathfrak{g}\to Der(\mathfrak{k})$ by $\phi(g)(k):=[g,k]$. Then set $\psi:=\phi\circ\sigma$. Then $(\chi,\psi)$ is a nonabelian 2-cocycle on $\mathfrak{b}$ with values in $\mathfrak{k}$. 

**Theorem. (cocycle crossed product of Lie algebras)** Let $(\chi,\psi)$ be a factor system as above.
Then define a $F$-linear bracket on the $F$-vector space $\mathfrak{b}\oplus\mathfrak{k}$ by

$$
[(b_1,k_1),(b_2,k_2)] = ([b_1,b_2],\chi(b_1\wedge b_2)+\psi(b_1)(k_2)-\psi(b_2)(k_1)+[k_1,k_2])
$$

Then 

(i) $[,]$ is a antisymmetric and satisfies the Jacobi identity, i.e. $\mathfrak{g}:=(\mathfrak{b}\oplus\mathfrak{k},[,])$ is an $F$-Lie algebra. 

(ii) $b\mapsto (b,0)$ defines an embedding $i:\mathfrak{b}\to\mathfrak{g}$ of Lie algebras and $p:(b,k)\mapsto k$ is a surjective homomorphism of Lie algebra whose kernel is the Lie ideal $i(\mathfrak{b})=\mathfrak{b}\oplus 0\subset\mathfrak{g}$. This way $0\to\mathfrak{k}\overset{i}\to\mathfrak{g}\overset{p}\to\mathfrak{b}\to 0$ is an extension of the base Lie algebra $\mathfrak{b}$ by the kernel Lie algebra $\mathfrak{k}$. 

(iii) If the 2-cocycle is obtained from a Lie algebra extension $0\to \mathfrak{k}\overset{i_0}\to \mathfrak{g}_0\overset{p_0}\to\mathfrak{b}\to 0$ and an arbitrary $F$-linear section $\sigma_0$ of $p_0$, then the map $can_\sigma:\mathfrak{g}_0\to\mathfrak{g}$ given by $g\mapsto (p(g),-\sigma(p(g))+g)$ is well-defined and a Lie algebra isomorphism such that $can_\sigma\circ i_0=i$, $p_0=p\circ can_\sigma$, hence the two extensions are isomorphic. 

In addition to the problem of extensions, nonabelian 2-cocycles appear in a more general problem of liftings of Lie algebras. 

#References

The notation above is from personal notes of Z. &#352;koda (1997). A systematic theory has been many times partly rediscovered from soon after the Eilenberg-MacLane work on group extension till nowdays. Here is a recent online account emphasising parallels with differential geometry:

*  Dmitri Alekseevsky, Peter W. Michor, Wolfgang Ruppert, Extensions of Lie algebras
[math.DG/0005042](http://arxiv.org/abs/math/0005042)

More conceptual picture is in a work of Danny Stevenson which extends also to it scategorification, extensions of Lie 2-algebras. See

* Danny Stevenson, Lie 2-algebras and the geometry of gerbes, Unni Namboodiri Lectures 2006 [slides](http://math.ucr.edu/home/baez/namboodiri/stevenson_maclane.pdf)