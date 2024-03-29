#Idea#

* A [[crossed module]] is the 'algebraic core' of a $\cat^1$-[[cat-1-group|group]], in as much as within a $\cat^1$-group we can find a crossed module in a simple way from which the whole of the $\cat^1$-group in all its glory can be reconstructed.

* A [[crossed square]] is similarly the 'algebraic core' of a $\cat^2$[[cat-2-group|group]].

* A _crossed $n$-cube_ should be the 'algebraic core' of a $\cat^n$-[[cat-n-group|group]].

A crossed square in the Guin-Valery Loday specification has quite a few axioms, many more than those for a crossed module. Does that mean that crossed $n$-cubes will be defined with a very large number of axioms (perhaps dependent on $n$)? No (unless you think that 11 is large!)

Finally a particular example of a [[crossed square]] is given by a group with two [[normal subgroup]]s, and their intersection together with the commutator map.  It would be appropriate if a group together with $n$ normal subgroups, all the  intersections and all the commutator maps, formed an example of a crossed $n$-cube.  It does.  The axioms below govern the $h$-maps, by using analogues of the relationships between commutator maps in such a $n$-cube of inclusions of intersections.

The result (definition due to Graham Ellis and Richard Steiner, reference below) is a set of 11 axioms. That is all, and these objects model all homotopy $(n+1)$-[[homotopy n-type|types]].


#Definition#

We denote by $\langle n \rangle$ the set $\{1,2,\ldots, n\}$.

A _crossed $n$-cube_, $M$, is a family of  groups,  $\{M_A: A \subseteq  \langle n \rangle\}$,
together with homomorphisms,  $\mu_i :M_A \rightarrow  M_{A-\{i\}}$, for $i \in  \langle n \rangle
, A \subseteq  \langle n \rangle$, and functions, $h:M_{A} \times  M_{B} \rightarrow
M_{A\cup B}$, for $A, B \subseteq  \langle n \rangle$, such that if $^{a}b$ denotes $h(a,b)b$
for  $a \in M_{A}$ and $b \in M_{B}$ with  $A \subseteq  B$, then for  $a,
a^\prime \in M_{A},\, b, b^\prime \in M_{B},\, c \in  M_{C}$  and  $i, j \in
\langle n \rangle$, the following axioms hold:

1. $\mu_i a = a$ if $i \notin A$

1. $\mu_i\mu_j a = \mu_j\mu_i a$

1. $\mu_i h(a,b) = h(\mu_i a,\mu_i b)$

1. $h(a,b) = h(\mu_i a,b) = h(a,\mu_i b)$ if $i \in A \cap B$ 

1. $h(a,a^\prime ) = [a,a^\prime ]$

1. $h(a,b) = h(b,a)^{-1}$

1. $h(a,b) = 1$ if $a = 1$ or $b = 1$

1. $h(aa^\prime ,b) = {}^{a}h(a^\prime ,b)h(a,b)$

1. $h(a,bb^\prime )  =  h(a,b){ }^b h(a,b^\prime )$

1. ${ }^{a}h(h(a^{-1},b),c)^{c}h(h(c^{-1},a),b)^{b}h(h(b^{-1},c),a)  =  1$

1. ${ }^{a}h(b,c)  =  h(^{a}b,^{a} c)$  if $A \subseteq  B \cap  C$. 



A morphism of crossed $n$-cubes 
$$f :\{M_{A}\} \rightarrow \{M^{\prime}_{A}\}$$
is a family of homomorphisms, $\{f_{A}: M_{A} \rightarrow  M^{\prime}_A \,|\, A \subseteq  \langle n \rangle\}$, which commute with the maps, $\mu_i$, and the functions, $h$. 

This gives us a category, $Crs^{n} $, equivalent to that of $\cat^n$-[[cat-n-group|groups]].

# Homotopical example#

 The  _fundamental crossed $n$-cube of groups functor_  $\Pi '$ is defined from  $n$-cubes of pointed spaces to crossed $n$-cubes of
groups:  $\Pi  'X_{*}$   is simply  the crossed $n$-cube of
groups equivalent to the cat$^n$-group  $\Pi X_{*}$. It is easier
to identify  $\Pi '$  in classical terms in the case $X_{*}$   is
the $n$-cube  of spaces arising from a pointed  $(n +
1)$-ad  $\mathcal{X}  = (X;X_1,\ldots ,X_n)$. That is, let  $X_{
\langle n \rangle } = X$  and for  $A$  properly contained in
$\langle n \rangle$ let   $X_A = \bigcap _{i \not\in A}  X_i$. Then
$M = \Pi '\mathcal{X}$   is given as follows (Ellis and Steiner, 1987):
$M_{\emptyset}  = \pi_1(X_\emptyset )$; if  $A = {i_1,\ldots ,i_r}$,
in the right order, then $M$ is the homotopy  $(r + 1)$-ad group
$\pi _{r+1}(X _A;X_A \cap X_{i_1} ,\ldots ,X_A   \cap  X_{i_r} )$;
the maps $\mu$ are given by the usual boundary maps;  the
$h$-functions are  given by generalised Whitehead products.  

Note
that whereas these separate elements of structure had all been
considered previously, the aim of this theory is to consider the
whole structure, despite its apparent complications. The equivalence of categories is a convincing reason for supposing that the axioms for a crossed $n$-cube of groups are a complete axiomatisation of this homotopical structure, as was not previously known. 

# Algebraic example#
Let us put a bit of flesh on the example given in the introduction.  Suppose that  $G$ is a group and $N_1, N_2, .., N_n$ are $n$-[[normal subgroup]]s of $G$ (there may be repeats).

Now define for $A \subseteq  \langle n \rangle$, $M_A = \bigcap\{N_i\mid i \in A\}$, and for $A\in M_A$, $b\in M_B$, $h(a,b) = [a,b]$, the [[commutator]] of $a$ and $b$ in $G$.  The result is a crossed $n$-cube (sometimes called the _inclusion crossed $n$-cube_ determined by the normal $n$-ad of subgroups).


#Simplicial example#
If instead of a space you start with a [[simplicial group]] $G$, as model for a connected homotopy type, then there is a crossed $n$-cube generalising the [[crossed square]] given in terms of the [[Moore complex]].


#References#

* [[G. J. Ellis]] and [[R. Steiner]], _Higher dimensional crossed modules and the homotopy groups of 
(n + 1)-ads_, J. Pure Appl. Alg., 46, (1987), 117&#8211;136.

* [[Ronnie Brown|R. Brown]] _Computing homotopy types using crossed n-cubes of groups_, Adams  Memorial Symposium on
Algebraic Topology}, Vol 1, edited N. Ray and G  Walker,
Cambridge University Press, 1992, 187-210.  [Here is a link to a revised version with hyperref](http://groupoids.org.uk/pdffiles/ADAMSVT.pdf)

*  [[Ronnie Brown|R. Brown]] _Homotopical excision (work to be done!)_ Presentation at Higher Structures Lisbon, July 2017. [RB's preprints](http://groupoids.org.uk/brownpr.html)