A $2$-group is a [[vertical categorification]] of the idea of [[group]]. 

It is the special case of an [[n-group]] for $n=2$.

# Strict $2$-groups

We will start by looking at strict 2-groups.


##Definition##

A **strict 2-group** is an [[internal category]] in [[Grp]].  Equivalently, it is an internal group object in [[Cat]].

##Expanding the definition##

Copying and adapting from the entry on general internal categories we have:

A [[internal category]] in [[Grp]] is 

* a collection of group homomorphisms of the form
  $$
    C_1 \stackrel{s,t}{\to} C_0 \stackrel{i}{\to} C_1
  $$
such that the composites $s\cdot i$ and $t\cdot i$ are the identity morphisms on $C_0$, and
  such that, writing  $C_1 \times_{t,s} C_1$ for the pullback, 
  $$
    \array{
      C_1 \times_{t,s} C_1 &\to& C_1
      \\
      \downarrow && \downarrow^{t}
      \\
      C_1 &\stackrel{s}{\to}& C_0
    }
  $$
  there is, in addition,  a homomorphism
  $$
     C_1 \times_{t,s} C_1 \stackrel{comp}{\to} C_1
  $$
  "respecting $s$ and $t$";

 * such that the _composition_ $comp$ is associative
   and unital with respect to $i$ "in the obvious way".

##Discussion, examples and Remarks##

* Any such internal category is, in fact, an internal [[groupoid]] in [[Grp]].

*  Perhaps the _simplest example_ of such a structure is a 
[[congruence|congruence relation]] on a group $G$. If $\sim$ is a congruence relation on $G$, then we form the 2-group by setting $C_0 = G$ and $C_1$ to be the group of pairs $(a,b)$ with $a\sim b$.  That this is a group follows from the definition of congruence given in the above reference. The two maps $s$ and $t$ are defined by $s(a,b) = a$, $t(a,b) = b$, whilst $i(a) = (a,a)$. The pullback is a subgroup of $C_1\times C_1$ given by all 'pairs of pairs' $((a,b),(b,c))$ and the composition homomorphism sends such a pair to $(a,c)$.  The other properties are easy to check.

* Any congruence relation corresponds to a normal subgroup, given by those elements $a$ that are congruent to the identity element of $G$, so that $e\sim a$. Likewise given a normal subgroup of $G$ you get a congruence.

* Any _2-group_ corresponds to a [[crossed module]] by the Brown-Spencer theorem (R. Brown and C. Spencer, _G-groupoids, crossed modules and the fundamental groupoid of a 
topological group_, Proc. Kon. Ned. Akad. v. Wet, 79, (1976), 296--302.) The previous entry indicates how to prove that result in a particular case. Here is a bit more detail:

If $(C\stackrel{\delta}{\to}P)$ is a crossed module, the corresponding _2-group_ has $G_0 = P$, $G_1 = C\rtimes P$, the [[semi-direct product]] of $C$ and $P$, using the action of $P$ on $C$, given in the specification of the crossed module. The maps are $s(c,p) = p$, $t(c,p) = \delta(c)\cdot p$, (with the other structure maps left as exercises). 

# Weak $2$-groups

Other forms of _2-group_ exist, in which the key observation is that any strict 2-group as above gives a strict monoidal category with inverses.  It is therefore natural to look at monoidal categories with weak inverses, and these are the general form of 2-group. (To be added, by someone at a later date).