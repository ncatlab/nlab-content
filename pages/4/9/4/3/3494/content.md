
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

<img src="http://latex.codecogs.com/gif.latex?\xymatrix{X(13)X(01)\ar[rr]^{X(123)X(01)}%26%26X(23)X(12)X(01)\\X(03)\ar[u]^{X(013)}\ar[rr]_{X(023)}%26%26X(23)X(02)\ar[u]_{X(23)X(012)}}"/>
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
h. c. diagram of type $BG$, the corresponding one object groupoid to $G$.)

(ii)**Vogt's theorem**

If $\mathbf{A}$ is a small category, there is a category $\mathbf{Coh(A,Top)}$
  of h.c. diagrams and homotopy classes of h. c. maps between them.  Moreover
  there is an equivalence of categories

$$\mathbf{Coh(A,Top)} \stackrel{\simeq}{\to} \mathbf{Ho(Top^A)}$$

## References

For [[Rainer Vogt|Vogt]]'s theorem, the original reference is 

* R.M. Vogt, _Homotopy limits and colimits_, Math. Z., 134 (1973) 11-52. 

A generalisation of his theorem using simplicially enriched categories and the [[homotopy coherent nerve]] of such a thing, is to be found in

* J.-M. Cordier and T. Porter, _Vogt's Theorem on Categories of Homotopy Coherent Diagrams_, 
Math. Proc. Camb. Phil. Soc. 100 (1986) pp. 65-90.

(WORK IN PROGRESS: MORE TO COME!)