\tableofcontents

\section{Introduction}

Observing that an [[anabelioid]] is in particular a [[topos]], a finite étale morphism $\mathcal{X} \rightarrow \mathcal{Y}$ of [[anabelioid|anabelioids]] is the same as an [[étale geometric morphism]]: it is a 'local isomorphism', in some sense. 

\section{Definition}

Recall that a [[morphism of anabelioids]] $\mathcal{X} \rightarrow \mathcal{Y}$ is simply an [[exact functor]] $\mathcal{Y} \rightarrow \mathcal{X}$, that is to say, a functor $\mathcal{Y} \rightarrow \mathcal{X}$ preserving both finite limits and finite colimits. The following definition follows [Mochizuki2004](#Mochizuki2004).

\begin{defn} A [[morphism of anabelioids]] $f: \mathcal{X} \rightarrow \mathcal{Y}$ is _finite étale_ if there is an object $S$ of $\mathcal{Y}$ such that $f = i_S \circ i$ for some isomorphism of anabelioids $i: \mathcal{X} \rightarrow \mathcal{Y}_{/ S}$, where $\mathcal{Y}_{/ S}$ denotes the [[overcategory]] of objects of $\mathcal{Y}$ over $S$, and where $i_{S}: \mathcal{Y}_{/ S} \rightarrow \mathcal{Y}$ is the canonical functor.  \end{defn}

\section{References}

* {#Mochizuki2004} _The geometry of anabelioids_, [[Shinichi Mochizuki]], 2004, Publ. Res. Inst. Math. Sci., 40, No. 3, 819-881. [paper](http://www.kurims.kyoto-u.ac.jp/~motizuki/The%20Geometry%20of%20Anabelioids.pdf) [Zentralblatt review](https://zbmath.org/?q=an%3A1113.14021)