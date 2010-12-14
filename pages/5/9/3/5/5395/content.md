
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* the following line creates the automatic table of contents
{: toc}


## Statement ##

+-- {: .un_theorem}
###### Theorem
**(The adjoint lifting theorm)**. Consider the following [[commutative diagram|commutative square]] of [[functor]]s:
$$
\begin{array}{cccc}\mathcal{A} & \overset{Q}{\to}  & \mathcal{B}    \\
^{U}\downarrow     &                   & \downarrow^{V} \\
\mathcal{C}        & \underset{R}{\to} & \mathcal{D}
\end{array}
$$

and suppose that
 
* $U$ and $V$ are [[monadic functor|monadic]], and 

* $\mathcal{A}$ has [[coequalizer]]s of reflexive pairs.

Then, if $R$ has a [[left adjoint]], then $Q$ also has a [[left adjoint]]. 
=--

A detailed proof may be found in Sec. 4.5 of Vol. 2 of [Borceux](#Borceux)
(see especially Theorem 4.5.6 on p. 226 and Ex. 4.8.6 on p. 252).  

+-- {: .un_cor}
###### Corollary
If the bottom functor $R$ of the above square is the
identity arrow (so that $U=V\circ Q$), if $U$ and $V$ are monadic, and
if $\mathcal{A}$ has coequalizers of reflexive pairs, then $Q$ is monadic.
=--

+-- {: .proof}
###### Proof
The adjoint lifting theorem implies the existence of a left
adjoint, and the rest is a straightforward application of the
[[monadicity theorem]].
=--

## Examples ##

### Forgetful functors between varieties of algebras ###
Since varieties of algebras are [[cocompleteness of varieties of algebras|cocomplete]] and monadic over
$\mathbf{Set}$, the corollary implies that forgetful functors between
varieties of algebras (e.g., the forgetful functor
$\mathbf{Rng}\to\mathbf{Ab}$) are monadic.   

### Sufficient conditions for cocompleteness of monadic categories ###
Let $\mathcal{J}$ be an arbitrary category, and consider the commutative diagram 
$$
\begin{array}{ccccc}\mathcal{A} & \overset{\Delta}{\to} & \mathcal{A}^\mathcal{J}    \\
^{U}\downarrow                 &                        & \downarrow^{U^{\mathcal{J}}} \\
\mathcal{C}                    & \underset{\Delta}{\to} & \mathcal{C}^\mathcal{J}
\end{array}
$$
where $U$ is monadic, $\Delta$ is the [[diagonal functor]] and $U^{\mathcal{J}}=U\circ
-$. If $F$ is left adjoint   
to $U$, then $F^\mathcal{J}$ is left adjoint to $U^{\mathcal{J}}$ (using
the unit and counit of the original adjunction, one can construct
appropriate natural transformations that satisfy the triangular
identities, see, e.g., p. 119 of [[Categories Work]]).  Also, the
conditions of the monadicity theorem for $U$ imply those for
$U^\mathcal{J}$ (basically because the definition of a split fork involves only
compositions and identities, and because natural transformations are composed
componentwise).  

Now, if $\mathcal{C}$ is $\mathcal{J}$-cocomplete (so that the
bottom horizontal functor has a left adjoint) and $\mathcal{A}$ has
coequalizers of reflexive pairs, then the adjoint lifting theorem
implies that $\mathcal{A}$ is $\mathcal{J}$-cocomplete. In particular,
if $\mathcal{A}$ has coequalizers of reflexive pairs and $\mathcal{C}$
is small-cocomplete, then $\mathcal{A}$ is small cocomplete.

## References ##
Section 4.5 of volume 2 of 

* [[Francis Borceux]], _Handbook of categorical algebra_ , in 3 vols. 
{#Borceux}