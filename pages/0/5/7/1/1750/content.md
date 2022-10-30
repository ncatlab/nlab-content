[[!redirects ?]]
Recall the notion of a [[Grothendieck fibration]].
It [[Grothendieck fibration|generalizes]] to the notion of a fibration in a 2-category using [[Grothendieck fibration|Grothendieck fibrations]] themselves, using [[generalized element|generalized elements]]. We here give an alternative, yet equivalent, 2-categorical definition, trying to explain how it specializes to Grothendieck fibrations. The definition is due to the Australian school, probably Ross Street, and is recalled in Mark Weber's paper _Yoneda Structure from 2-toposes_, the main source for this page.

Fix a 2-category $\mathcal{K}$. For any two morphisms
$f: A \to C$ and $c: B \to C$, let $f/g$ be the corresponding [[comma object]] and let $f/=g$ be their [[pullback]].

A morphism $p:A \to B$ in it is a **fibration** when for all morphism $f: X \to B$, the canonical map $i: f/=p \to f/p$ has a [[right adjoint]] in $\mathcal{K} / X$.

The purpose of this page is the following result:

+-- {: .standout #ElemFibSpecializesToCat }

When $\mathcal{K}$ is [[Cat]], fibrations in this sense are precisely [[Grothendieck fibration|Grothendieck fibrations]].

=--

This surely needs some unfolding. First, recall that the
2-category $Cat/X$ has objects the functors $C \to X$, as morphisms the commuting triangles
$$\array{C & \stackrel{h}{\to} & C' \\ & f \searrow \swarrow g &  \\  & X,  & }$$
and as 2-cells the natural transformations $\alpha : h_1 \to h_2$ such that $g\alpha = id_f$.

Next, recall that for $f: X \to B$ and $p: A \to B$ the comma object $f/p$ has objects the triples $(x, a, \alpha)$, with $\alpha: f(x) \to p(a)$. We will abbreviate the latter as just $\alpha$.

The pullback $f/=p$ has objects the pairs $(x, a)$ with 
$f(x) = p(a)$, and 
the above mentioned canonical morphism $f/=p \to f/p$ is simply the inclusion functor of identity maps $id: f(x) \to p(a)$. 

Somewhat unprecisely, seeing both categories $f/p$ and $f/=p$ as sitting over $X$ means that functors between those should be the identity on the $x$ component, and natural transformations should have the identity as their $x$ component.

Let us concentrate on the case $X = B$. Then the pullback category $f/=p$ has as objects the pairs $(b, a)$ such that 
$b = p(a)$, i.e., just objects $a$ of $A$. And similarly, its morphisms are just morphisms of $A$.

Assuming a right adjoint $q$ to $i$, $q$ sends a morphism $\alpha: b \to p(a)$ to some object $q(\alpha)$ of $A$, which $i$ then sends to the identity on $pq(\alpha)$, or more exactly the triple $(pq(\alpha), q(\alpha), id_{pq(\alpha)})$.

The counit for the corresponding adjunction has to be a morphism in $f/p$ from the latter to $\alpha$ itself, i.e., a pair $(\epsilon_0, \epsilon_1)$ making the square
$$\array{pq(\alpha) & \stackrel{id}{\to} & pq(\alpha) \\
\epsilon_1 \downarrow & & \downarrow p(\epsilon_0) \\
b & \stackrel{\alpha}{\to} & p(a)}$$
commute.

But, as a 2-cell in $Cat/B$, this pair must have $\epsilon_1 = id$, hence the counit is actually providing an arrow $\epsilon_0$ in $A$, sent to $\alpha$ by $p$.

Moreover, its universal property tells us that for any other morphism in $f/p$ from some $i(a')$ to our $\alpha$, i.e., for any $a'$ and any pair $(h,k)$ making the square
$$\array{p(a') & \stackrel{id}{\to} & p(a') \\
k \downarrow & & \downarrow p(h) \\
b & \stackrel{\alpha}{\to} & p(a)}$$
commute, there is a unique map $m: a' \to q(\alpha)$ in $A$ such that the above square factors in $f/p$ as
$$\array{
p(a') & \stackrel{id}{\to} & p(a') \\
p(m) \downarrow &  & \downarrow p(m) \\
pq(\alpha) & \stackrel{id}{\to} & pq(\alpha) \\
id \downarrow & & \downarrow p(\epsilon_0) \\
b & \stackrel{\alpha}{\to} & a.}$$

In other words, the universal property provides a unique $m$ such that $\epsilon_0 m = h$ and $p(m) = k$, which exactly asserts that $\epsilon_0$ is [[Grothendieck fibration|cartesian]]. 

Hence $p$ is a Grothendieck fibration. The other implication remains to be proved, but not today.
