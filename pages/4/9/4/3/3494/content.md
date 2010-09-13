
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

First a vague version:

A homotopy coherent diagram is a diagram of objects in a category which has a notion of homotopy, where commutativity is replaced by explicit homotopies, those homotopies are to then be coherently linked by higher homotopies ... and so on.

The idea perhaps intuitively makes sense but the management of the interactions between the various levels of homotopy requires care. The ideas were handled in various ways , but we will concentrate on approaches linked to the initial work of [[Michael Boardman]] and [[Rainer Vogt]] and then developed further by [[Jean-Marc Cordier]] and [[Tim Porter]]. 

We will often use h.c. as an abbreviation for ''homotopy coherent''.




##Examples 

**h.c. diagrams in a category with [[cylinder functor]], denoted $-\times I$**

1.  A diagram indexed by the small category, $[2]$.

<img src="http://latex.codecogs.com/gif.latex?\xymatrix{%26X(1)\ar[dr]^{X(12)}%26\\X(0)\ar[rr]_{\hspace{.5cm}X(02)}\ar[ur]^{X(01)}_{X(012)}%26%26X(2)}"/>

is h.c. if there is specified a homotopy 

$$X(012) : X(0)\times I \to X(2),$$

$$X(012) : X(02) \simeq X(12)X(01).$$

1. For a diagram indexed by $[3]$: Draw a 3-simplex, marking the vertices
$X(0)$, \ldots, $X(3)$, the edges $X(ij)$, etc., the faces $X(ijk)$, etc.  The 
homotopies $X(ijk)$ fit together to make the sides of a square

$$
 \begin{matrix}
  X(1 3)X(0 1)&\xrightarrow{X(1 2 3)X(0 1)}&X(2 3)X(1 2)X(0 1)\\
  \mathllap{X(0 1 3)}\left\uparrow\space{30}{20}{0}\right.& &\left.\space{30}{20}{0}\right\uparrow\mathrlap{X(2 3) X(0 1 2)}\\
  X(0 3)&\xrightarrow[\qquad X(0 2 3)\qquad]{\quad}&X(2 3)X(0 2)
 \end{matrix}
$$
and the
diagram is made h.c. by specifying a second level homotopy 

$$X(0123) : X(0)\times I^2\to X(3)$$

filling this square, in the sense that restricting to each side of the square in the double homotopy gives the correspondingly labelled homotopy from the diagram.



These can be continued for larger $[n]$, and the results glued together to
make larger h.c. diagrams.  Of course, this is not how it is done, but it
provides some understanding of the basic idea.  


Before giving the detailed definition, let us look at some results which relate to why h.c. is useful.

## Results

(i) If $X : \mathbf{A}\to \mathbf{Top}$ is a commutative diagram and we
replace some of the $X(a)$ by homotopy equivalent $Y(a)$ with specified
homotopy equivalence data:

$$f(a) : X(a) \to Y(a), \quad g(a) : Y(a) \to X(a)$$

$$H(a) : g(a)f(a) \simeq Id, \quad K(a) : f(a)g(a) \simeq Id,$$

then we can combine these data into the construction of a h. c. diagram $Y$
based on the objects $Y(a)$ and homotopy coherent maps 

$$f : X\to Y, \quad g : 
Y \to X,  etc.,$$

making $X$ and $Y$ homotopy equivalent as h.c. diagrams.

(This applied to a $G$-space, $X$, shows that if we replace $X$ by 
a homotopy equivalent $Y$, then $Y$ will be a h. c. version of a $G$-space, i.e. a
h. c. diagram of shape $BG$, the corresponding one object groupoid to $G$.)

(ii)**Vogt's theorem**

If $\mathbf{A}$ is a small category, there is a category $\mathbf{Coh(A,Top)}$
  of h.c. diagrams and homotopy classes of h. c. maps between them.  Moreover
  there is an equivalence of categories

$$\mathbf{Coh(A,Top)} \stackrel{\simeq}{\to} \mathbf{Ho(Top^A)}.$$



(iii) Cordier (1980), 

Given ${\mathbb{A}}$, a small category, then the $SSet$-category
${S(\mathbb{A})}$ (for the definition see [[homotopy coherent nerve]]) is such that a
h.c. diagram of shape ${\mathbb{A}}$ in $Top$ is given precisely by an 
$SSet$-functor

$$F : {S(\mathbb{A})} \to Top$$


This suggested the extension of h.c. diagrams to other contexts such as a
general locally Kan $SSet$-category, $\mathcal{B}$ and suggests the definition of homotopy coherent diagram in a $\mathcal{S}$-category and thus a [[homotopy coherent nerve]] of an $SSet$-category.

To understand simple h.c. diagrams and thus the h.c. simplicial nerve $N(\mathcal{B})$, we  unpack the definition of homotopy coherence, for conveneince, repeating some points made in [[homotopy coherent nerve]].



The first thing to note is that for any $n$ and $0\leq i\lt j\leq n$, $S[n](i,j) \cong \Delta[1]^{j-i-1}$, the $(j-i-1)$-cube given by the product of $j-i-1 $ copies of $\Delta[1]$.  Thus we can reduce the higher homotopy data to being just that, maps from higher dimensional cubes.

Next some notation:

Given simplicial maps

$$f_1: K_1 \to \mathcal{B}(x,y),$$

$$f_2: K_2 \to \mathcal{B}(y,z),$$

we will denote the composite

$$K_1 \times K_2 \to \mathcal{B}(x,y)\times \mathcal{B}(y,z) \stackrel{c}{\to} \mathcal{B}(x,z)$$

just by $f_2.f_1$ or $f_2f_1$.  (We already have seen this in the h.c. diagram above for 
$\mathbb{A} = [3]$.  $X(123)X(01)$ is actually $X(123)(I \times X(01) )$, whilst $X(23)X(012)$ is exactly what it states.)

The original definition of Vogt from 1973 is essentially the following 

##Definition (original form)##

Suppose now that we have the h.c. diagram $F : S(\mathbb{A}) \to \mathcal{B}$.  This is specified by assignments:

* to each object $a$ of $\mathbb{A}$, it assigns an object $F(a)$ of $\mathcal{B}$;

* for each string of composable maps in $\mathbb{A}$,

$$\sigma = (f_0, \ldots, f_n)$$

starting at $a$ and ending at $b$, a simplicial map

$$F(\sigma) : S(\mathbb{A})(0,n+1) \to \mathcal{B}(F(a), F(b)),$$

that is, a higher homotopy

$$F(\sigma) : \Delta[1]^n \to \mathcal{B}(F(a), F(b)),$$

such that

(i) if $f_0 = id$, $F(\sigma) = F(\partial_0\sigma)(proj \times \Delta[1]^{n-1})$

(ii) if $f_i = id$, $0\lt i \lt n$

$$F(\sigma) = F(\partial_i\sigma(.(I^i \times m \times I^{n-i}),$$ 

where $m : I^2 \to I$ is the multiplicative structure on $I = \Delta[1]$ by the 'max' function on $\{0,1\}$;

(iii) if $f_n = id$, $F(\sigma) = F(\partial_n \sigma)$;

(iv)$_{i}$  $F(\sigma)|(I^{i-1}\times \{0\} \times I^{n-i}) = F(\partial_i\sigma), 1 \leq i \leq n-1$;

(v)$_{i}$  $F(\sigma)|( I^{i-1}\times \{1\} \times I^{n-i}) = F(\sigma^\prime_i) . F(\sigma_i)$, where $\sigma_i = (f_0, \ldots, f_{i-1}$ 
and $\sigma^\prime = (f_i, \ldots, f_n)$.  We have used $\partial_i$ for the face operators in the nerve of $\mathbb{A}$.


This original form can be very useful for checking (bare hands!) within an application that a diagram <i>is</i> h.c., although the $SSet$-functor approach is for many uses more compact and maniable and allows functorial constructions more easily. The link with the [[bar construction]] and [[comonadic resloution]] approaches give suggestive links to interpretation of cohomology classes.

(To come: morphisms between h.c. diagrams)
## References

For [[Rainer Vogt|Vogt]]'s theorem, the original reference is 

* R.M. Vogt, _Homotopy limits and colimits_, Math. Z., 134 (1973) 11-52. 

A generalisation of his theorem using simplicially enriched categories and the [[homotopy coherent nerve]] of such a thing, is to be found in

* J.-M. Cordier and T. Porter, _Vogt's Theorem on Categories of Homotopy Coherent Diagrams_, 
Math. Proc. Camb. Phil. Soc. 100 (1986) pp. 65-90.


A neat application to changing objects in diagrams within a homotopy type can be found in

* J.-M. Cordier and T. Porter, _Maps between homotopy coherent diagrams_, Top. and its Appls., 
28, (1988), 255 &#8211; 275.

A summary of homotopy coherence can be found in Chapter 5 of 

* K. H. Kamps and T. Porter, _Abstract Homotopy and Simple Homotopy Theory_ ([GoogleBooks](http://books.google.de/books?id=7JYKxInRMdAC&dq=Porter+Kamps&printsec=frontcover&source=bl&ots=uuyl_tIjs4&sig=Lt8I92xQBZ4DNKVXD0x76WkcxCE&hl=de&sa=X&oi=book_result&resnum=3&ct=result#PPP1,M1))


and in chapter 10 of the [[Menagerie]].


(WORK IN PROGRESS: MORE TO COME!)