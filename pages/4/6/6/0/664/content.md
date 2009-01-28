Preamble to go here.

We denote by $\langle n \rangle$ the set $\{1,2,\ldots, n\}$

A _crossed $n$-cube_, $M$, is a family of  groups,  $\{M_A: A \subseteq  \langle n \rangle\}$,
together with homomorphisms,  $\mu_i :M_A \rightarrow  M_{A-\{i\}}$, for $i \in  \langle n \rangle
, A \subseteq  \langle n \rangle$, and functions, $h:M_{A} \times  M_{B} \rightarrow
M_{A\cup B}$, for $A, B \subseteq  \langle n \rangle$, such that if $^{a}b$ denotes $h(a,b)b$
for  $a \in M_{A}$ and $b \in M_{B}$ with  $A \subseteq  B$, then for  $a,
a^\prime \in M_{A},\, b, b^\prime \in M_{B},\, c \in  M_{C}$  and  $i, j \in
\langle n \rangle$, the following axioms hold:

(1) $\mu_i a = a$ if $a \notin A$

(2) $\mu_i\mu_j a = \mu_j\mu_i a$

(3) $\mu_i h(a,b) = h(\mu_i a,\mu_i b)$

(4) $h(a,b) = h(\mu_i a,b) = h(a,\mu_i b)$ if $i \in A \cap B$ 

(5) $h(a,a^\prime ) = [a,a^\prime ]$

(6) $h(a,b) = h(b,a)^{-1}$

(7) $h(a,b) = 1$ if $a = 1$ or $b = 1$

(8) $h(aa^\prime ,b) = {}^{a}h(a^\prime ,b)h(a,b)$

(9) $h(a,bb^\prime )  =  h(a,b){ }^b h(a,b^\prime )$

(10) ${ }^{a}h(h(a^{-1},b),c)^{c}h(h(c^{-1},a),b)^{b}h(h(b^{-1},c),a)  =  1$

(11) ${ }^{a}h(b,c)  =  h(^{a}b,^{a} c)$  if $A \subseteq  B \cap  C$. 



A morphism of crossed $n$-cubes 

$$\{M_{A}\} \rightarrow \{M^{\prime}_{A}\}$$

is a family of homomorphisms, $\{f_{A}: M_{A} \rightarrow  M^{\prime}_A \,|\, A \subseteq  \langle n \rangle\}$, which commute with the maps, $\mu_i$, and the functions, $h$. 

This gives us a category, $Crs^{n} $, equivalent to that of cat$^{n}$-groups.