
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{: toc}


## Idea

One can ask whether a nonlinear map between locally convex topological vector spaces is smooth according to various definitions. The definition due to Michal, developed by [[Andree Ehresmann|Bastiani]], is a very general such notion.


## Definition

A map $\Phi:E\rightarrow F$ from a [[locally convex topological vector space]] (lctvs) $E$ into another lctvs $F$ is said to be **Michal-Bastiani smooth** (or **MB-smooth**) if its [[directional derivatives]] of order $k$,

$$ 
D^k\Phi[x](y_1,\ldots,y_k) = \left.\frac{\partial^k}{\partial\lambda_1\cdots\partial\lambda_k}\right|_{\lambda_1=\cdots=\lambda_k=0}\Phi\left(x+\sum^k_{j=1}\lambda_j y_j\right)
$$

exist and the maps $D^k\Phi:E\times E^k\rightarrow F$ are [[jointly continuous map|jointly continuous]] for all $k\in\mathbb{N}$. The notion is due to Michal ([Michal 38](#Michal38),[Michal 40](#Michal40)), and was further developed by ([Bastiani 64](#Bastiani64)).

This notion of smoothness is the one used in [[Milnor]]'s treatment of infinite-dimensional [[Lie groups]] ([Milnor 84](#Milnor)) and Hamilton's expos&#233; of the Nash-Moser [[inverse function theorem]] ([Hamilton 92](#Hamilton)). A comparison to other notions of smoothness for topological vector spaces with various properties is in ([Keller 74](#Keller)).

## Properties

MB-smooth maps have the following properties.

* Continuous [[linear maps]] are MB-smooth;

* MB-smooth maps are [[continuous map|continuous]];

* MB-smooth maps are smooth in the sense of [[convenient vector spaces]], since the [[chain rule]] holds;

* Maps between [[Fréchet spaces]] are MB-smooth if and only if they are conveniently smooth.

Note that a map that is smooth in the sense of a convenient vector space (equivalently, a smooth map between the corresponding [[diffeological spaces]]) is not necessarily continuous, so not all convenient smooth maps between lctvs are MB-smooth. Explicit examples have been given in ([Gl&#246;ckner 06](#Glockner06)). It is even the case that one can have a convenient _isomorphism_ that is not MB-smooth, so the faithful and non-full functor
$$
lctvs_{MB} \to lctvs_{convenient} \hookrightarrow DiffeologicalSpace
$$
is not even injective on isomorphism classes. The following example was supplied in ([TaQ 15](#TaQ15)):

Let $E$ be the vector space of all real (two-sided) sequences $x=\langle\sp x_i\mid i\in\mathbb{Z}\rangle$ for which $x_i=0$ for $i\ll 0$, topologized so that we get a linear homeomorphism $E\to\mathbb{R}^\mathbb{N}\times\mathbb{R}^{(\mathbb{N})}$ defined by $x\mapsto(u,v)$ where $u_i=x_{i-1}$ and $v_i=x_{-i}$ for $i\gt 0}$. 

Then define the bijection $f:E\to E$ by $x\mapsto y$ where $y_i=x_i$ for $i\neq 0$ and $y_0=x_0+\sum_{i\in\mathbb{N}}(x_i\cdot x_{-i})$. 
The inverse is given by $y\mapsto x$ where $y_i=x_i$ for $i\neq 0$ and $x_0=y_0-\sum_{i\in\mathbb{N}}(y_i\cdot y_{-i})$. 
The duality map $\mathbb{R}^\mathbb{N}\times\mathbb{R}^{(\mathbb{N})}\to\mathbb{R}$, $x\mapsto \sum_{i\in\mathbb{N}}(x_i\cdot x_{-i})$, is discontinuous but bornological, and hence a conveniently smooth bilinear map. Thus $f$ is discontinuous and so not MB-smooth.



## References


* {#Michal38} Aristotle Demetrius Michal, _Differential calculus in linear topological spaces_, Proc. Nat. Acad. Sci. USA **24** (1938), 340-342 ([pdf](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC1077109/pdf/pnas01796-0040.pdf))

* {#Michal40} Aristotle Demetrius Michal, _Differential of  functions with arguments and values in  topological  abelian groups_, Proc. Nat. Acad. Sci. USA **26** (1940), 356&#8211;359. ([pdf](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC1078188/pdf/pnas01616-0038.pdf))

* {#Bastiani64} [[Andree Bastiani]], _Applications diff&#233;rentiables et vari&#233;t&#233;s diff&#233;rentiables de dimension infinie_, J. Anal. Math. **13** (1964), 1&#8211;114. ([article](http://dx.doi.org/10.1007/BF02786619), paywalled)


* {#Milnor} [[John Milnor]], _Remarks on Infinite-Dimensional Lie Groups_, in: B. DeWitt, R. Stora, eds., Les Houches Session XL, _Relativity, Groups and Topology II_ (North-Holland, 1984), pp. 1007-1057

* {#Hamilton} [[Richard Hamilton]], _The Inverse Function Theorem of Nash and Moser_. Bull. Amer. Math. Soc. **7** (1982) 65-222.

* {#Keller} Keller, H. H., _Differential Calculus in Locally Convex Spaces_, Lecture Notes in Mathematics 417, Springer-Verlag, 1974 ([Springerlink](http://dx.doi.org/10.1007/BFb0070564), paywalled)

* {#Glockner06} [[Helge Glöckner]], _Discontinuous non-linear mappings on locally convex direct limits_, Publ. Math. Debrecen 68 (2006) 1-13, [arXiv:math/0503387](http://arxiv.org/abs/math/0503387).


* {#TaQ15} TaQ ([user 12643](http://mathoverflow.net/users/12643/taq)), Answer to _Do locally convex topological vector spaces embed into diffeological spaces?_, MathOverflow, &lt;http://mathoverflow.net/q/209470> (version: 2015-06-16)




[[!redirects Michal-Bastiani smooth maps]]
[[!redirects MB-smooth maps]]
[[!redirects MB-smooth map]]