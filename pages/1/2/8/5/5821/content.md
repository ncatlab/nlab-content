# Crossed G-algebra
* table of contents
{: toc}

##Idea

(Here $G$ will be a group (a discrete one for the moment).)

A crossed $G$-algebra is a type of $G$-[[graded algebra]], with an inner product and a 'crossed' or 'twisted' multiplication. They arise as the analogues of [[Frobenius algebras]] for 2d-[[HQFTs]], [[equivariant TQFTs]] and in slight generality in the study of symmetries of singularities.  They were introduced by [[Turaev]] in 1998. The generalised structures have been studied by [[R. Kaufmann]].


##Nomenclature
[[Greg Moore|Moore]] and [[Graeme Segal|Segal]] (see references below) do not like the term 'crossed algebra' and suggest the alternative name 'Turaev algebra'.


##Definitions:

We will lead up to the definition of crossed $G$-algebra through various stages.

We need a particular form of [[graded algebra]] in which the summands are projective modules, so we give that form first.

###Graded $G$-algebra

A **graded $G$-algebra** or **$G$-algebra** over a field (or more generally a commutative ring), $\mathbb{k}$ is an associative algebra, $L$, over $\mathbb{k}$ with a decomposition,

$$L = \bigoplus_{g\in G} L_g,$$ 

as a direct sum of projective $\mathbb{k}$-modules of finite type such that

(i) $L_g L_h \subseteq L_{gh}$ for any $g,h \in G$ 
(so, if $\ell_1$ is graded $g$, and $\ell_2$ is graded $h$, then $\ell_1\ell_2$ is graded $gh$),

and 

(ii) $L$ has a unit $1 = 1_L\in L_1$ for 1, the identity element of $G$.


###Example:###

(i)  The [[group algebra]], $\mathbb{k}[G]$, has an obvious $G$-algebra structure in which each summand of the decomposition is free of dimension 1. 

(ii)  For any associatve $\mathbb{k}$-algebra, $A$, the algebra,   $A[G]= A\otimes_\mathbb{k}\mathbb{k}[G]$, is also $G$-algebra.  Multiplication in $A[G]$ is given by $(ag)(bh) = (ab)(gh)$ for $a,b \in A$, $g,h \in G$, in the obvious notation.

(iii) If $G$ is the trivial group, then a $G$-graded algebra is just an algebra (of finite type), of course.


###Frobenius $G$-algebra

A **Frobenius $G$-algebra** is a $G$-algebra, $L$, together with a symmetric $\mathbb{k}$-bilinear form,

$$\rho : L\otimes L \to \mathbb{k}$$

such that 

(i)  $\rho(L_g\otimes L_h) = 0$ if $h \neq g^{-1}$;

(ii) the restriction of $\rho$ to $L_g \otimes L_{g^{-1}}$ is non-degenerate for each $g\in G$;

and

(iii)  $\rho(ab,c) = \rho(a,bc)$ for any $a,b,c \in L$.

\

We note that (ii) implies that $L_{g^{-1}} \cong  L_g^*$, the dual of $L_g$.



###Examples continued:
  
(i) The group algebra, $L = \mathbb{k}[G]$, is a Frobenius $G$-algebra with $\rho(g,h) = 1$ if $gh = 1$, and 0 otherwise, and then extending linearly. (Here we write $g$ both for the element of $G$ labelling the summand $L_g$, and the basis element generating that summand.)

(iii) For $G$ trivial, a Frobenius 1-algebra is a [[Frobenius algebra]].

###Crossed $G$-algebra

Finally the notion of  crossed $G$-algebra combines the above with an action of $G$ on $L$, explicitly:

A **crossed $G$-algebra** over $\mathbb{k}$ is a Frobenius $G$-algebra, $L$, over $\mathbb{k}$ together with a group homomorphism,

$$\varphi: G \to Aut(L)$$

satisfying:

(i) if $g\in G$ and we write $\varphi_g = \varphi(g)$ for the corresponding automorphism of $L$, then $\varphi_g$ preserves $\rho$, (i.e., $\rho(\varphi_ga,\varphi_gb) = \rho(a,b)$) and 

$$\varphi_g(L_h) \subseteq L_{ghg^{-1}}$$

for all $h\in G$;

(ii) $\varphi_g|_{L_g} = id$ for all $g\in G$;

(iii) (twisted or crossed commutativity) for any $g,h \in G$, $a\in L_g$, $b\in L_h$, $\varphi_h(a)b = ba$;

(iv) for any $g,h \in G$ and $c \in L_{ghg^{-1}h^{-1}}$,

$$Tr(c\varphi_h : L_g \to L_g) = Tr(\varphi_{g^{-1}}c : L_h \to L_h),$$

where $Tr$ denotes the $\mathbb{k}$-valued trace of the endomorphism. (The homomorphism $c\varphi_h$ sends $a\in L_g$ to $c\varphi_h(a) \in L_g$, whilst $(\varphi_{g^{-1}}c)(b) = \varphi_{g^{-1}}(cb)$ for $c \in L_h$. This is sometimes called the 'torus condition'.)

###Note:

a) We note that the usage of terms differs between Turaev's book (2010) and here, as we have taken 'crossed $G$-algebra' to include the Frobenius condition. We thus follow Turaev's original convention (preprint 1999) in this.  

b) The useful terminology 'twisted sector' in a crossed $G$-algebra refers to a summand, $L_g$, for and index, $g$, which is  not the identity element of $G$, of course, then $L_1$ is called  the 'untwisted sector'


##Operations on crossed $G$-algebras

(To be added)

##Related notions

* crossed $C$-algebra for a [[crossed module]] of groups;

*[[twisted G-algebra]]

##References

* V. [[Turaev]],  _Homotopy Quantum Field Theory_ ,
EMS Tracts in Math.10, European Math. Soc. Publ. House, Zurich 2010. (for the detailed development and the links with low dimensional topology and [[HQFT]]s).

* [[Greg Moore]], [[Graeme Segal]], _D-branes and K-theory in 2D topological field theory_ ([arXiv hep-th 0609042](http://arxiv.org/abs/hep-th/0609042))





[[!redirects crossed G-algebras]]
[[!redirects Turaev algebra]]