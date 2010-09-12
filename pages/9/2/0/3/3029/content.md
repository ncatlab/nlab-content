
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

* [[group cohomology]]

  * [[nonabelian group cohomology]], [[groupoid cohomology]]

* **group extension**

* [[Lie group cohomology]] 

  * [[∞-Lie groupoid cohomology]]

***

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _group extension_ of a [[group]] $G$ by a group $A$ is group $\hat G$ that sits in an [[exact sequence]] $A \to \hat G \to G$. 

(For now we will put emphasis on the general case i.e. nonabelian group extensions, later we plan a separate entry on abelian group extensions.) 

## Definition

We say that a sequence of [[group]]s

\[\label{shortExtension} 1\to K
\overset{i}\to G\overset{p}\to B\to 1\]

is **exact** if $i$ is [[monomorphism]], $p$ an [[epimorphism]] and $Ker(p)=Im(i)$. In terms of one-object groupoids, this is equivalent to saying that $\mathbf{B}K\to \mathbf{B}G\to \mathbf{B}B$ is a [[fibration sequence]]. If $K$ and $B$ are given groups, then any exact sequence of the form above is called an **extension** of $B$ by $K$ (some say conversely of $K$ by $B$). Letters are here chosen to suggest that $B$ is a base to which $G$ projects and $K$ is the *[[kernel]]* of $i$ and for $G$ itself we often say that it is a group extension of $B$ by $K$. 

If $K$ is abelian then we write $0$ instead of $1$ at the left start of the sequence, and if $B$ is exact we do the same at the right-hand end of the sequence. 

We say that two group extensions $1\to K\stackrel{i}\to G\stackrel{p}\to B\to 1$ and $1\to K\stackrel{i'}\to G'\stackrel{p'}\to B\to 1$ are **equivalent** if there is an [[isomorphism]] $\epsilon:G\to G'$ such that 
$\epsilon\circ i = i'$ and $p=p'\circ \epsilon$. In other words, there is a
commutative diagram

\[\label{equivExt}\array{
1\to &K&\stackrel{i}\to &G&\stackrel{p}\to &B&\to 1\\
&\downarrow\mathrlap{=}&&\downarrow\mathrlap\epsilon&&\downarrow\mathrlap=&\\
1\to &K&\stackrel{i'}\to &G'&\stackrel{p'}\to& B&\to 1
}\]

## Properties

### Torsors {#Torsors}

+-- {: .un_prop}
###### Prosition

For $A \stackrel{i}{\to} \hat G \stackrel{p}{\to} G$ a group extension, we have that $p : \hat G \to G$ is an $A$-[[torsor]] over $G$ with  the [[action]] of $A$ on $\hat G$ is defined by

$$  
  \rho : A \times \hat G \stackrel{(i,Id)}{\to} \hat G \times \hat G \stackrel{\cdot}{\to} \hat G
  \,.
$$


=--

+-- {: .proof}
###### Proof

That $\rho$ is indeed an action _over_ $B$ in that

$$
  \array{  
     A \times \hat G &&\stackrel{\rho}{\to}&& \hat G
     \\
     & {}_{\mathllap{ p \circ p_2}}\searrow && \swarrow_{\mathrlap{p}}
     \\
     && \hat G 
  }
$$

follows from the fact that $p$ is a group homomorphism and that $A$ is in its [[kernel]].

That $A$ is actually _equal_ to the kernel gives the principality condition

$$
  (\rho, p_2) : A\times \hat G \stackrel{\simeq}{\to} \hat G \times_G \hat G
  \,.
$$

=--

For $A$ an [[abelian group]] we may understand the $A$-torsor/$A$-[[principal bundle]] $\hat G$ as the [[delooping]] of the $\mathbf{B}A$-[[principal 2-bundle]] $\mathbf{B} \hat G \to \mathbf{BG}$ that is classified by (is the [[homotopy fiber]] of) the 2-[[cocycle]] in [[group cohomology]]  $c : \mathbf{B}G \to \mathbf{B}^2 A$ that classifies the extension.

All this is then summarized by the statement that

$$
  A \to \hat G \to G \to \mathbf{B}A \to \mathbf{B}\hat G \to \mathbf{B}G \stckrel{c}{\to}
  \mathbf{B}^2 A
$$

is a [[fiber sequence]] in [[∞Grpd]] (or in [[?LieGrpd]] if we have [[Lie group]] extensions, etc).
## Schreier theory for nonabelian group extensions

### Traditional way

[[Otto Schreier]] (1926) and [[Samuel Eilenberg|Eilenberg]]-[[Saunders MacLane|Mac Lane]] (late 1940-s) developed a theory of classification of nonabelian extensions of abstract groups leading to the low dimensional [[nonabelian group cohomology]]. This is sometimes called **Schreier's theory** of nonabelian group extensions.

The traditional Schreier-Mac Lane way to obtain nonabelian group 2-cocycle
from a group extension as above starts with choosing a set-theoretic section of $p:G\to B$. 

Note. The exposition which follows in this long "traditional" section of this entry is mainly from personal notes of Zoran &#352;koda from 1997. 

Each element $g$ of $G$ defines an inner automorphism $\phi(g)$ of $K$
by $\phi(g)(k) = gkg^{-1}$. 
The restriction $\phi|_K$ takes
(by definition) values in the subgroup $Int(K)$ of inner automorphisms
of $K$. In fact $\phi:G\to Inn(G)\subset Aut(K)$ is a homomorphism of groups.

If $g_1$ and $g_2$ are in the same left coset, that is $g_1K = g_2K$,
then there is $k \in K$, $g_1 = g_2k$, so that $\forall k' \in K$ we have
$\phi(g_1k') = \phi(g_2kk') = \phi(g_2)\phi(kk')$ and therefore
$\phi(g_1K) \subset \phi(g_2)Int(K)$. Thus we obtain a well-defined map
$\phi_* : G/K \rightarrow Aut(K)/Int(K)$.
Choose a set-theoretic section of the projection $p : G \rightarrow B$
and let
\[\psi \stackrel{def}{=} \phi \circ \sigma: B \rightarrow Aut(K).\]
**Warning.** Unlike $\phi$, the map $\psi$ is *not* a homomorphism of groups. 

We attempt to reconstruct $G$ from
the knowledge of $\psi$ and $K$.
As a set, $G$ can be naturally identified with $B \times K$.
Indeed, write each element $g \in G$ as
$\sigma(b)k, b \in B, k \in K$ by setting
$b = p(g), k = \sigma(p(g))^{-1}g$. 
Elements $b \in B$ and $k \in K$ in that decomposition are unique,
and we get a bijection
\begin{equation}
B\times K\ni (b,k)\mapsto\sigma(b)k \in G,
\end{equation}
whose inverse is the map $g \mapsto (p(g), \sigma(p(g))^{-1}g)$.
By means of that bijection, $B \times K$ inherits the group structure
from $G$. Let us figure out the multiplication rule on $B \times K.$
If $\sigma(b_1)k_1 = g_1$, and $\sigma(b_2)k_2 = g_2$, then,
\begin{equation}
g_1g_2 = \sigma(b_1)k_1\sigma(b_2)k_2 =
\sigma(b_1)\sigma(b_2)\sigma(b_2)^{-1}k_1\sigma(b_2)k_2.
\end{equation}
 Now $p(\sigma(b_1)\sigma(b_2)) = p(b_1b_2)$ so
$$\chi(b_1,b_2) \stackrel{def}{=}
 \sigma(b_1b_2)^{-1}\sigma(b_1)\sigma(b_2) \in K.
$$
This formula clearly
defines a function $\chi : B \times B \rightarrow K$. In this notation, 
$$\array{
g_1g_2 & = & \sigma(b_1b_2)\chi(b_1,b_2)\phi(\sigma(b_2)^{-1})(k_1)k_2 \\
       & = & \sigma(b_1b_2)\chi(b_1,b_2)[\psi(b_2)^{-1}(k_1)] k_2.
}$$
and using bijection of $G$ with $B\times K$ this can be expressed in terms of elements in $B\times K$ so that
\begin{equation}\label{mrule}
(b_1,k_1)(b_2,k_2) = (b_1b_2,\chi(b_1,b_2)[\psi(b_2)^{-1}(k_1)] k_2).
\end{equation}

According to this formula, *all the information about the multiplication is encoded in functions $\chi : B \times B \rightarrow Aut(K)$
and $\psi : B \rightarrow Aut(K)$, and we may forget about $\sigma$* at this point. However, _not every pair $(\chi,\psi)$ will
give some multiplication rule on $B \times K$_.
Let $a,b,c \in B$,
and $e = e_K$ be the unity element in $K$.
Then
$$
[(a,e)(b,e)](c,e) = (a b, \chi(a,b))(c,e) =
 (a b c, \chi(a b,c) \psi(c)^{-1}(\chi(a,b))).
$$
From the other side, this has to be the same, by associativity, to
$$
(a,e)[(b,e)(c,e)] = (a,e)(bc,\chi(b,c)) = (a b c,\chi(a,b c)\chi(b,c))
$$
where we took into account that expressions like $[\psi^{-1}(b)(e)] = e$,
because $\psi(b)$ is an *automorphism* for each $b \in B$.

 Comparing the expressions above we obtain
\[\label{psi1}
 \chi(a b,c)\psi(c)^{-1}(\chi(a,b)) = \chi(a,b c)\chi(b,c),
    for all a,b,c \in B.
\]

If the pair $(\chi,\psi)$ is constructed as above, then

$$\array{
\psi(a)\psi(b)k & = & \phi(\sigma(a))\phi(\sigma(b))k \\
        & = & \sigma(a)\sigma(b)k\sigma(b)^{-1}\sigma(a)^{-1} \\
        & = & \sigma(a b)\chi(a,b)k\chi(a,b)^{-1}\sigma(a b)^{-1} \\
        & = & \psi(a b) Ad_K(\chi(a,b)) k,
}$$

where $Ad_K$ is the canonical map $K \rightarrow Int(K)$, $k\mapsto k(-)k^{-1}$.

Thus we obtain the relation
\[\label{psi2}
\psi(a)\psi(b) = \psi(a b) Ad_K(\chi(a,b))
\]

+-- {: .un_defn}
###### Definition
Let $B$ and $K$ be two groups.
Let $\chi: B \times B \rightarrow K$
and $\psi : B \rightarrow Aut(K)$ satisfy \eqref{psi1}
and \eqref{psi2}. Then we call that the family
$\{\chi(b_1,b_2)| b_1,b_2 \in B\}$
is a factor system (This term is due Schreier(1924))
or a **nonabelian group 2-cocycle with automorphisms**, and
the family $\{\psi(b) | b \in B \}$ -- a system of automorphisms
=--

A 2-cocycle $\chi$ is **counital** if $\chi(b,e) = \chi(e,b) = e$, for all $b \in B$.

If $K$ is commutative, then $\psi$ is always a homomorphism (cf. (eq:psi2)). Then $K$ is a right $B$-module through $\psi(-)^{-1}$. That justifies the sometimes used term "(right) cocycle $B$-module" for $(K,\psi,\chi)$. If $\psi$ is trivial ($\psi(b) = Id_K, \forall b \in B$)
then the cocycle condition (eq:psi1) becomes
\begin{equation}
\chi(a b,c)\chi(a,b) = \chi(a,b c)\chi(b,c). 
\end{equation}

+-- {: .un_theorem}
###### Theorem
If formulas (eq:psi1) and (eq:psi2)
are both satisfied, then the formula (eq:mrule)
for multiplication of pairs defines a group multiplication on $B \times K$. That set, together
with multiplication (eq:mrule) is called the
**cocycle cross product** of $B$ and $K$ with cocycle $\chi$ and
action $\psi$. If the cocycle is trivial i.e. $\chi(\cdot,\cdot) = e_K$,
we call it the **(external) semidirect product**.
=--

+-- {: .proof}
###### Proof
The checking the associativity we have done above for pairs of the form $(a,e)$ etc. This was useful to find the cocycle condition correctly. Now the general associativity should be a similar calculation with general elements. Using (eq:psi1) and (eq:psi2) it can be done.

$$\array{
\psi(a)\psi(e)k & =& \psi(a)Ad_K(\chi(a,e))k \\
& = &\psi(a)\chi(a,e)k\chi(a,e)^{-1}
}$$
where we used \eqref{psi2}.

Thus $Ad_K(\chi(a,e)) = \psi(e)$ and therefore it does not
depend on $a$.

Then use (eq:psi1) with $b = c = e$ to get
$\psi(e)^{-1}(\chi(a,e)) = \chi(e,e), \forall a \in B$.

Thus $\chi(a,e)^{-1}(\chi(a,e))\chi(a,e) = \chi(e,e)$,
that is $\chi(a,e)$ does not depend on $a$.

Now we claim that the *unit* element is given by $(e, \chi(e,e)^{-1})$.
To verify that it is also a right unit we compute

$$\array{
(a,b)(e,\chi(e,e)^{-1}) & = & (a, \chi(a,e) \psi(e)^{-1}(b)\chi(e,e)^{-1}) \\
& = & (a, \chi(a,e)\chi(e,e)^{-1}b\chi(e,e)\chi(e,e)^{-1})
}$$

what is equal to $(a,b)$ by just proved statement that
$\chi(a,e)$ does not depend on $a$.

Now use (eq:psi1) with $a = b = e$ to get

\[\label{psiac}
\psi(c)^{-1}(\chi(e,e)) = \chi(e,c), \forall c \in B.
\]

Thus we can verify that $(e, \chi(e,e)^{-1})$ is a left unit too
by a calculation as follows. Namely

$$(e,\chi(e,e)^{-1})(a,b)= (a,\chi(e,a)\psi(a)^{-1}(\chi(e,e)^{-1})b)$$

by the definition of the product. Then by (eq:psiac), this equals to

$$(a,\psi(a)^{-1}(\chi(e,e))\psi(a)^{-1}(\chi(e,e)^{-1})b)$$

and, because $\psi(a)^{-1}$ is an antiautomorphism, this is finally
equal to $(a,b)$.

Now check that each element $(a,b)$ can be
factorized as $(a,e)(e,\chi(e,e)^{-1}b)$.
In order to show that $(a,b)$ has
an inverse it is then enough to
show that both $(a,e)$ and
$(e,\chi(e,e)^{-1}b)$ have inverses.

Claim: the inverse of $(a,e)$ is 

$$(a^{-1},\chi(a,a)^{-1}\chi(e,e)^{-1}).$$ 

To this aim, we calculate

$$(a,e)(a^{-1},\chi(a,a^{-1})^{-1}\chi(e,e)^{-1}) = (e,\chi(a,a^{-1})\psi(a^{-1})^{-1}(e)\chi(a,a^{-1})^{-1}\chi(e,e)^{-1}) =(e,\chi(e,e^{-1}),$$ 

because $\psi(a)^{-1}(e) = e$. Furthermore, 

$$(a,e)(a^{-1},\chi(a,a^{-1})^{-1}\chi(e,e)^{-1}) = (e,\chi(a,a^{-1})\psi(a^{-1})^{-1}(e)\chi(a,a^{-1})^{-1}\chi(e,e)^{-1}) = (e,\chi(e,e^{-1}),$$ 

because $\psi(a)^{-1}(e) = e$. Next, 

$$(a^{-1},\chi(a,a^{-1})^{-1}\chi(e,e)^{-1})(a,e) =
(e,\chi(a^{-1},a)\psi(a)^{-1}(\chi(a,a^{-1}) \chi(e,e)^{-1}))$$ 

what equals $(e,\chi(e,e)^{-1})$.

Indeed, (eq:psi1) with $a = a, b = a^{-1}, c = a$
reads $\chi(e,a) \psi(a)^{-1}(\chi(a, a^{-1}))$ $=\chi(a,e)\chi(a^{-1},a)$.

Then apply (eq:psiac) and take inverse of both sides
to obtain

$$\psi(a)^{-1}(\chi(a,a^{-1})^{-1}\chi(e,e)^{-1}))
= \chi(a^{-1},a)^{-1}\chi(a,e)^{-1}.$$ 

Then recall that $\chi(a,e)$ does not depend on $a$ and multiply by  $\chi(a^{-1},a)$ from the left.

Claim: the inverse of $(e,\chi(e,e)^{-1}k)$
is $(e,\chi(e,e)k^{-1})$.
Here the verification is symmetric ($k$ vs. $k^{-1}$) for the left and for the right inverse and immediate.
=--

Given groups $K$ and $B$ and any maps $\chi$ and $\psi$ satisfying (eq:psi1) and (eq:psi2), needed to define a cocycle cross product $B\times_\chi K$ of $K$ and $B$, one defines the map $i : K \rightarrow B \times_\chi K$ by $k \mapsto (e,\chi(e,e)^{-1}k)$.
Then $i$ is a monomorphism of groups, $i(K)$ is
a normal subroup of the cocycle cross product of $B$ and $K$,
and there is a canonical isomorphism $B \cong G/K$.
We define the set-theoretic maps $\sigma',\chi'$ and $\psi'$
as follows. $\sigma' : B \rightarrow B \times K$
is defined by $\sigma'(b) = (b, e)$ , for all $b \in B$.
Then $\chi' : B \times B \to i(K)$ is defined by
$\chi'(b_1,b_2) = \sigma'(b_1b_2)^{-1}\sigma'(b_1)\sigma'(b_2)$
and $\psi' : B \to Aut(i(K))$ is defined
    by $\psi'(b)i(k) = \sigma'(b)i(k)\sigma'(b)^{-1}$.
Using the natural identifications $i : K \cong i(K)$,
and $i_{Aut} : Aut(i(K)) \cong Aut(K)$, we have $\psi' = i_{Aut}\circ \psi$ and $\chi' = i \circ \chi$. Now

$$\array{
\chi'=i\circ\chi 
&\Leftrightarrow&(b_1,e)(b_2,e)(e,\chi(e,e)^{-1}k)
=(b_1 b_2,e)(e,\chi(e,e)^{-1}\chi(b_1,b_2)k)\\
&\Leftrightarrow& (b_1b_2,\chi(b_1,b_2))(e,\chi(e,e)^{-1}k) = (b_1 b_2,\chi(b_1 b_2,e)\chi(e,e)^{-1}\chi(b_1,b_2)k)\\
&\Leftrightarrow&
\chi(b_1 b_2,e)\psi(e)^{-1}(\chi(b_1,b_2))\chi(e,e)^{-1}k = \chi(b_1 b_2,e)\chi(e,e)^{-1}\chi(b_1,b_2)k
}$$

for all $b_1,b_2 \in B$ for all $k \in K$ in all these lines.
The last line is true by (eq:psi1).

Similarly, $\psi' = i_{Aut} \circ \psi$ iff $(b,e)(e,\chi(e,e)^{-1}k) = (e,\chi(e,e)^{-1}\psi(b)k)(b,e)$ for all $b$ and $k$. 

Here the LHS computes as $(b,k)$ using $\chi(b,e) = \chi(e,e)$, and the RHS is 

$$(e,\psi(b)k)(b,e) = (b, \chi(e,b)\psi(b)^{-1}(\chi(e,e)^{-1}\psi(b)(k)))
= (b, k)$$

by (eq:psiac).

**Proposition.** The following are equivalent

* (i) extension \eqref{shortExtension} is split

* (ii) for extension \eqref{shortExtension}
there is a subgroup $B_1 \subset G$ such that
$B_1 \cap i(K) = 1$ and $B_1i(K) = G$
($G$ is an internal semidirect product of $K$ and $B_1$).

* (iii) extension \eqref{shortExtension} is
isomorphic to an external semidirect product
of $K$ and $B$. 

*Proof.* (i) $\Rightarrow$ (ii) If the extension is split then
there is a *homomorphism* $\sigma : B \rightarrow G$
such that $p \circ \sigma = id_B$. Let $B_1 = \sigma(B)$.
By exactness of \eqref{shortExtension}), all
elements in $i(K)$ map $p$ sends to 1, and by
 $p \circ \sigma = id_B$ map $p|_{B_1}$ is injection,
therefore the only element in $i(K)$
which belongs to $B_1$ is 1.

$B_1i(K) = G$ is also obvious: e.g. for given $g \in G,$
$p(g) = p\sigma p(g)$, so that $p((\sigma p (g))^{-1}g) = 1$
what means $(\sigma p (g))^{-1}g \in {Ker}(p)$ so that
$g = (\sigma p (g))i(k)$ for some $k \in K$ by exactness.


(ii) $\Rightarrow$ (iii) Our previous elaborate discussion of
cocycle cross products makes it obvious:
choosing a section $\sigma$ which is a homomorphism
gives $\chi(a,b) = 1$, and we can construct
equivalent external semidirect product
as a cocycle cross product with trivial $\chi$.

(iii) $\Rightarrow$ (i) Equivalence of extensions preserves the
property of the corresponding short exact sequence to be split.
Every external semidirect product is as a set $K\times B$
and the product is given by formula \eqref{mrule} without a cocycle.
The map $\sigma : B \rightarrow G$,
$B \ni b \mapsto (1_K,b) \in K \times B$, splits the sequence.

**Definition.** Extension \eqref{shortExtension} is Abelian
iff $K$ is Abelian. An Abelian extension \eqref{shortExtension}
is central iff it is isomorphic to a cocycle cross product
extension with all the automorphisms $\psi(b), b \in B$ trivial.
We say that the extension \eqref{shortExtension}
is Abelian iff $G$ is Abelian.

Remarks. (i) Note that \eqref{psi2} implies that $\psi$
is a homomorphism if $K$ in the case of Abelian extensions (for
any choice of set-theoretic section $\sigma$.

(ii) If $G$ is Abelian then \eqref{shortExtension} is central,
but not every central extension is corresponding to an Abelian $G$.
Abelian extensions in terms of the above definition trivially
(strictly!) include both central extensions and extensions with $G$
central.
By abuse of language one sometimes says for $G$
to be an extension of $K$ what leads to strange expression that not every
Abelian extension (as extension -- in terms of the definition above) is Abelian (as a group).



#### Comparing different extensions;  2-coboundaries {#2Coboundaries}

Let us now investigate when two extensions
$G_1$ and $G_2$ of $B$ by $K$,
given by $\psi,\chi$ and $\psi',\chi'$ respectively, are equivalent, cf. diagram \eqref{equivExt}.

We know that $\epsilon|_K : i(k) \stackrel{\epsilon}\mapsto i'(k)$, for all $k \in K$.
The formula for $i$ in \luse{crossform} says that whenever we represent
an extension as a cocycle extension we have $i(k) = (e,\chi(e,e)^{-1}k).$
Thus $\epsilon(e,\chi(e,e)^{-1}k) = (e,\chi'(e,e)^{-1}k)$, for all $k \in K.$ Also recall (or recalculate) that every element $(a,k)$ in $G$ can be
factorized as $(a,e)(e,\chi(e,e)^{-1}k)$.
By the definition $\epsilon$ is a homomorphism of groups,
so $\epsilon(a,k) = \epsilon(a,e)\epsilon(e,\chi(e,e)^{-1}k)$.
Also the cosets are preserved, so $\epsilon(a,e) = (a,\lambda(a))$
where $\lambda : B \rightarrow K$ is some set-theoretic map.
Thus

$$\array{
\epsilon(a,k) & = & (a,\lambda(a))(e,\chi'(e,e)^{-1}k) \\
    & = & (a, \chi'(a,e)\psi'(e)^{-1}(\lambda(a))\chi'(e,e)^{-1}k) \\
    & = & (a, \lambda(a)k).
}$$

Now multiply more general elements in $G$:

$$
\array{
\epsilon((b_1,k_1)(b_2,k_2)) = (b_1,\lambda(b_1)k_1)(b_2,\lambda(b_2)k_2) \\
= (b_1b_2,\chi'(b_1,b_2)\psi'(b_2)^{-1}(\lambda(b_1)k_1)\lambda(b_2)k_2)
}$$

what should be the same as

\[
\epsilon((b_1b_2,\chi(b_1,b_2)\psi(b_2)^{-1}(k_1)k_2))
 = (b_1b_2,\lambda(b_1b_2)\chi(b_1b_2)\psi(b_2)^{-1}(k_1)k_2)
\]

In a special case, when $k_1 = e_K$ we have therefore

\begin{equation}
\chi(b_1,b_2) = \lambda(b_1b_2)^{-1}\chi'(b_1,b_2)
\psi'(b_2)^{-1}(\lambda(b_1))\lambda(b_2) \label{equiv1}
\end{equation}

In order to obtain a relation between $\psi'(b)(k)$
and $\psi(b)(k)$ note that
\[
\epsilon ((e,\chi(e,e)^{-1}k)(b,e)) = (e, \chi'(e,e)^{-1}k)(b,\lambda(b)).
\]
That is equivalent to any in the following chain of formulas:
$$\array{
\epsilon (b,\chi(e,b)\psi(b)^{-1}(\chi(e,e)^{-1}k)) &=&
    (b, \psi'(b)^{-1}(\chi'(e,e)^{-1}k)\lambda(b)) \\
\Leftrightarrow \lambda(b)\chi(e,b)\psi(b)^{-1}(\chi(e,e)^{-1}k))
&=& \chi'(e,b)\psi'(b)^{-1}(\chi'(e,e)^{-1}k)\lambda(b) 
}$$

Then by \eqref{psiac}, it follows that 
$$\array{
     \lambda(b)\chi(e,b)\chi(e,b)^{-1}\psi(b)^{-1}(k)
&=& \chi'(e,b)\chi'(e,b)^{-1}\psi'(b)^{-1}(k)\lambda(b)   \\
\Leftrightarrow \lambda(b)\psi(b)^{-1}(k))
&=& (\psi'(b)^{-1}(k))\lambda(b) \\
\Leftrightarrow (Ad_K(\lambda(b)) \circ\psi(b)^{-1})(k)
&=& \psi'(b)^{-1}(k)
}$$

Now invert the maps in $Aut(K)$ to obtain

\[
\psi'(b) = \psi(b)Ad_K(\lambda(b)^{-1}) \label{equiv2}
\]

Thus we obtain

**Theorem.** Two extensions of a group $B$ by group $K$ with
corresponding systems $(\psi,\chi)$ and $(\psi',\chi')$ are
equivalent iff there is a homomorphism
$\lambda: B \rightarrow K$ such that
the relations \eqref{equiv1}
and \eqref{equiv2} are valid.

If function $\lambda$ takes values in the center of $B$
then \eqref{equiv2} implies that $\psi' = \psi : B \rightarrow Aut(K)$
and conversely.

If instead of functions $\psi$ and $\psi'$ we consider the
respective maps into the group of external automorphisms
(cosets of automorphisms with respect
to the group of internal homomorphisms)
$[\psi], [\psi']:~B \rightarrow Aut(K)/Int(K)$,
then the equivalent extensions define the same maps.
By \eqref{psi2} these maps are actually homomorphisms (unlike e.g.$\psi$).
For a given $\psi$ if there is $\chi$ so that $(\psi,\chi)$ does define
an extension of $B$ by $K$ we say that
the extension is *associated* to (the homomorphism) $[\psi]$.
That does not mean that any given homomorphism
in $hom_{Group}(B,Aut(K)/Int(K))$
is associated to any extension, nor it means that if
a homomorphism is associated to some extension,
that every its representative in $hom_{Set}(B,Aut(K))$
is a part of a pair $(\psi,\chi)$ defining an extension.
To see that situation in more detail we start with a *given*
automorphism, which we call $\theta$ ,
and *choose* an element $\psi(a)\in\theta(a)$, the representative
of a coset in $Aut(K)/Int(K)$;
that choice should be specified for all $a \in B$.
Note that for any $\rho \in Aut(K), a \in K$ we have, by direct inspection,
$\rho Ad_K(a)\rho^{-1} = Ad_K(\rho(a))$. Thus there is a well-defined function

$$  Ad_K \circ h : B \times B \rightarrow Int(K), \,\,\,
(Ad_K\circ h)(a,b) := \psi(a b)^{-1}\psi(a)\psi(b)$$

- indeed 

\[\psi(a)Ad_K(r_1)\psi(b)Ad_K(r_2) = \psi(a)\psi(b)Ad_K(\psi(b)^{-1}(r_1)r_2)\] 

so choosing $\psi(a b) \in [\psi(a b)]$ is the same as choosing it in $[\psi(a)][\psi(b)]$ and guarantees that $\psi(a b)^{-1}\psi(a)\psi(b)$ is in $Int(K)$. Let us choose some $h$ so that $Ad_K \circ h$ is interpretable as a genuine composition.

$$\array{
(\psi(a)\psi(b))\psi(c) & = & \psi(a b)Ad_K(h(a,b))\psi(c) \\
    & = & \psi(a b)\psi(c)\psi(c)^{-1}Ad_K(h(a,b))\psi(c) \\
    & = & \psi(a b c)Ad_K(h(a b,c))Ad_K(\psi(c)^{-1}h(a,b)) \\
    & = & \psi(a b c)Ad_K(h(a b,c)\psi(c)^{-1}h(a,b))
}$$

what is by associativity the same as

$$\array{
\psi(a)(\psi(b)\psi(c)) & = & \psi(a)\psi(b c)Ad_K(h(b,c)) \\
    & = & \psi(a b c)Ad_K(h(a,b c))Ad_K(h(b,c)) \\
    & = & \psi(a b c)Ad_K(h(a,b c)h(b,c)).
}$$

Thus $Ad_K(h(a b,c)\psi(c)^{-1}h(a,b)) = Ad_K(h(a,b c)h(b,c)).$
Two elements of $K$ generate the same automorphism iff they
differ by a central element. Thus

\begin{equation} \label{2semicoc}
h(a b,c)\psi(c)^{-1}h(a,b) = h(a,b c)h(b,c)z(a,b,c)
\end{equation}

for a unique central element $z(a,b,c) \in Z(K).$
 The correspondence $z : (a,b,c) \mapsto z(a,b,c)$ maps
$B \times B \times B$ into $Z(K)$.

**Proposition.** $z$ is an (Abelian) 3-cocycle with values
 in $_/Z(K)_{\psi^{-1}}$
($Z(K)$ understood as trivial-$\psi^{-1}$ $B$-bimodule):

\begin{equation}
z(b,c,d)z(a,b c,d)\psi(d)^{-1}z(a,b,c) = z(a,b,c d)z(a b,c,d)
\label{3coc}
\end{equation}

To see this we calcuate
$$\array{
h(a b c,d)[\psi(d)^{-1}h(a b,c)\psi(c)^{-1}h(a,b)]
& = h(a b c,d)[\psi(d)^{-1}h(a,b c)h(b,c)z(a,b,c)] \\
& = h(a,b c d)h(b c,d)z(a,b c,d)[\psi(d)^{-1}h(b,c)z(a,b,c)] \\
& = h(a,b c d)h(b,c d)h(c,d)z(b,c,d)z(a,b c,d)\psi(d)^{-1}z(a,b,c)
}$$
Compare
$$\array{
h(a b c,d)[\psi(d)^{-1}h(a b,c)\psi(c)^{-1}h(a,b)]
& = h(a b c,d)[\psi(d)^{-1}h(a,b c)]\psi(d)^{-1}\psi(c)^{-1}h(a,b) \\
& = h(a b c,d)[\psi(d)^{-1}h(a b,c)]h(c,d)^{-1}[\psi(c d)^{-1}h(a,b)]h(c,d) \\
& = h(a b c,d)h(a b,c d)z(a b,c,d)[\psi(c d)^{-1}h(a,b)]h(c,d) \\
& = h(a,b c d)h(b,c d)h(c,d)z(a,b,c d)z(a b,c,d)
}$$

**Proposition.** (i) If we choose a different $h$
such that 

$$Ad_K(h(a,b)) = \psi(a b)^{-1}\psi(a)\psi(b),$$

then $z$ will change only up to a 3-coboundary $d f,$
i.e. there is a function $f : B \times B \rightarrow Z(K)$,
such that $z' = (d f)z$ where

\[ (d f)(a,b,c) = f^{-1}(b,c)f^{-1}(a,b c)f(a b,c)\psi(c)^{-1}f(a,b),\,\,\,\,\,
for all a,b,c \in B.\]

(ii) Conversely, if $z$ is
a 3-cocycle obtained from $\psi$ as above and $d f$ is a 3-coboundary,
then there is a $h'$ determining
the same inner automoprhism of $K$
such that the corresponding 3-cocycle $z'$ is equal to $(df)z$.

(iii) Let $\psi, \psi' : B \rightarrow Aut(K)$ be
two set-theoretic sections so that $[\psi] = [\psi'] = \theta : B
\rightarrow Aut(K)/Int(K)$, then (for arbitrary choice of
$h$, $h'$) the cocycles $z$ and $z'$
obtained as above differ only up to a 3-coboundary. $\|$

*Proof.* (i) Choose two different $h',h: B \times B \rightarrow K$
such that $Ad_K(h') = Ad_K(h)$. Then $h'(a,b) = h(a,b)f(a,b)$ where
$f : B \times B \rightarrow Z(K)$ is some function with values
in center of $K$.  A direct comparison of \eqref{2semicoc} written for
$h,z$ and $h',z'$ respectively proves the assertion.

(ii) Trivial: Any $f : B \times B \rightarrow Z(K)$
such that $h' = hf$ will not change the inner automorphism.
Thus any central 3-coboundary  $df$ can be obtained by
changing a choice of $h$.

(iii) $[\psi'] = [\psi]$ implies that exists $k : B \rightarrow K,
\psi'(a) = \psi(a)Ad_K(k(a)).$ Then

$$\array{
\psi'(a b)Ad_K(h'(a,b)) & = & \psi'(a)\psi'(b) = \psi(a)Ad_K(k(a))\psi(b)Ad_K(k(b))\\
& = & \psi(a)\psi(b)Ad_K([\psi(b)^{-1}k(a)]k(b)) \\
& = & \psi(a b)Ad_K(h(a,b)[\psi(b)^{-1}k(a)]k(b)) \\
& = & \psi'(a b)Ad_K(k(a b)^{-1}h(a,b)[\psi(b)^{-1}k(a)]k(b)).
}$$

Thus $ h'(a,b) = k(a b)^{-1}h(a,b)[\psi(b)^{-1}k(a)]k(b),$
for appropriate choice of $h'$ - what can change $z'$ up to coboundary -
using the freedom from (i). If we want formula involving $\psi'$
instead than we use $\psi'(a) = \psi(a)Ad_K(k(a))$ to obtain
$k(a b)h'(a,b) = h(a,b)k(b)[\psi'(b)^{-1}k(a)]$.
Using that and previous identities,

$$\array{
k(a b c)h'(a b,c)\psi'(c)^{-1}h'(a,b) 
&=& h(a b,c)k(c)[\psi'(c)^{-1}k(a b)]\psi'(c)^{-1}h'(a,b) \\
&=& h(a b,c)k(c)\psi'(c)^{-1}k(a b)h'(a,b) \\
&=& h(a b,c)k(c)\psi'(c)^{-1}h(a,b)k(b)[\psi'(b)^{-1}k(a)] \\
&=& h(a b,c)[\psi(c)^{-1}h(a,b)]k(c)\psi'(c)^{-1}k(b)[\psi'(b)^{-1}k(a)] \\
&=& h(a,b c)h(b,c)z(a,b,c)k(c)
    [\psi'(c)^{-1}k(b)][\psi'(c)^{-1}\psi'(b)^{-1}k(a)] \\
&=& h(a,b c)h(b,c)k(c)[\psi'(c)^{-1}k(b)]
    [\psi'(c)^{-1}\psi'(b)^{-1}k(a)]z(a,b,c) \\
&=& h(a,b c)k(b c)h'(b,c)[\psi'(c)^{-1}\psi'(b)^{-1}k(a)]z(a,b,c) \\
&=& h(a,b c)k(b c)h'(b,c)h'(b,c)^{-1}[\psi'(b c)^{-1}k(a)]h'(b,c)z(a,b,c)\\
&=& h(a,b c)k(b c)[\psi'(b c)^{-1}k(a)]h'(b,c)z(a,b,c)\\
&=& k(a b c)h'(a,b c)h'(b,c)z(a,b,c) 
}$$

for all $a,b,c \in B$. Thus $h'(a b,c)\psi'(c)^{-1}h'(a,b) = h'(a,b c)h'(b,c)z(a,b,c)$ i.e.
our choice of $h'$ insured no change in $z$. Of course that means
that in arbitrary choice of $h'$
we do not miss more than a coboundary by (i).

**Corollary.** A given homomorphism
$\theta : B \times B \rightarrow Aut(K)/Int(K)$
is associated to some extension of $B$ by $K$ iff $z$ is
a 3-coboundary. 

*Proof.* Indeed, if $\theta$ is associated to an extension,
then we know that there is an isomorphism of the extension with
a cross product given by some cocycle $\chi$ and
some automorphism $\psi$ such that $[\psi] = \theta$. But using
the identification, $\chi = h$ for that particular choice
of $\psi$, so that $z = 1$. By the proposition, every
other $z$ obtained from $\theta$ is in the same cohomology class,
thus every such $z$ is a coboundary. Conversely, if $z$ is
a coboundary, then by the proposition, we can change it to $z = 1$,
and then we have all the conditions for a cross product
extension satisfied.

### $n$POV

One may regard the above from the [[nPOV]] as a special case of the way cocycles in the general notion of [[cohomology]] classify their [[homotopy fiber]]s. More on this is at

* [[group cohomology]]

* [[nonabelian group cohomology]].


## Literature

* [[Samuel Eilenberg]], [[Saunders MacLane]], Cohomology theory in abstract groups. II. Group extensions with a non-Abelian kernel.  Ann. of Math. (2)  48,  (1947). 326--341 [jstor](http://www.jstor.org/pss/1969174)

* [[Saunders MacLane]], Cohomology theory in abstract groups. III. Operator 
homomorphisms of kernels.  Ann. of Math. (2)  50,  (1949). 736--761. 

* Lawrence Breen, Th&#233;orie de Schreier sup&#233;rieure, Ann. Sci. &#201;cole Norm. Sup. (4) 25 (1992), no. 5, 465--514 [numdam](http://www.numdam.org/item?id=ASENS_1992_4_25_5_465_0). 

* A. G. Kurosh, Theory of groups 

* Kenneth S. Brown, Cohomology of groups, Graduate Texts in Mathematics, __87__, Springer-Verlag, New York-Berlin, 1982. 

* J-P. Serre, Cohomologie galoisienne, Lecture Notes in Mathematics, 5 (Fifth ed. 1994), Springer-Verlag, MR1324577

* M. Bullejos, A. Cegarra,  A 3-dimensional non-abelian cohomology of groups with applications to homotopy classification of continuous maps Canad. J. Math., vol. 43, (2), 1991, p. 1-32.

* Antonio M. Cegarra, Antonio R. Garz&#243;n, A long exact sequence in non-abelian cohomology, Proc. Int. Conf. Como 1990., Lec. Notes in Math. 1488, Springer 1991.

See also references of Dedecker listed [[zoranskoda:Paul Dedecker|here]]. 

[[!redirects Schreier's theory]]
[[!redirects Schreier theory]]
