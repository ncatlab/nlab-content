
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition ##

+--{: .num_defn}
###### Definition
A 2-category is **Heyting** if it is [[coherent 2-category|coherent]]  and each pullback functor $f^*:Sub(Y)\to Sub(X)$ has a right adjoint $\forall_f$.
=--

As in the 1-categorical case, this also ensures that each $Sub(X)$ is a Heyting algebra and that each $f^*$ is a homomorphism of Heyting algebras.  Moreover, the right adjoints $\forall_f$ satisfy the [[Beck-Chevalley condition|Beck-Chevalley condition]] for pullback squares, because the left adjoints $\exists_f$ do.  This is just what is necessary for the [[michaelshulman:2-internal logic|internal]] interpretation of (finitary) first-order logic.


## Examples ##

* $Cat$ is Heyting.

* A 1-category is Heyting as a 2-category iff it is [[Heyting category|Heyting]] as a 1-category.

* A (0,1)-category is Heyting iff it is a [[Heyting algebra|Heyting algebra]].

* Any well-powered infinitary-coherent 2-category is Heyting, by the adjoint functor theorem for posets.  In particular, any [[michaelshulman:Grothendieck 2-topos]] is Heyting.

* Unlike in the 1-categorical case, there seems no reason why a coherent 2-category with [[michaelshulman:exponentials in a 2-category|exponentials]] must be Heyting.  It does, however have adjoints to pullback along fibrations and opfibrations, and in particular along product projections, which is enough for some uses of universal quantification in the internal logic.


## Preservation

Clearly if $K$ is Heyting, so are $K^{co}$, $gpd(K)$, $pos(K)$, $disc(K)$, and $Sub(1)$ (the Heyting algebra of subterminals).

Moreover, Heytingness is also preserved by [[michaelshulman:fibrational slice|fibrational slicing]].  First we show:

+--{: .num_theorem}
###### Theorem
If $K$ is Heyting, then for any $X$ and any $A\in Opf(X)$, $Sub_{Opf(X)}(A)$ is a coreflective sub-poset of $Sub_K(A)$.
=--
+--{: .proof}
###### Proof
As proven [[michaelshulman:fibrational slice|here]], $Sub_{Opf(X)}(A)$ is a full sub-poset of $Sub_K(A)$.  Moreover, it is easy to see that a ff $B\to A$ is in $Sub_{Opf(X)}(A)$ precisely when

1. $B\to X$ is an opfibration and
1. $B\to A$ is a morphism of opfibrations.

In general, the first condition does _not_ imply the second.  It is also easy to check that these two conditions together are equivalent to saying that the composite
$$B\times_X X ^{\mathbf{2}} \to A\times_X X ^{\mathbf{2}} \overset{a}{\to} A$$
factors through $B\to A$, where $a$ is the action making $A$ into a fibration.  Note that $B\times_X X ^{\mathbf{2}} $ is alternately written as $p^*B$, where $p:A\times_X X ^{\mathbf{2}} \to A$ is the projection onto the first factor.  Therefore, $B$ is in $Sub_{Opf(X)}(A)$ just when $\exists_p a^*B\le B$, or equivalently when $B\le \forall_a p^*B$.

We claim that $B\mapsto \forall_a p^* B$ coreflects $Sub(A)$ into $Sub_{Opf(X)}(A)$, and given the above, it suffices to verify that it is a comonad.  First, let $i:A\to A\times_X X ^{\mathbf{2}}$ be the inclusion of identities; then $a i\cong 1$ and $p i \cong 1$, so we have
$$
\begin{aligned}
  i^*a^*B =& B\\
  a^*B \le& \forall_i B\\
  \forall_p a^* B \le& \forall_p \forall_i B = B.
\end{aligned}
$$
This gives the counit of the comonad.  The comultiplication is a little more involved.  First note that we have a pullback square
$$\array{
  A\times_X X ^{\mathbf{2}} \times_X X ^{\mathbf{2}} &   \overset{q}{\to} & A\times_X X ^{\mathbf{2}} \\
  ^{a\times 1}\downarrow && \downarrow^a\\
  A\times_X X ^{\mathbf{2}}  & \underset{p}{\to} & A}$$
where $q$ denotes projection onto the first two factors.  Thus, by the Beck-Chevalley condition, $a^*\forall_p = \forall_q (a\times 1)^*$ and therefore
$$\forall_p a^*\forall_p a^* B =
\forall_p \forall_q (a\times 1)^* a^* B = 
\forall_p \forall_q (1\times m)^* a^* B
$$
where $m:X ^{\mathbf{2}} \times_X X ^{\mathbf{2}} \to X^{\mathbf{2}} $ is the "composition" morphism.

Let us write $X^{\to\to}$ for $X ^{\mathbf{2}} \times_X X ^{\mathbf{2}}$, the object of composable arrows in $X$, and write $X^{\overset{\nearrow}{\to}\to}$ for the power of $X$ with the category
$$\array{&& \bullet\\ & \nearrow\\ \bullet &\to & \bullet & \to &\bullet}$$
Let $r:X^{\overset{\nearrow}{\to}\to} \to X^{\to\to}$ forget the "lonely" arrow, and let $c:X^{\to\to} \to X^{\overset{\nearrow}{\to}\to}$ make the lonely arrow into the composite of the other two.  Then $r c \cong 1$, and moreover $p' q' c\cong 1\times m$, where $p'$ and $q'$ are $p$ and $q$  applied to the non-lonely arrows.  Thus, we have
$$\begin{aligned}
  c^* (q')^* (p')^* a^* B =& (1\times m)^* a^* B\\
  (q')^* (p')^* a^* B \le& \forall_c (1\times m)^* a^* B\\
  \forall_r (q')^* (p')^* a^* B \le& \forall_r \forall_c (1\times     m)^* a^* B\\
  \forall_r (q')^* (p')^* a^* B \le& (1\times m)^* a^* B\\
  q^* p^* \forall_p a^* B \le& (1\times m)^* a^* B\\
  \forall_p a^* B \le& \forall_p \forall_q (1\times m)^* a^* B\\
  \forall_p a^* B \le& \forall_p a^*\forall_p a^* B.
\end{aligned}$$
as desired.  (Here we have used another Beck-Chevalley condition to move $r$ past $q'$ and $p'$, turning them into $p$ and $q$ and it into $p$.)
=--


+--{: .num_cor}
###### Corollary
If $K$ is Heyting, so is each [[fibrational slice]] $Opf(X)$ and $Fib(X)$.
=--
+--{: .proof}
###### Proof
This follows from the adjoint lifting theorem for posets: for any $f:A\to B$ in $Opf(X)$ we have a commutative square
$$\array{Sub_{Opf(X)}(B) & \overset{f^*}{\to} & Sub_{Opf(X)}(A)\\
  \downarrow && \downarrow\\
  Sub_K(B)& \underset{f^*}{\to} & Sub_K(A)}$$
where the vertical arrows are comonadic (inclusions of coreflective sub-posets) and the bottom horizontal arrow has a right adjoint; hence so does the top horizontal arrow.
=--


## Booleanness

We may naturally say that a coherent 2-category $K$ is **Boolean** if each $Sub(X)$ is a Boolean algebra.  As usual, this implies that $K$ is Heyting; we have $\forall_f = \neg \exists_f \neg$.

Note that a subobject and its complement in $Sub(X)$ need _not_ be "disjoint" in the sense introduced [[coherent 2-category|here]]; only their pullback, not their comma object, need be initial.  Note also that unlike in the 1-categorical case, Booleanness is _not_ stable under slicing; this fails already in the (1,2)-category $Pos$ (though it holds in any (2,1)-category).

## References

The above definitions and observations are originally due to

* [[Michael Shulman]], _[[michaelshulman:Heyting 2-category]]_ 

[[!redirects Heyting 2-categories]]

[[!redirects Heyting (2,1)-category]]
[[!redirects Heyting (2,1)-categories]]
