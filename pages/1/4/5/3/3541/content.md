A __quantum channel__ is a mapping between [[Hilbert spaces]], $\Phi : L(\mathcal{H}_{A}) \to L(\mathcal{H}_{B})$, where $L(\mathcal{H}_{i})$ is the family of operators on $\mathcal{H}_{i}$.  

+--{: .query}
[[David Roberts]]: Can we write this as:

>A __quantum channel__ is an arrow in a category whose objects are Hilbert spaces, and the arrow itself is a morphism of C-star algebras $\Phi : L(\mathcal{H}_{A}) \to L(\mathcal{H}_{B})$, where $L(\mathcal{H}_{i})$ is the family of operators on $\mathcal{H}_{i}$.  
=--

In general, we are interested in completely positive trace-preserving (CPTP) maps.  

> Zoran: what this ugly acronym means ? We should have an antiacronym point of view in nlab, whenever the acronyms are not in hugely wide use!

> Reply to Zoran: I have corrected it.  However, I was under the impression it was in wide use.  I used it on MathOverflow without a problem and certainly anyone working in quantum information theory (which is what this is under) should know it.

>Harry: What is "the family" of operators on $\mathcal{H}_i$?  A family taking values in $X$ is just a function $I\to X$, where $I$ is called the index.  

The operator spaces can be interpreted as $C^{*}$-[[C-star algebra|algebras]] and thus we can also view the channel as a mapping between $C^{*}$-algebras, $\Phi$: $A \to B$.  Since quantum channels can carry classical information as well, we could write such a combination as $\Phi : L(\mathcal{H}_{A}) \otimes C(X) \to L(\mathcal{H}_{B})$, where $C(X)$ is the space of [[continuous functions]] on some space $X$ and is also a $C^{*}$-algebra.  In other words, whether or not classical information is processed by the channel, it (the channel) is a mapping between $C^{*}$-algebras.  

>Zoran: the point of view that quantum channels are used for processing information is very biased point of view of one of the engineering fields. In nuclear physics multichannel processes were used half a century ago to formulate nonhermitean perturbation theory, where various emissions of particles, radiation and heat within a nucleus leads to dissipation. We should have a general point of view and not be crippled by somebody's particular engineering fad. 

> Reply to Zoran: Maybe, but the word "channel" (according to the dictionary) implies an information processing context and, besides, that is how they are used in quantum information theory which is what this page is about.  I'm not sure I'd call it a "fad" either.  I go to enough cross-disciplinary meetings to know that its a paradigm that runs across a number of fields and sub-fields.

Note, however, that these are not necessarily the same $C^{*}$-algebras.  Since the channels are represented by square matrices, the input and output $C^{*}$-algebras must have the same dimension, $d$.  Thus we can consider them both subsets of some $d$-dimensional $C^{*}$-algebra, $C$, i.e. $A \subset C$ and $B \subset C$. Thus a quantum channel is a mapping from $C$ to itself.

The following is a proof that a quantum channel is a [[category]].  The proof actually proves it is a [[monoid]], but the need for it to be a category becomes more clear when we start dealing with these things en masse.

+-- {: .un_prop}
###### Proposition

The quantum channels $t: L(\mathcal{H}) \to L(\mathcal{H})$, together with the $d$-dimensional $C^{*}$-algebra, $C$, on which they act, forms a category we call $\mathbf{Chan}(d)$, where $C$ is the sole object and the quantum channels $t$ are the arrows.
=--

+-- {: .proof}
###### Proof
Consider the quantum channels

$\begin{aligned}
r: L(\mathcal{H}_{\rho}) \to L(\mathcal{H}_{\sigma}) & \where &
\sigma=\sum_{i}A_{i}\rho A_{i}^{\dagger} \\
t: L(\mathcal{H}_{\sigma}) \to L(\mathcal{H}_{\tau}) &
\where &
\tau=\sum_{j}B_{j}\sigma B_{j}^{\dagger} 
\end{aligned}$

where the usual properties of such channels are assumed (e.g. trace preserving, etc.).  We form the composite $t \circ r: L(\mathcal{H}_{\rho}) \to L(\mathcal{H}_{\tau})$ where


$\begin{aligned}
\tau & = \sum_{j}B_{j}\left(\sum_{i}A_{i}\rho A_{i}^{\dagger}\right)B_{j}^{\dagger}  \\
& = \sum_{i,j}B_{j}A_{i}\rho A_{i}^{\dagger}B_{j}^{\dagger} \\
& = \sum_{k}C_{k}\rho C_{k}^{\dagger} 
\end{aligned}$

and the $A_{i}$, $B_{i}$, and $C_{i}$ are Kraus operators.

Since $A$ and $B$ are summed over separate indices the trace-preserving property is maintained, i.e. $\sum_{k} C_{k}^{\dagger}C_{k}=\mathbb{1}$.

For a similar methodology see [Nayak and Sen](http://arxiv.org/abs/quant-ph/0605041).

We take the identity arrow, $1_{\rho}: L(\mathcal{H}_{\rho}) \to L(\mathcal{H}_{\rho})$, to be the time evolution of the state $\rho$ in the absence of any channel.  Since this definition is suitably general we have that $t \circ 1_{A}=t=1_{B} \circ t \quad \forall \,\, t: A \to B$.

Consider the three unital quantum channels $r: L(\mathcal{H}_{\rho}) \to L(\mathcal{H}_{\sigma})$, $t: L(\mathcal{H}_{\sigma}) \to L(\mathcal{H}_{\tau})$, and $v: L(\mathcal{H}_{\tau}) \to L(\mathcal{H}_{\upsilon})$ where $\sigma=\sum_{i}A_{i}\rho A_{i}^{\dagger}$, $\tau=\sum_{j}B_{j}\sigma B_{j}^{\dagger}$, and $\eta=\sum_{k}C_{k}\tau C_{k}^{\dagger}$.  We have

$\begin{aligned}
v \circ (t \circ r) & = v \circ \left(\sum_{i,j}B_{j}A_{i}\rho A_{i}^{\dagger}B_{j}^{\dagger}\right) = \sum_{k}C_{k} \left(\sum_{i,j}B_{j}A_{i}\rho A_{i}^{\dagger}B_{j}^{\dagger}\right) C_{k}^{\dagger}  \\
& = \sum_{i,j,k}C_{k}B_{j}A_{i}\rho A_{i}^{\dagger}B_{j}^{\dagger}C_{k}^{\dagger} = \sum_{i,j,k}C_{k}B_{j}\left(A_{i}\rho A_{i}^{\dagger}\right)B_{j}^{\dagger}C_{k}^{\dagger}  \\
& = \left(\sum_{i,j,k}C_{k}B_{j}\tau B_{j}^{\dagger}C_{k}^{\dagger}\right) \circ r = (v \circ t) \circ r
\end{aligned}$.

and thus we have associativity.  Note that similar arguments may be made for the inverse process of the channel if it exists (it is not necessary for the channel here to be reversible).
=--


[[!redirects quantum channel]]
[[!redirects quantum channels]]
