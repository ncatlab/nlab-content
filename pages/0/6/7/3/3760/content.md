## Idea## 



In try to study a group $G$, one way to proceed is to 

* look for a set of generating elements;

* look for 'relations' between those elements.

The problem is partially how one is to interpret this second part. To do this we need to look at words in the generators and hence at the [[free group]] on the set of generators.

For example, if we have the symmetric group $S_3$, or, isomorphically, the dihedral group (of symmetries of a triangle) which we will call $D_3$ (following the geometric convention (see the Wikipedia article on dihedral groups), then we have 6 elements, and they are all able to be got as products of a transposition and a three cycle (or alternatively as a reflection and a rotation).  If we call the three cycle $a$ and the transposition $b$, we have

$$S_3=\{1,a,a^2,b,ab,a^2b\}.$$

What about the other words: $ba$ for instance.  If one calculates $b a$ in $S_3$ and then looks up what you get you have $ba = a^2b$, so that there is a relation between these two words. This however is not all. What about $b a b a a b a a  a b b a a $ that is a word in the $a$s and $b$s so should represent something in $S_3$, in fact if you thing in the geometric version of $D_3$ you can pick up  a triangle and interpret that word as a list of instructions for moving the triangle. You then find out what this word is out of the 6 possibles. 

For a presentation, you give a set of generators $X$, so there will be an epimorphism from $F(X)$ to $G$, and then you try to find a description for the kernel of that epimorphism, which we will denote by $N$.  The description of this normal subgroup $N$ is as the [[normal closure]] of a set $R$ of relations, i.e. words in the generators or, equally validly, elements in the free group on $X$.


##Definition##
A  **presentation** of a group $G$ is a pair of sets, written $\langle X; R\rangle$ such that $F=\langle X\rangle$ is the [[free group]] on the set of letters $X$ and $N$ the [[normal subgroup|normal closure]] of the set of relators $R$, together with a specified isomorphism from $F/N$ to $G$.

The specified isomorphism is often omitted, as usually the set $X$ of generators is chosen as a subset of the set of elements of $G$.  In this case, but the universal properties of free groups and quotients, there is a unique map $F\to G$ which restricts to the inclusion of $X$, and thereby at most one map $F/N \to G$ which does so; this map is then the one asserted to be an isomorphism.

Sometimes it is convenient to proceed otherwise, however, and to give a specific function from a set $X$ to the set of elements of $G$.  This function then induces a group homomorphism from $F=\langle X\rangle$ to $G$, and if this is a surjection, then we can find some $N$ (generators for its kernel) to produce a presentation of $G$.

##Examples##

*  $G$ a cyclic group of order $n$ has presentation $\langle a ; a^n\rangle$.

*  $S_3$ has a presentation $\langle a,b ; a^3, b^2,(ab)^2 \rangle$.

##Discussion##

*  'Relations' and 'relators': In the discussion of $S_3$ above we had a **relation** $b a = a^2b$. so we are relating two words of $F(X)$. It is often the case that instead of relations we use **relators**, in other words a relation of form $r = 1$ where $r$ is a word in the generators. In the example $ b a = a^2b$ can be easily shown to imply and be implied by $ a b a b = 1$.


*  Given a group presentation as above, we have a 
short exact sequence,

$$1\to N \to F \to G \to 1,$$ 

where $F = F(X)$, the free group on the set $X$, $R$ is a 
subset of $F$ and $N = N(R)$ is the normal closure in $F$ of the set $R$.  The group 
$F$ acts on $N$ by conjugation: ${}^uc = ucu^{-1}, for  c\in N, u \in F$ and the 
elements of $N$ are words in the conjugates of the elements of $R$:

$$c = {}^{u_1}(r_1^{\varepsilon_1}){}^{u_2}(r_2^{\varepsilon_2})\ldots 
{}^{u_n}(r_n^{\varepsilon_n})$$

where each $\varepsilon_i$ is $ + 1$ or $ - 1$.  One also says such elements are **consequences** of 
$R$.  Heuristically an [[identity among the relations]] of $\mathcal{P}$ is such an element $c$ 
which equals 1. 
