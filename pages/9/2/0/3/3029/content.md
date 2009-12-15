(For now we will put emphasis on the general case i.e. nonabelian group extensions, later we plan a separate entry on abelian group extensions.) 

#Definition

We say that a sequence of groups

$$ 1\to K
\overset{i}\to G\overset{p}\to B\to 1$$

is **exact** if $i$ is [[monomorphism]], $p$ an [[epimorphism]] and $Ker(p)=Im(i)$. If $K$ and $B$ are given groups, then any exact sequence of the form above is called an extension of $B$ by $K$ (some say conversely of $K$ by $B$). Letters are here chosen to suggest that $B$ is a base to which $G$ projects and $K$ is the *kernel* of $i$ and for $G$ itself we often say that it is a group extension of $B$ by $K$. 

If $K$ is abelian then we write $0$ instead of $1$ at the left start of the sequence, and if $B$ is exact we do the same at the right-hand end of the sequence. 

We say that two group extensions $1\to K\stackrel{i}\to G\stackrel{p}\to B\to 1$ and $1\to K\stackrel{i'}\to G'\stackrel{p'}\to B\to 1$ are equivalent if there is an isomorphisms $\gamma:G\to G'$ such that 
$\gamma\circ i = i'$ and $p=p'\circ \gamma$. In other words, there is a
commutative diagram

$$\array{
1\to &K&\stackrel{i}\to &G&\stackrel{p}\to &B&\to 1\\
&\downarrow\mathrlap{=}&&\downarrow\mathrlap\gamma&&\downarrow\mathrlap=&\\
1\to &K&\stackrel{i'}\to &G'&\stackrel{p'}\to& B&\to 1
}$$

#Scheier's theory traditional way

[[Otto Schreier]] (1926) and Eilenberg-Mac Lane (late 1940-s) developed a theory of classification of nonabelian extensions of abstract groups leading to the low dimensional nonabelian group cohomology. This is sometimes called **Schreier's theory** of nonabelian group extensions.

The traditional Schreier-Mac Lane way to obtain nonabelian group 2-cocycle
from a group extension as above starts with choosing a set-theoretic section of $p:G\to B$. 

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
[(a,e)(b,e)](c,e) = (ab, \chi(a,b))(c,e) =
 (abc, \chi(ab,c) \psi(c)^{-1}(\chi(a,b))).
$$
From the other side, this has to be the same, by associativity, to
$$
(a,e)[(b,e)(c,e)] = (a,e)(bc,\chi(b,c)) = (abc,\chi(a,bc)\chi(b,c))
$$
where we took into account that expressions like $[\psi^{-1}(b)(e)] = e$,
because $\psi(b)$ is an *automorphism* for each $b \in B$.

 Comparing the expressions above we obtain
\[\label{psi1}
 \chi(ab,c)\psi(c)^{-1}(\chi(a,b)) = \chi(a,bc)\chi(b,c),
    \forall a,b,c \in B.
\]

If the pair $(\chi,\psi)$ is constructed as above, then

$$\array{
\psi(a)\psi(b)k & = & \phi(\sigma(a))\phi(\sigma(b))k \\
        & = & \sigma(a)\sigma(b)k\sigma(b)^{-1}\sigma(a)^{-1} \\
        & = & \sigma(ab)\chi(a,b)k\chi(a,b)^{-1}\sigma(ab)^{-1} \\
        & = & \psi(ab) In_K(\chi(a,b)) k,
}$$

where $In_K$ is the canonical map $K \rightarrow Int(K)$.

Thus we obtain the relation
\[\label{psi2}
\psi(a)\psi(b) = \psi(ab) In_K(\chi(a,b))
\]

+-- {: .un_defn}
###### Definition
Let $B$ and $K$ be two groups.
Let $\chi: B \times B \rightarrow K$
and $\psi : B \rightarrow Aut(K)$ satisfy (eq:psi1)
and (eq:psi2). Then we call that the family
$\{\chi(b_1,b_2)| b_1,b_2 \in B\}$
is a factor system (This term is due Schreier(1924))
or a **nonabelian group 2-cocycle with automorphisms**, and
the family $\{\psi(b) | b \in B \}$ -- a system of automorphisms
=--

A 2-cocycle $\chi$ is **counital** if $\chi(b,e) = \chi(e,b) = e$, for all $b \in B$.

If $K$ is commutative, then $\psi$ is always a homomorphism (cf. (eq:psi2)). Then $K$ is a right $B$-module through $\psi(-)^{-1}$. That justifies the sometimes used term "(right) cocycle $B$-module" for $(K,\psi,\chi)$. If $\psi$ is trivial ($\psi(b) = Id_K, \forall b \in B$)
then the cocycle condition (eq:psi1) becomes
\begin{equation}
\chi(ab,c)\chi(a,b) = \chi(a,bc)\chi(b,c). 
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
\psi(a)\psi(e)k & =&
     \psi(a)In_K(\chi(a,e))k \\
& = &\psi(a)\chi(a,e)k\chi(a,e)^{-1}
}$$
where we used \eqref{psi2}.

Thus $In_K(\chi(a,e)) = \psi(e)$ and therefore it does not
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
=(b_1b_2,e)(e,\chi(e,e)^{-1}\chi(b_1,b_2)k)\\
&\Leftrightarrow& (b_1b_2,\chi(b_1,b_2))(e,\chi(e,e)^{-1}k) = (b_1b_2,\chi(b_1b_2,e)\chi(e,e)^{-1}\chi(b_1,b_2)k)\\
&\Leftrightarrow&
\chi(b_1b_2,e)\psi(e)^{-1}(\chi(b_1,b_2))\chi(e,e)^{-1}k = \chi(b_1b_2,e)\chi(e,e)^{-1}\chi(b_1,b_2)k
}$$

for all $b_1,b_2 \in B$ for all $k \in K$ in all these lines.
The last line is true by (eq:psi1).

Similarly, $\psi' = i_{Aut} \circ \psi$ iff $(b,e)(e,\chi(e,e)^{-1}k) = (e,\chi(e,e)^{-1}\psi(b)k)(b,e)$ for all $b$ and $k$. 

Here the LHS computes as $(b,k)$ using $\chi(b,e) = \chi(e,e)$, and the RHS is 

$$(e,\psi(b)k)(b,e) = (b, \chi(e,b)\psi(b)^{-1}(\chi(e,e)^{-1}\psi(b)(k)))
= (b, k)$$

by (eq:psiac).

#Schreier's theory of extensions modern way

...

#Literature

* S. Eilenberg, S. MacLane, Cohomology theory in abstract groups. II. Group extensions with a non-Abelian kernel.  Ann. of Math. (2)  48,  (1947). 326--341 [jstor](http://www.jstor.org/pss/1969174)

* S. MacLane, Cohomology theory in abstract groups. III. Operator 
homomorphisms of kernels.  Ann. of Math. (2)  50,  (1949). 736--761. 


[[!redirects Schreier's theory]]
