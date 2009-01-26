#Idea#

In the context of [[groupoidification]] and [[geometric function theory]] one thinks of a [[span]] as a generalized linear map. The _span trace_ is the corresponding generalization of the notion of a trace of a linear map.

This is just the general [[trace]] of an endomorphism which is definable in any compact symmetric [[monoidal category]], of which $Span$ is an example (as described below). 

In the context of [[FQFT]] a useful aspect of the span trace is that it is manifestly dual to the [[co-span co-trace]], which, as described there, corresponds under the interpretation of spans as [[cobordism]]s to gluing of the two ends of a cobordism. 



#Definition#

For 

$$
  \array{
    && R
    \\
    & {}^x\swarrow && \searrow^{y}
    \\
    X &&&& X
  }
$$

a [[span]] with identical left and right index object $X$, its _span trace_ $tr(R)$ is the composite of the result 

$$
  \array{
    && R
    \\
    & {}^{x \times y}\swarrow && \searrow
    \\
    X \times X &&&& pt
  }
$$

of dualizing one leg of the span with the span

$$
  \array{
    && X
    \\
    & {}^{}\swarrow && \searrow^{Id \times Id}
    \\
    pt &&&& X \times X
  }
$$

i.e. the [[pullback]]

$$
  \array{
    &&&&
    \mathrm{tr}R
    \\
    &&& \swarrow && \searrow 
    \\
    && X &&&& R
    \\
    & {}^{}\swarrow && \searrow^{Id \times Id}
    && {}^{x \times y}\swarrow && \searrow
    \\
    pt &&&& X \times X &&&& pt
  }  
$$

regarded as a span from the point to the point

$$
  \array{
    && tr(R)
    \\
    & {}^{}\swarrow && \searrow
    \\
    pt &&&& pt
  }
  \,.
$$

## Definition for multispans

More generally, the trace of a [[multispan]] over $n$ identical of its index objects $X$ is the composite with the multispan

$$
  \array{
    & X
    \\
    & {}^{Id}\swarrow \downarrow^{Id} & \cdots 
    \\
    X & X & \cdots & X & \cdots
  }
$$


#Examples

Let the ambient category be [[Set]], let $X$ be a finite set and $R \to X \times X$ an $|X| \times |X|$-matrix of finite sets, regarded under [[groupoid cardinality]] as a [[groupoidification|groupoidified]] $|X| \times |X|$-matrix with entries in $\mathbb{N}$.

The trace of the span
$$
  \array{
    && R
    \\
    & {}^x\swarrow && \searrow^{y}
    \\
    X &&&& X
  }
$$

is the pullback

$$
  \array{
     tr(R) &\to& R
     \\
     \downarrow && \downarrow^{x,y}
     \\
     X &\stackrel{Id \times Id}{\to}& X \times X
  }
$$

which is the [[coproduct]] set $tr(R) = \sqcup_{x \in X} R_{x,x}$. Under [[groupoid cardinality]] this is indeed the trace 
$|tr(R)| = \sum_{x} |R_{x,x}| $
of the matrix $|R|$ represented by $R$. 


#Remarks#

* The dual notion is that of [[co-span co-trace]]

#References#

That the canonical trace on $Span$ is compatible with the interpretation of spans as linear maps in the context of [[groupoidification]], and that it corresponds under duality  (in terms of the [[co-span co-trace]]) to the gluing of ends of [[cobordism]]s was mentioned in

* Urs Schreiber, [(co)-traces](http://golem.ph.utexas.edu/category/2008/05/hopkinslurie_on_baezdolan.html#c021537)

