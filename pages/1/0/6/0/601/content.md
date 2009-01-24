#Idea#

One can naturally think of a [[cospan]] as the abstraction of a [[cobordism]]. For instance an [[interval object]] cospan models the standard topological interval $[0,1]$ regarded as a cobordism from pt to pt.

The [[duality|concrete dual]] of a co-span, obtained by mapping it into some target object, is a [[span]], which in the context of [[groupoidification]] and [[geometric function theory]] can be interpreted as a generalized linear map. On such a generalized linear map, there is a notion of _trace_, the [[span trace]].

The _co-span co-trace_ is the concept dual to that: the image of the co-trace of a co-span under mapping it into a target object is the span trace of the result of mapping the original co-span to that target object. 


#Definition#

For 

$$
  \array{
    && T
    \\
    & {}^{in}\nearrow && \nwarrow^{out}
    \\
    \Sigma &&&& \Sigma
  }
$$

a [[cospan]] with identical left and right index object $\Sigma$, its **co-span co-trace** $cotr(T)$ is the composite of the result 

$$
  \array{
    && T
    \\
    & {}^{in \sqcup out}\nearrow && \nwarrow
    \\
    \Sigma \sqcup \Sigma &&&& \emptyset
  }
$$

of dualizing one leg of the co-span with the co-span

$$
  \array{
    && \Sigma
    \\
    & {}^{}\nearrow && \nwarrow^{Id \sqcup Id}
    \\
    \emptyset &&&& \Sigma \sqcup \Sigma
  }
$$

i.e. the [[pushout]]

$$
  \array{
    &&&&
    \mathrm{cotr}T
    \\
    &&& \nearrow && \nwarrow 
    \\
    && \Sigma &&&& T
    \\
    & {}^{}\nearrow && \nwarrow^{Id \sqcup Id}
    && {}^{in \sqcup out}\nearrow && \nwarrow
    \\
    \emptyset &&&& \Sigma \sqcup \Sigma &&&& \emptyset
  }  
$$

regarded as a cospan from the initial object 
$\emptyset$ to $\emptyset$

$$
  \array{
    && cotr(T)
    \\
    & {}^{}\nearrow && \nwarrow
    \\
    \emptyset &&&& \emptyset
  }
  \,.
$$

## Definition for multi-cospans

More generally, the trace of a [[multi-cospan]] over $n$ identical of its index objects $\Sigma$ is the composite with the multi-cospan

$$
  \array{
    & \Sigma
    \\
    & {}^{Id}\nearrow \uparrow^{Id} & \cdots 
    \\
    \Sigma & \Sigma & \cdots & \Sigma & \cdots
  }
$$


#Examples

## Co-tracing topological interval to circle

Let the ambient category be [[Top]], let $I = [0,1]$ be the standard topological interval and let $e := (0,\epsilon)$ be a small open interval, for some $0 \lt \epsilon \lt 1/2$ -- to be thought here as a _collar_ of the point $pt$.

Let

$$
  \array{
     && I
     \\
     & {}^1\nearrow && \nwarrow^{1-(-)}
     \\
     e &&&& e
  }
$$

be the interval regarded as a collared cobordisms from the point to the point. Its cotrace, the pushout

$$
  \array{
     cotr(I) &\leftarrow& I
     \\
     \uparrow && \uparrow^{in \sqcup out}
     \\
     e &\stackrel{Id \sqcup Id}{\leftarrow}& e \sqcup e
  }
$$

is the result of gluing the ends of the interval to each other, i.e. the circle

$$
  cotr(I) = S^1
  \,.
$$

+--{.query}
[[Urs Schreiber|Urs]]: This may require a bit more care
with the topology involved.
=--


## Co-tracing category interval object to the natural numbers

Let the ambient category be [[Cat]], let $I = \{a \to b\}$ be the standard [[interval object]] in [[Cat]] and let 
$pt = \{\bullet\}$ be the terminal category.

Let

$$
  \array{
     && I
     \\
     & {}^{pt \mapsto a}\nearrow && \nwarrow^{pt \mapsto b}
     \\
     pt &&&& pt
  }
$$

be the standard [[interval object]] in [[Cat]]
regarded in the standard way as a cospan from the 
point to the point. Its cotrace, the pushout

$$
  \array{
     cotr(I) &\leftarrow& I
     \\
     \uparrow && \uparrow^{in \sqcup out}
     \\
     pt &\stackrel{Id \sqcup Id}{\leftarrow}& pt \sqcup pt
  }
$$

is the result of gluing the ends of the interval object to each other, which here is the [[skeleton]] of the [[fundamental category]] of the [[directed space|directed circle]], namely the [[monoid]] of natural numbers, regarded as a one-object category:

$$
  cotr(I) = \mathbf{B} \mathbb{N} = \{\bullet \stackrel{n}{\to} \bullet | n \in \mathbb{N}\}
  \,.
$$

If instead we start with the standard interval object in groupoids, $I_{inv} = \{a \stackrel{\simeq}{\to} b\}$ with the nontrivial morphism from $a$ to $b$ being an [[isomorphism]], then the co-trace in question is the [[skeleton]] of the [[fundamental groupoid]] of the ordinary [[topological space|topological circle]]

$$
  cotr(I_{inv}) = \mathbf{B} \mathbb{Z} = \{\bullet \stackrel{n}{\to} \bullet | n \in \mathbb{Z}\}
  \,.
$$



#Remarks#

* The dual notion is that of [[span trace]]

#References#

While the concept is obvious, it is apparently (?) not discussed yet in the (young) literature on the subject. On the blog the concept was mentioned in

* Urs Schreiber, [(co)-traces](http://golem.ph.utexas.edu/category/2008/05/hopkinslurie_on_baezdolan.html#c021537)