
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--



# Pointed derivators
* table of contents
{: toc}

## Idea

A [[derivator]] is *pointed* if it has a [[zero object]] in the sense appropriate to a derivator.

## Definition

A derivator $D\colon Dia^{op} \to Cat$ is **pointed**, or has a **zero object**, if each [[category]] $D(X)$ has a zero object.

Note that these zero objects are automatically preserved by all the [[functors]] $u_!,u^*,u_*$, since they are all [[adjoint functor|adjoints]] on one side or the other.

## Properties

This simple definition hides a lot of structure.

### Relative diagram categories

If $D$ is a pointed derivator and $i\colon A\hookrightarrow B$ is a [[full subcategory]], we write $D(B,A)$ for the full subcategory of $D B$ on those diagrams $X\in D B$ such that $i^*X$ is null.

+-- {: .num_lemma #SieveRel}
###### Lemma
If $i$ is the inclusion of a [[sieve]], then $i_*\colon D(A) \to D(B)$ is [[full and faithful functor|fully faithful]] and its [[essential image]] is $D(B,B\setminus A)$.  Similarly, if $i$ is a cosieve, then $i_!$ identifies $D(A)$ with $D(B,B\setminus A)$.
=--
+-- {: .proof}
###### Proof
Suppose $i$ is a sieve.  Since $i$ is in particular fully faithful, so is $i_*$ by general arguments (see [[homotopy exact square]]).  Moreover, since $i$ is a sieve, the square
$$\array{ \emptyset & \to & A\\
\downarrow & & \downarrow^i\\
B\setminus A & \underset{j}{\to} & B}
$$
is homotopy exact (where $j$ is the inclusion).  Therefore $j^* i_* X$ is terminal for any $X\in D(A)$, so that $i_*$ lands inside $D(B,B\setminus A)$.  Conversely, if $X\in D(B,B\setminus A)$, then the map $X \to i_* i^* X$ is an isomorphism on $A$ (since $i_*$ is fully faithful) and on $B\setminus A$ (since both are terminal there), hence is itself an isomorphism; so $X$ is in the essential image of $i_*$.
=--

The following theorem is stated as Proposition 7.4 of [Heller's paper](#HellerStable) "Stable homotopy theories and stabilization".

+-- {: .num_theorem #RelRefl}
###### Theorem
$D(B,A)$ is a [[reflective subcategory|reflective]] and [[coreflective subcategory|coreflective]] subcategory of $D(B)$.
=--
+-- {: .proof}
Let $M i$ denote the "codirected [[mapping cylinder]]" of $i\colon A \hookrightarrow B$, by which we mean the full subcategory of $B\times I$ on the objects $(x,0)$ for $x\in B$ and $(i(x),1)$ for $x\in A$ (here $I$ is the [[interval category]] $(0\to 1)$).  This is also the same as the [[cocomma object]] $(B \uparrow i)$.  Write $B \overset{u}{\to} M i \overset{p}{\to} B$ for the evident inclusion and projection.

Consider the adjunction
$$ D(M i) \underoverset{p^*}{p_!}{\rightleftarrows} D(B). $$
We claim that this restricts to an adjunction
\[ D(M i,A) \underoverset{p^*}{p_!}{\rightleftarrows} D(B,A) \label{ppadj} \]
where $A$ denotes the subcategory of $M i$ on the objects $(i(x),1)$.  Certainly $p^*$ takes $D(B,A)$ into $D(M i,A)$, since $i\colon A \hookrightarrow B$ is the composite $A \hookrightarrow M i \overset{p}{\to} B$.  On the other hand, the square
$$\array{A & \hookrightarrow & M i \\
\downarrow & & \downarrow^p\\
A & \underset{i}{\to} & B }
$$
is [[homotopy exact square|homotopy exact]], so $p_!$ takes $D(M i,A)$ into $D(B,A)$.

Now since $u$ is the inclusion of a [[sieve]], by the previous lemma, $u_*$ identifies $D(B)$ with $D(M i,A)$.  Therefore, the inclusion $D(B,A)\hookrightarrow D(B)$ can be identified with the restricted right adjoint $p^*\colon D(B,A) \to D(M i,A)$, which therefore has a left adjoint $p_!$.  Explicitly, the left adjoint is $p_! u_*$.

The proof of coreflectivity is of course dual, using the directed mapping cylinder instead of the codirected one.
=--

Note that if $i'\colon A'\hookrightarrow B'$ is another full inclusion and
$$\array{A & \overset{f}{\to} & A'\\
  ^i\downarrow && \downarrow^{i'}\\
  B& \underset{g}{\to} & B'}$$
commutes, then we have a restriction $(g,f)^*\colon D(B',A') \to D(B,A)$, which has a left adjoint $(g,f)_!$ given by the composite
$$ D(B,A) \hookrightarrow D(B) \overset{g_!}{\to} D(B') \overset{L_{B',A'}}{\to} D(B',A') $$
where $L_{B,A}\colon D(B) \to D(B,A)$ denotes the reflection.  It also has a right adjoint defined dually.


### Pointed exactness

Define a **category with zeros** to be a category $B$ equipped with a full subcategory $B_0$.  By the preceding remarks, any pointed derivator gives rise to a contravariant pseudofunctor defined on the 2-category of categories with zeros (and functors preserving the specified subcategories), all of whose transition functors have both adjoints.  It is natural to look for exactness conditions, analogous to (Der4) and the characterization of [[homotopy exact squares]], which apply to these adjoints.

Since the Beck-Chevalley transformation relating composites of these adjoints is the composite of the corresponding transformation for the unpointed diagram and a Beck-Chevalley transformation relating the restriction functors to the reflections $D(B) \to D(B,B_0)$, we clearly need to study when restriction commutes with these reflections.  This is the purpose of the following definition and lemma.


+-- {: .num_defn #LocallyNullFinal}
###### Definition
A functor $f\colon A \to B$ between categories with zeros is **locally null-final** if for every $a\in A$, every $b_0 \in B_0$, and every morphism $\phi\colon b_0 \to f(a)$, the category of triples $(a_0\in A_0, a_0 \xrightarrow{\alpha} a, b_0 \xrightarrow{\beta} f(a_0))$ such that $\phi = f(\alpha).\beta$ has a contractible nerve.
=--

+-- {: .num_lemma #LocallyNullFinalLemma}
###### Lemma
If $f\colon A \to B$ is [locally null-final](#LocallyNullFinal) and $D$ is a pointed derivator, then the functors $f^*\colon D(B) \to D(A)$ and $f^*\colon D(B,B_0) \to D(A,A_0)$ commute with the reflections of $D(B)$ and $D(A)$ into $D(B,B_0)$ and $D(A,A_0)$, respectively.  In other words, the canonical [[natural transformation]]

$$
  \array{ 
    D(A) & \xleftarrow{f^*} & D(B) 
    \\
    ^{L_A}\downarrow & \seArrow & \downarrow^{L_B} 
    \\
    D(A,A_0) & \xleftarrow{f^*} & D(B,B_0)
  } 
$$

is an [[isomorphism]].

=--

+-- {: .proof}
###### Proof
Recall that $L_A$ is computed as the composite $D(A) \xrightarrow{u_*} D(M_A, A_0) \xrightarrow{p_!} D(A,A_0)$, where $M_A$ is the codirected mapping cylinder of $A_0\to A$.  We can therefore factor the above square as
$$\array{
  D(A) & \xleftarrow{f^*} & D(B) \\
  ^{u_*}\downarrow & & \downarrow^{u_*} \\
  D(M_A,A_0) & \xleftarrow{f^*} & D(M_B,B_0)\\
  ^{p_!}\downarrow & & \downarrow^{p_!} \\
  D(A,A_0) & \xleftarrow{f^*} & D(B,B_0)}
$$
It suffices, therefore, to show that the squares
$$\array{A & \xrightarrow{u} & M_A \\
  ^f \downarrow & & \downarrow^f \\
  B & \xrightarrow{u} & M_B}
\qquad\text{and}\qquad
\array{M_A & \xrightarrow{f} & M_B\\
  ^p\downarrow & & \downarrow^p\\
  A & \xrightarrow{f} & B}
$$
are homotopy exact.

For the first square, consider first a $b\in B$ and $a\in A\subset M_A$ and a $\varphi\colon f(a)\to b$ in $B\subset M_B$.  The category of triples $(a', a\to a', f(a')\to b)$ which compose to $\varphi$ is contractible, since $(a, id_a, \varphi)$ is an initial object.  Second, we should consider a $b\in B$ and an $a_0\in A_0 \subset M_A$, and a $\varphi\colon f(a_0)\to b$ in $B_0 \subset M_B$ --- but by definition of $M_B$, no such morphism $\varphi$ can exist.  Thus, the first square is always homotopy exact.

In fact, however, the preceeding argument is unnecessary, because we have seen that with their targets restricted as above, the functors $u_*$ are equivalences, and the [[mate]] of an isomorphism with respect to any pair of adjoint equivalences is again an isomorphism.  Note that the fact that $u_*$ is an equivalence was already used in making the assertion that $p_! u_*$ is a left adjoint to $D(A,A_0) \hookrightarrow D(A)$, and therefore the inverse of the top square already factors into the definition of the transformation appearing in the statement of the lemma.  (This may reassure a reader who was worried about the fact that the canonical transformation in the first square goes the "wrong direction".)

For the second square, consider first an $a\in A$ and a $b\in B\subset M_B$, and a $\varphi\colon b \to f(a)$.  The category we must investigate containts two types of objects:

* triples $(a'\in A, b\to f(a'), a' \to a)$ which compose to $\varphi$, and
* triples $(a_0 \in A_0, b\to f(a_0), a_0 \to a)$ which compose to $\varphi$.

By definition of $M_A$, the morphisms between these objects are the obvious ones, except that there are no morphisms from the second type to the first.  Now the full subcategory on the first type of object is coreflective, since $A_0$ is coreflective in $M_A$.  And that full subcategory is contractible, since $(a, \varphi, id_a)$ is a terminal object.  Thus, since adjunctions induce homotopy equivalences of nerves, the category in question is also contractible.

Finally, consider the case of an $a\in A$ and a $b_0\in B_0 \subset M_B$, and a $\varphi\colon b_0 \to f(a)$.  The category in question consists of triples $(a_0\in A_0, b_0 \to f(a_0), a_0\to a)$ which compose to $\varphi$ (since there are no morphisms in $M_B$ from $b_0\in B_0$ to anything in the image of $A\subset M_A$).  But this is precisely the category asserted to be contractible in the assumption that $f$ is locally null-final.
=--

+-- {: .num_theorem #HomotopyExactWithZeros1}
###### Theorem
If a square
$$\array{ I & \xrightarrow{f} & J \\
  ^h\downarrow & \swArrow & \downarrow^k\\
  K & \xrightarrow{g} & L}$$
of categories with zeros has the properties that

1. it is [[homotopy exact square|homotopy exact]] as a square of categories, when the full subcategories are ignored, and

1. $g$ is [locally null-final](#LocallyNullFinal),

then for any pointed derivator, the induced transformation
$$\array{ D(I,I_0) & \xleftarrow{f^*} & D(J,J_0) \\
  ^{h_!}\downarrow & \seArrow & \downarrow^{k_!}\\
  D(K,K_0) & \xleftarrow{g^*} & D(L,L_0)}$$
is an isomorphism.
=--
+-- {: .proof}
###### Proof
By definition, the displayed functors $h_!$ and $k_!$ are obtained by applying the $h_!$ and $k_!$ of a derivator followed by the reflection into the relative diagram categories.  Thus the given square factors into
$$\array{ D(I,I_0) & \xleftarrow{f^*} & D(J,J_0) \\
  ^{h_!}\downarrow & \seArrow & \downarrow^{k_!}\\
  D(K)  & \xleftarrow{g^*} & D(L)\\
  ^{L_K}\downarrow & \seArrow & \downarrow^{L_L}\\
  D(K,K_0) & \xleftarrow{g^*} & D(L,L_0)}$$
in which the first square is an isomorphism by the first assumption, and the second square by the second assumption and 
Lemma \ref{LocallyNullFinalLemma}.

=--

For example, we can conclude:

+-- {: .num_cor #LocallNullFinalFF}
###### Corollary
If $f\colon A\to B$ is a fully faithful and locally null-final functor between categories with zeros, then for any pointed derivator $D$, the functor $f_!\colon D(A,A_0) \to D(B,B_0)$ is fully faithful.
=--
+-- {: .proof}
###### Proof
The square
$$\array{ A & \xrightarrow{id} & A \\
  ^{id}\downarrow & \swArrow & \downarrow^f\\
  A & \xrightarrow{f} & B}$$
satisfies the hypotheses of the previous theorem.
=--

Theorem \ref{HomotopyExactWithZeros1} is not best possible, however.  Its two conditions characterize when the two squares into which the Beck-Chevalley transformation factors are separately isomorphisms.  However, it might happen that the composite is an isomorphism even though one or the other of the transformations is not separately an isomorphism.

In particular, the condition of "local null-finality" on the bottom morphism $g$ uses no information about the categories $I$ and $J$.  If we know some things about them, then we can correspondingly weaken this condition.

+-- {: .num_theorem #HomotopyExactWithZeros2}
###### Theorem
Suppose given a square
$$\array{ I & \xrightarrow{f} & J \\
  ^h\downarrow & \swArrow & \downarrow^k\\
  K & \xrightarrow{g} & L}$$
of categories with zeros, where $L$ is equipped with a full subcategory $\hat{L}_0 \subseteq L_0$ of its category of zeros.  Write $\check{L}_0 = L_0 \setminus \hat{L}_0$, and suppose the following.

1. The square is [[homotopy exact square|homotopy exact]] as a square of categories, when the categories of zeros are ignored.

1. For any pointed derivator $D$, the functor $k_!\colon D(J) \to D(L)$ maps $D(J,J_0)$ into $D(L,\hat{L}_0)$.  For instance, this is the case if for each $z\in \hat{L}_0$, the category $k/z$ has a terminal object lying in $J_0$.

1. For each $x\in L\setminus L_0$ and $y\in \hat{L}_0$ and morphism $x\xrightarrow{\varphi} y$ in $L$, the following category has a contractible nerve: its objects are triples $(z\in L_0, x\xrightarrow{\alpha} z, z\xrightarrow{\beta} y)$ such that $\beta\alpha=\varphi$, and its morphisms are morphisms $z_1\to z_2$ in $L$ commuting with the given morphisms *and* such that either $z_1 \in \hat{L}_0$ or $z_2 \notin \hat{L}_0$.

1. For every $x\in \check{L}_0$ and $y\in K$ and $x \xrightarrow{\varphi} g(y)$ in $L$, the category of triples $(z\in K_0 \cap g^{-1}(\check{L}_0), x\xrightarrow{\alpha} g(z), z \xrightarrow{\beta} y)$ such that $g(\beta).\alpha= \varphi$ has a contractible nerve ("relative local null-finality").

Then for any pointed derivator, the induced transformation
$$\array{ D(I,I_0) & \xleftarrow{f^*} & D(J,J_0) \\
  ^{h_!}\downarrow & \seArrow & \downarrow^{k_!}\\
  D(K,K_0) & \xleftarrow{g^*} & D(L,L_0)}$$
is an isomorphism.
=--

+-- {: .proof}
###### Proof
**(Sketch)** Because of the second condition in the theorem, instead of the reflection $D(L) \to D(L,L_0)$ it will suffice to consider the reflection $D(L,\hat{L_0}) \to D(L,L_0)$.  We use the third condition to give an alternate way to compute this reflection, and the fourth condition to ensure that restriction along $g$ commutes with this reflection.

Let $\hat{M}_L$ be the codirected mapping cylinder of $\check{L}_0 \hookrightarrow L$.  If $L \xrightarrow{u} \hat{M}_L \xrightarrow{p} L $ are as before, then $u_*$ identifies $D(L,\hat{L}_0)$ with the subcategory of $D(\hat{M}_L)$ consisting of diagrams which are zero on the copy of $\check{L}_l$ that is the target end of the mapping cylinder and on the copy of $\hat{L}_0$ inside the copy of $L$ that is the source end; call this subcategory $D(\hat{M}_L, \hat{L}_0 \cup \check{L}_0)$.

Now if the adjunction $p_! \colon D(\hat{M}_L) \rightleftarrows D(L) \;: p^*$ restricts to an adjunction $D(\hat{M}_L, \hat{L}_0 \cup \check{L}_0)\rightleftarrows D(L,L_0)$, we will be able to compute the reflection $D(L,\hat{L}_0) \to D(L,L_0)$ as $p_! u_*$, as before.  This will follow if the following square is exact:
$$\array{ \hat{L}_0 \cup \check{L}_0 & \to & \hat{M}_L \\
  \downarrow & & \downarrow \\
  L_0 & \to & L } $$
where $\hat{L}_0 \cup \check{L}_0$ denotes the same full subcategory of $\hat{M}_L$ as above.  Exactness of this square can be verified to be equivalent to the third condition in the theorem.

Finally, modifying the proof of Lemma \ref{LocallyNullFinalLemma}, we see that the fourth condition in the theorem implies commutativity of $g^*$ with this reflection $p_! u_*$.  Therefore, the theorem follows as before.
=--

If $\hat{L}_0 = \emptyset$, then the second and third conditions of Theorem \ref{HomotopyExactWithZeros2} are vacuous and it reduces to Theorem \ref{HomotopyExactWithZeros1}.  At the other extreme, if $\hat{L}_0 = L_0$, then the second and fourth conditions of Theorem \ref{HomotopyExactWithZeros2} are vacuous and the third becomes "$k_!$ maps $D(J,J_0)$ into $D(L,L_0)$."


### Extraordinary inverse images


+-- {: .num_theorem #EOInv}
###### Theorem
A derivator $D$ is pointed if and only if whenever $u\colon A\to B$ is a [[sieve]] in $Dia$, the functor $u_* \colon D(A) \to D(B)$ has a right adjoint $u^!$, and dually whenever $u$ is a cosieve, the functor $u_!$ has a left adjoint $u^?$.
=--
+-- {: .proof}
The "if" direction of this is easy, since $u\colon \emptyset \to B$ is always a sieve, while $u_*\colon * \to U(B)$ assigns the terminal object of $D(B)$.  Thus, if $u_*$ has a further right adjoint, it must preserve colimits, and in particular its value on the unique object of $D(\emptyset)$ must be an initial object (as well as a terminal one).

Conversely, if $D$ is pointed and $u$ is a sieve, then by Lemma \ref{SieveRel}, $u_*$ identifies $D(A)$ with $D(B,B\setminus A)$.  But by Theorem \ref{RelRefl}, the inclusion $D(B,B\setminus A)\hookrightarrow D(B)$ has a right adjoint.  The other case is dual.
=--

The functors $u^!$ and $u^?$ are sometimes referred to as *extraordinary* and *co-extraordinary inverse image* functors.  Our proof shows that $u^? = u^* p_! v_*$, where $v$ and $p$ are respectively the inclusion of $B$ in the codirected mapping cylinder of $B\setminus A \hookrightarrow B$, and its projection to $B$.

In the literature, the existence of these functors is often taken as the definition of when a derivator is pointed.  The equivalence of the two definitions is a "super-difficult" exercise in [Maltsionitis' notes](http://people.math.jussieu.fr/~maltsin/Seville/Lecture_III_Derivators.pdf).


### Loop and suspension

In a pointed derivator, we have a [[suspension]] functor $\Sigma\colon D 1 \to D 1$ defined as the composite
$$ D 1 \overset{a_*}{\to} D \Gamma \overset{a b c_!}{\to} D \square \overset{d^*}{\to} D 1$$
where $\square$ denotes the category
$$ \array{ a & \to & b \\ \downarrow & & \downarrow \\ c & \to & d } $$
and $\Gamma$ its full subcategory on $\{a,b,c\}$.

Equivalently, the suspension can be defined as the composite
$$ D 1 = D(1,\emptyset) \overset{(a,\emptyset)_!}{\to} D(\square,b c) \overset{(d,\emptyset)^*}{\to} D(1,\emptyset) = D 1.$$
This follows because we have $D 1 \simeq D(\Gamma,b c)$, and thus $(a,\emptyset)_!$ is isomorphic to $(a b c,b c)_!\colon D(\Gamma,b c) \to D(\square,b c)$, which by definition is $L_{\square,b c} \circ a b c_!$.  But $a b c_!$ is fully faithful since $a b c\colon \Gamma \hookrightarrow \square$ is, and so it already takes $D(\Gamma,b c)$ into $D(\square,b c)$.  Thus $L_{\square,b c}$ is doing nothing, so $(a,\emptyset)_!$ is essentially just $a b c_!$ which appeared in our previous definition of $\Sigma$.  (The other functor $a_*$ essentially implements the equivalence $D 1 \simeq D(\Gamma,b c)$.)

Similarly, we have a [[loop space object]] functor $\Omega\colon D 1 \to D 1$ defined as the composite
$$ D 1 \overset{d_!}{\to} D \Gamma^{op} \overset{b c d_*}{\to} D \square \overset{a^*}{\to} D 1.$$
where $\Gamma^{op}$ is the full subcategory of $\square$ on $\{b,c,d\}$, and it can equivalently be given as the composite
$$ D 1 = D(1,\emptyset) \overset{(d,\emptyset)_*}{\to} D(\square,bc) \overset{(a,\emptyset)^*}{\to} D(1,\emptyset) = D 1.$$
The description in terms of relative diagram categories makes it clear that $\Sigma \dashv \Omega$.

We can also describe $\Sigma$ and $\Omega$ in terms of the extraordinary inverse image functors.  Since the square
$$ \array{ \Gamma & \to & \Gamma \\
^r\downarrow & & \downarrow^{a b c}\\
* & \underset{d}{\to} & \square}$$
is homotopy exact, the composite $d^* a b c_!$ in our first definition is the same as $r_!$.  The other functor $a_*$ can in turn be decomposed as a composite $a b_* s_*$, where $s\colon * \to I$ is the inclusion of $s$ into the interval category $(s\to t)$, and $ab\colon I\to \Gamma$ is the inclusion into $\{a,b\}$.

Therefore we have $\Sigma \cong r_! a b_* s_*$.  But $\Gamma$ can be identified with $M s$ and $a b$ with the inclusion $u\colon I \hookrightarrow M s$, while $r$ factors as $M s \overset{p}{\to} I \overset{q}{\to} *$ so that $r_! \cong q_! p_!$.  But finally, the square
$$\array{* & \overset{t}{\to} & I\\
\downarrow & & \downarrow^q\\
*& \to & *}$$
is homotopy exact, so $q_! \cong t^*$ and thus
$$\Sigma \cong t^* p_! u_* s_* \cong t^? s_*.$$
Dually, we can identify $\Omega \cong s^! t_!$, from which it again follows directly that $\Sigma \dashv \Omega$.

### Enrichment over pointed sets

Every pointed derivator can be canonically "[[enriched derivator|enriched]]" over [[pointed sets]], in the sense that we can extend it to a functor
$$D': \; Set_* Cat \; \to\; Set_* CAT$$
from small $Set_*$-enriched categories to large ones, satisfying analogues of the derivator axioms.  Specifically, if $C$ is a $Set_*$-category, define $\bar{C}$ to be $C$ with a [[zero object]] adjoined.  (Note that zero objects are [[absolute colimits]] in $Set_*$-categories.)  Then set $D'(C) = D(\bar{C},0)$, the "relative diagram category" as defined above, i.e. the full subcategory of $D(\bar{C})$ on those diagrams which send the zero object to zero.

Any $Set_*$-functor automatically preserves zero objects (since an object $x$ of a $Set_*$-category is zero iff its identity $id_x$ is the basepoint of the pointed homset $hom(x,x)$).  In particular, any $Set_*$-functor $u:A\to B$ induces a relative functor $(u,0):(\bar{A},0) \to (\bar{B},0)$, and hence a pullback $u^* = (u,0)^*:D'(B) \to D'(A)$.  According to the general theory of relative diagram categories, this functor has left and right adjoints $u_!$ and $u_*$, obtained from left and right extension along $u$ followed by reflection or coreflection from $D(\bar{B})$ into $D(\bar{B},0)$.  In fact, however, in this case the reflection/coreflection is unnecessary: since the comma category $(u,0)/0$ has a terminal object $0$, the functor $u_!$ already maps $D(\bar{A},0)$ into $D(\bar{B},0)$.

Thus we have a $Set_*$-analogue of the derivator axiom (Der3), existence of adjoints.  For the enriched axiom (Der2), conservativity, observe that if $I$ is the unit $Set_*$-category having one object $x$ with $hom(x,x) = S^0 = \{1_x, 0\}$, then $D'(I) \simeq D(*)$.  So the family of $Set_*$ functors $I \to A$ for any $Set_*$-category $A$ gives rise a family $*\to \bar{A}$ picking out the nonzero objects, but since any two zero objects are isomorphic, (Der2) for $D$ implies that the resulting family of functors $D'(A) \to D'(I)$ are jointly conservative.

We can also conclude a version of the axiom (Der4) about exact squares from the above theorems about exactness for categories with zeros.  Namely, if
$$\array{ A & \to & B \\ \downarrow & \swArrow & \downarrow \\ C & \to & D }$$
is a comma square of $Set_*$-categories, then
$$\array{ \bar{A} & \to & \bar{B} \\ \downarrow & \swArrow & \downarrow \\ \bar{C} & \to & \bar{D} }$$
is homotopy exact when considered as a square of ordinary categories.  Moreover, the functor $\bar{C} \to \bar{D}$ is always locally null-final.  Thus, by Theorem \ref{HomotopyExactWithZeros1}, our "$Set_*$-enriched derivator" satisfies the Beck-Chevalley condition for any comma square of $Set_*$-categories.

It remains to consider the axiom (Der1) regarding coproducts.  The coproduct "$A\vee B$" of two $Set_*$-categories $A$ and $B$, as $Set_*$-categories, is not quite a "disjoint" union, but rather includes zero morphisms in both directions from each category to the other.  The inclusions $i,j$ of $A$ and $B$ are fully faithful, however, and the induced functors $\bar{i}\colon \bar{A}\to \overline{A\vee B}$ and $\bar{j}\colon \bar{B}\to \overline{A\vee B}$ are locally null-final; hence the left extensions $i_! \colon D'(A) \to D'(A\vee B)$ and $j_!\colon D'(B) \to D'(A\vee B)$ are also fully faithful.

By exactness with zeros, we can show that $j^* i_!$ and $i^* j_!$ send everything to zero.  Therefore, if we define a functor $(i,j)_!\colon D'(A) \times D'(B) \to D'(A\vee B)$ by $(i,j)_!(X,Y) = (i_! X + j_! Y)$, then we have $(i^*, j^*)(i,j)_! \cong Id$.  On the other hand, by fully-faithfulness of $i_!$ and $j_!$, for any $Z\in D'(A\vee B)$ the map $i_! i^* Z \to Z$ is an isomorphism on objects of $A$, and similarly for $j$ and $B$; hence $(i,j)_! (i^*,j^*) \cong Id$ as well.  In particular, $(i^*,j^*)$ is an equivalence of categories, providing the $Set_*$-enriched version of (Der1).

+--{: .query}
What about (Der5)?
=--

Conversely, given a functor $D'$ as above satisfying the axioms as given above, we can define $D(A) = D'(A')$, where $A'$ denotes the free $Set_*$-category on an ordinary category $A$ (i.e. adjoin a new zero morphism between each pair of objects).  This $D$ will automatically satisfy axioms (Der3) (homotopy Kan extensions) and (Der2) (conservativity on objects) since $D'$ does, and it satisfies (Der1) on coproducts since $D'$ does and since $(A+B)' \cong A' + B'$.

+--{: .query}
Does (Der4) on Beck-Chevalley conditions carry back over?  Does this require a "pointed version of Cisinski's theorem"?
=--

Finally, of course each category $D(A) = D'(A')$ has a zero object, so $D$ is a pointed derivator.  Thus, it seems that $Set_*$-enrichment is an essentially equivalent way to express the notion of pointed derivator.  (This approach was used by Franke (see below).)

+--{: .query}
However, what is not immediately clear is that passing from $D$ to $D'$ and back to $D$ again gives the same derivator.  At first sight this seems to require a stronger theorem about homotopy exactness with zeros than is stated above, one in which the square need not be homotopy exact without zeros.
=--


## The pointed reflection

Every derivator can be made pointed in a universal way; given $D$ we define $D_*(A)$ to be the full subcategory of $D(A\times I)$ which is terminal when restricted along $0\colon A\to A\times I$.  It requires a little work to show that this is a derivator.  The main observation being that the inclusion $D_*(A) \hookrightarrow D(A\times I)$ has a left adjoint (the "mapping cone"), which can be constructed just as in the proof of Theorem \ref{RelRefl}.  See III.5 of [Heller's memoir](#HellerHomotopy).


## References

See [[derivator]] for general references.  The pointed reflection is discussed in III.5 of

* [[Alex Heller]], _Homotopy theories_ , Mem. AMS 71:383.
 {#HellerHomotopy}

The definition of relative diagram categories is taken from:

* [[Alex Heller]], _Stable homotopy theories and stabilization_ , [MR](http://www.ams.org/mathscinet-getitem?mr=1431157)
 {#HellerStable}

The $Set_*$-enriched approach is taken as basic in

* Jens Franke, _Uniqueness theorems for certain triangulated categories with an Adams spectral sequence_, [K-theory archive](http://www.math.uiuc.edu/K-theory/0139/)

See also

* [[Moritz Groth]], _Derivators, pointed derivators, and stable derivators_ ([pdf](https://arxiv.org/pdf/1112.3840.pdf))


[[!redirects pointed derivators]]
[[!redirects derivator with a zero object]]
[[!redirects zero object in a derivator]]
[[!redirects derivators with zero objects]]
[[!redirects zero objects in a derivator]]
