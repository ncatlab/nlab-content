<div class="rightHandSide toc">
[[!include cohomology - contents]]
***
[[!include infinity-Lie theory - contents]]
</div>




#Contents#
* automatic table of contents
{:toc}


## Idea

While abelian [[Lie algebra cohomology]] is obtained from the study of [[Chevalley-Eilenberg complex]], some nonabelian generalizations are known in low dimensions. The coefficients are not now in a Lie algebra module (which is viewed here as an abelian Lie algebra with action of another Lie algebra), but an arbitrary Lie algebra with something that is action of another Lie algebra up to an inner automorphism. 

For example the problem of extensions of Lie algebras by nonabelian Lie algebras leads to 1,2,3 nonabelian cocycles; 2-cocycles are analogues of [[group extension|factor systems]].

Below, in the section [Abstract definition](#AbstractDefinition) we discuss how a nonabelian Lie algebra cocylce is a morphism

$$
  (\psi,\chi) : \mathfrak{g} \to Der(\mathfrak{k})
$$

of [[L-∞-algebra]]s to the [[strict Lie 2-algebra]] of derivations of $\mathfrak{k}$.

## Nonabelian 2-cocycles

Let $F$ be a field. **Lie algebra factor system** (or a **nonabelian 2-cocycle**) on a $F$-Lie algebra $\mathfrak{b}$ with coefficients in $F$-Lie algebra $\mathfrak{k}$ is a pair $(\chi,\psi)$ where $\chi: \mathfrak{b}\wedge \mathfrak{b}\to\mathfrak{k}$ and $\psi:\mathfrak{b}\to Der(\mathfrak{k})$ are $F$-linear maps satisfying

$$
  \begin{aligned}
& \chi([b_1,b_2]\wedge b_3)-\chi(b_1\wedge [b_2,b_3])+\chi(b_2\wedge[b_1,b_3])
\\& = \psi(b_3)(\chi(b_1\wedge b_2))-\psi(b_1)(\chi(b_2\wedge b_3))+\psi(b_2)(\chi(b_1\wedge b_3))
\end{aligned}
$$

for all $b_1,b_2,b_3\in B$ and

$$
[\psi(a),\psi(b)]=\psi([a,b])+ad_{\mathfrak{k}}(\chi(a\wedge b))
$$

where $a,b\in B$ and $ad_{\mathfrak{k}}:\mathfrak{k}\to Int(\mathfrak{k})$ is the canonical map into inner automorphisms $k\mapsto [k,]$. 

## Schreier's theory for Lie algebras

[[Otto Schreier]] (1926) and Eilenberg-Mac Lane (late 1940-s) developed a theory of nonabelian [[group extension|extensions of abstract groups]] leading to the low dimensional nonabelian group cohomology. For Lie algebras, the theory can be developed in the same manner. One tries to classify [[Lie algebra extension|extensions of Lie algebras]]

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

(ii) $k\mapsto (0,k)$ defines an embedding $i:\mathfrak{k}\to\mathfrak{g}$ of Lie algebras and $(b,k)\mapsto b$ is a surjective homomorphism of Lie algebra $p:\mathfrak{g}\to\mathfrak{b}$ whose kernel is the Lie ideal $i(\mathfrak{k})=0\oplus\mathfrak{k}\subset\mathfrak{g}$. This way $0\to\mathfrak{k}\overset{i}\to\mathfrak{g}\overset{p}\to\mathfrak{b}\to 0$ is an extension of the base Lie algebra $\mathfrak{b}$ by the kernel Lie algebra $\mathfrak{k}$. 

(iii) If the 2-cocycle is obtained from a Lie algebra extension $0\to \mathfrak{k}\overset{i_0}\to \mathfrak{g}_0\overset{p_0}\to\mathfrak{b}\to 0$ and an arbitrary $F$-linear section $\sigma_0$ of $p_0$, then the map $can_\sigma:\mathfrak{g}_0\to\mathfrak{g}$ given by $g\mapsto (p(g),-\sigma(p(g))+g)$ is well-defined and a Lie algebra isomorphism such that $can_\sigma\circ i_0=i$, $p_0=p\circ can_\sigma$, hence the two extensions are isomorphic. 

In addition to the problem of extensions, nonabelian 2-cocycles appear in a more general problem of liftings of Lie algebras. 

## Abstract definition {#AbstractDefinition}

We claim that the above definition of nonabelian Lie algebra cocycles may be understood naturally in terms of the general notion of [[cohomology]] and in particular is the image of the story of [[nonabelian group cohomology]] under Lie differentiation:

+-- {: .standout}

The following observation is not in the literature.

=--



+-- {: .un_prop}
###### Proposition

Let $\infty Lie$ be the [[(∞,1)-category]] of [[L-∞-algebra]]s.
Let $\mathfrak{g}, \mathfrak{k}$ be [[Lie algebra]]s. Then the
degree 2 nonabelian Lie algebra cohomology of $\mathfrak{g}$ with coefficients
in $\mathfrak{k}$ is 

$$
  H^2_{nonab}(\mathfrak{g}, \mathfrak{k})
  \simeq
  \pi_0 \infty Lie(\mathfrak{g}, Der(\mathfrak{k}))
  \,,
$$

where $Der(\mathfrak{k})$ is the [[strict Lie 2-algebra]] of derivations
on $\mathfrak{k}$.

More in detail:

* nonabelian degree 2 Lie algebra cocycles $(\psi,\xi)$ are in natural bijections with
  morphisms

  $$
    \mathfrak{g} \to Der(\mathfrak{k})
  $$

* coboundaries $\eta$ between cocycles $(\psi_1,\xi_1)$ and $(\psi_2,\xi_2)$
  correspond to homotopies between these

  $$
    \array{
      & \nearrow\searrow^{\mathrlap{(\psi_1,\chi_1)}}
      \\
      \mathfrak{g}
      &\Downarrow^{\eta}&
      Der(\mathfrak{k})
      \\
      & \searrow\nearrow^{\mathrlap{(\psi_2,\chi_2)}}
    }
  $$

  and this correspondence is precise if we take the homotopy to be
  induced from the "standard [[cylinder object]]", described below.

=--

+-- {: .proof}
###### Proof

Checking this is a straightforward matter of unwinding the definitions
of morphisms of $L_\infty$-algebras.

Which is what we indicate.

We model $\infty Lie$ as usual a subcategory of [[dg-algebra]]s of
[[semifree dga]]s, by representing each $L_\infty$-algebra $\mathfrak{g}$
by its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$.

For the [[Lie algebra]] $\mathfrak{g}$ itself with Lie bracket
$[-,-] : \mathfrak{g} \wedge \mathfrak{g} \to \mathfrak{g}$ this is the
[[semifree dga]]

$$
  CE(\mathfrak{g}) =
  (\wedge^\bullet \mathfrak{g}^* , \; d = [-,-]^* )
  \,,
$$

where the differential is on generators the dual of the Lie bracket,
$[-,-]^* : \mathfrak{g}^* \to \mathfrak{g}^* \wedge \mathfrak{g}^* $
extended as a graded derivation to all of $\wedge^\bullet \mathfrak{g}^*$.

For any [[strict Lie 2-algebra]] coming from a [[differential crossed module]]
$(\mathfrak{h}_1 \stackrel{\delta}{\to} \mathfrak{h}_1)$ with action
$\rho : \mathfrak{h}_1 \to der(\mathfrak{h}_2)$ -- that we think of
in the following as equivalently a linear map
$\rho : \mathfrak{h}_1 \otimes \mathfrak{h}_2 \to \mathfrak{h}_2$ --
the [[Chevalley-Eilenberg algebra]] is

$$
  CE(\mathfrak{h}_2 \stackrel{\delta}{\to} \mathfrak{h}_1)
  =
  \left(
    \wedge^\bullet ( \mathfrak{h}_1^* \oplus \mathfrak{h}_2^* )
    ,
    \;
    d_{\delta}
  \right)
$$

with $\mathfrak{h}_1^*$ in degree 1 and $\mathfrak{h}_2^*$ in degree 2, and with the
differential given on degree 1 generators by

$$
  d_\delta |_{\mathfrak{h}_1^*} = [-,-]_{\mathfrak{h}_1}^* + \delta^*
  : \mathfrak{h}_1^* \to 
    \mathfrak{h}_1^* \wedge \mathfrak{h}_1^*
    \oplus
    \mathfrak{h}_2^*
$$

and on degree 2 generators by

$$
  d_\delta |_{\mathfrak{h}_2^*} = \rho^*
  : 
  \mathfrak{h}_2^* \to \mathfrak{h}_1^* \otimes \mathfrak{h}_2^*
  \,.
$$

The case of the derivation [[strict Lie 2-algebra]] of a Lie algebra
$\mathfrak{k}$ is the special case of this for

$$
  Der(\mathfrak{k}) = (\mathfrak{k} \stackrel{ad}{\to} der(\mathfrak{k}))
  \,.
$$

Now a morphism

$$
  (\psi, \chi) : \mathfrak{g} \to Der(\mathfrak{k})
$$

of $\infty$-Lie algebras is given by a morphism

$$
  CE(\mathfrak{g}) \leftarrow CE(Der(\mathfrak{k})) :
  (\psi^*, \chi^*)
$$

of [[dg-algebra]]s.

Morphisms of [[dg-algebra]]s are given by morphisms of the underlying
graded algebras, subject to the respect for the differentials. Morphisms
of the underlying graded [[Grassmann algebra]]s are given by
grading preserving linear maps on the spaces of generators.

So the underlying maps

$$
  \wedge^\bullet \mathfrak{g}^*
   \leftarrow
  \wedge^\bullet (\mathfrak{h}_1^* \oplus \mathfrak{h}_2^*)
  :
  (\psi^* , \chi^*)
$$

come from linear maps

$$
  \mathfrak{g}^* \leftarrow \mathfrak{h}_1^* : \psi^*
$$

and

$$
  \mathfrak{g}^* \wedge \mathfrak{g}^* \leftarrow \mathfrak{h}_2^* : \chi^*
$$

i.e. form linear maps

$$
  \psi : \mathfrak{g} \to der(\mathfrak{k})
$$

and

$$
  \chi : \mathfrak{g} \wedge \mathfrak{g} \to \mathfrak{k}
  \,.
$$

This is the underlying data of the nonabelian 2-cocycle. Now the
respect for the differentials on the Chevalley-Eilenberg algebras will
give the cocycle condition:

let $\omega \in \mathfrak{h}_2^* \subset CE(\mathfrak{h}_1 \to \mathfrak{h}_2)$
be any degree 2 element, then respect for the differential implies that


$$
  \array{
    \omega(\chi([-,-],-))
    =
    \omega(\rho(\psi(-)(\chi(-,-))))
    &\stackrel{(\psi^*, \chi^*)}{\leftarrow}& \omega(\rho(-)(-)))
    \\
    \uparrow^{d_\mathfrak{g} = [-,-]^*} && \uparrow^{\mathrlap{d_{\delta}}}
    \\
    \omega(\xi(-,-))
    &\stackrel{(\psi^*, \chi^*)}{\leftarrow}&
    \omega
  }
  \,.
$$

Since this has to hold for all $\omega$, we get the first part of the cocycle condition:

$$
  \chi([-,-],-) = \rho(\psi(-)\chi(-,-))
$$

(both sides here regarded as elements of a graded Grassmann algebra as indicated above,
so with all antisymmetrization on the arguments implicit).

Similarly, for $\lambda \in \mathfrak{h}_1^* \subset CE(\mathfrak{h}_1 \to \mathfrak{h}_2)$
be any degree 1 element, then respect for the differential implies that

$$
  \array{
     \lambda(\psi([-,-]))
     =
     \lambda([\psi(-), \psi(-)])
     +
     \lambda(ad(\chi(-,-)))
     &\stackrel{}{\leftarrow}&  \lambda([-,-]_{\mathfrak{h}_1}) + \lambda(ad(-))
     \\
     \uparrow && \uparrow
    \\
    \lambda(\psi(-))
    &\stackrel{(\psi^* , \chi^*)}{\leftarrow}&
    \lambda
  }
  \,.
$$

Again, this has to hold for all $\lambda$, so we have the auxiliary condition on the
cocycle

$$
  \psi([-,-])
  =
  [\psi(-),\psi(-)]
  +
  ad(\xi(-,-))
  \,.
$$

This shows that morphisms $\mathfrak{g} \to Der(\mathfrak{k})$ are
in bijection to the nonabelian coccles.

It remains to show that the homotopies map to coboundaries. For that
we may take in $\infty Lie$ the standard [[cylinder object]] of some
$\mathfrak{CE}(\mathfrak{g})$ to be

$$
  CE(\mathfrak{g})\otimes CE(\mathfrak{g})
  \leftarrow
  C^\bullet(\Delta^1)\otimes CE(\mathfrak{g})
  \leftarrow
  CE(\mathfrak{g})
  \,,
$$

where $C^\bullet(\Delta^1)$ is the [[semifree dga]] of cochains on the
cellular 1-[[simplex]], i.e.

$$
  C^\bullet(\Delta^1) =
  (\wedge^\bullet (\langle a,b \rangle \oplus \langle c \rangle)
  , d a = - d b = d c
  )
  \,,
$$

with $a,b$ generators in degree 0 and $c$ in degree 1. Using this,
write out the data implied by a morphism $\eta$ that is a [[left homotopy]]

$$
  \array{
    CE(\mathfrak{g})
    \\
    \downarrow & \nwarrow^{\mathrlap{(\psi_1^*, \chi_1^*)}}
    \\
    C^\bullet(\Delta^1)\otimes CE(\mathfrak{g})
    &\stackrel{\eta}{\leftarrow}&
    CE(Der(\mathfrak{k}))
    \\
    \uparrow & \swarrow_{\mathrlap{(\psi_2^*, \chi_2^*)}}
    \\
    CE(\mathfrak{g})
  }
$$

along the above lines.

=--

+-- {: .query}

There is a slight gap here, concerning the fact that $CE(Der(\mathfrak{k}))$ may not be a Sullivan algebra, and hence not cofibrant in the [[model structure on dg-algebras]]: while it is of course a [[semifree dga]], it need not satisfy that addition nilpotency condition. I'll try to think what to do about that... -[[Urs Schreiber|Urs]]

=--



## References

* G. Hochschild, _Lie algebra kernels and cohomology_, Amer. J. Math. __76__, n.3 (1954) 698--716.

The notation above is from personal notes of Z. &#352;koda (1997). A systematic theory has been many times partly rediscovered from soon after the Eilenberg-MacLane work on group extension, among first by Hochschild and then by many others till nowdays. Here is a recent online account emphasising parallels with differential geometry:

*  Dmitri Alekseevsky, Peter W. Michor, Wolfgang Ruppert, Extensions of Lie algebras
[math.DG/0005042](http://arxiv.org/abs/math/0005042)

More conceptual picture is in a work of Danny Stevenson which extends also to its categorification, extensions of Lie 2-algebras. See

* Danny Stevenson, Lie 2-algebras and the geometry of gerbes, Unni Namboodiri Lectures 2006 [slides](http://math.ucr.edu/home/baez/namboodiri/stevenson_maclane.pdf)

A generalization is [[nonabelian Lie algebroid cohomology]].