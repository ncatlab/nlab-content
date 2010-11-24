#Idea#

In the context of [[groupoidification]] and [[geometric function theory]] one thinks of a [[span]] as a generalized linear map. The _span trace_ is the corresponding generalization of the notion of a trace of a linear map.

This is just the general [[trace]] of an [[endomorphism]] which is definable in any [[compact closed category|compact/autonomous]] [[symmetric monoidal category|symmetric monoidal (2-)category]], of which $Span$ is an example (as described below).

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

a [[span]] with identical left and right index object $X$, the simplest way to define its __span trace__ $tr(R)$ is as by regarding it as a map $R\to X\times X$, then pulling back along the [[diagonal morphism]] $X\to X\times X$.

This can be expressed in terms of the [[bicategory]] [[Span]] in several ways.  For instance, we can regarding it as the composite of the result 

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

##Trace of Set-valued matrices##

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


##Loop objects from homotopy span traces##

Let $C$ be a [[category of fibrant objects]] with [[interval object]] $I$. Recall that for every object $B$ of $C$ its free [[loop space object]] is the part of the [[path object]] $B^I = [I,B]$ which consists of closed paths, i.e. the pullback.
$$
  \array{
    \Omega B &\to& [I,B]
    \\
    \downarrow && \downarrow^{d_0 \times d_1}
    \\
    B &\stackrel{Id \times Id}{\to}& B \times B
  }
  \,.
$$
This can be understood as the _homotopy span trace_ of the identity span on $B$ 

$$
  \Omega B = hotr(Id_B) = hotr\left(
    \array{
      && B
      \\
      & {}^{Id}\swarrow && \searrow^{Id}
      B &&&& B
    }
  \right)
  \,,  
$$
where the homotopy span trace is computed like the span trace but with the pullback replaced by a [[homotopy limit|homotopy pullback]]:
$$
  hotr(Id_B) =
  holim 
  \left(
    \array{
      B &&&& B
      \\
      & {}_{Id \times Id}\searrow && \swarrow_{Id \times Id}
      \\
      &&
      B \times B
    }
  \right)
  \,.
$$
According to the example described at [[homotopy limit]] and  using that we assume that we are in a [[category of fibrant objects]] we can compute this homotopy limit, up to weak equivalence, as the ordinary limit of the weakly equivalent pullback diagram 
$$
  \array{
     F
     &&&& 
     B &\stackrel{Id \times Id}{\to}& B \times B
     &\stackrel{Id \times Id}{\leftarrow}& B
     \\
     \downarrow^{\simeq}
     &&&&
     \downarrow^{\simeq} && \downarrow^{Id} && \downarrow^{Id}
     \\
     F'
     &&&&
     [I,B] &\stackrel{d_0 \times d_1}{\to}&
     B \times B &\stackrel{Id \times Id}{\leftarrow}&
     B
  }
$$
where we replace $B$ by its [[path object]] $B^I = [I,B]$ using the factorization of $B \stackrel{Id \times Id}{\to} B \times B$ as $B \stackrel{\simeq}{\to} [I,B] \stackrel{d_0 \times d_1}{\to} B \times B$ guaranteed to exist in a [[category of fibrant objects]], where $[I, B] \stackrel{d_0 \times d_1}{\to} B \times B$ is a _fibration_:

$$
  holim_D F \stackrel{\simeq}{\to} lim_D F'
  \,.
$$

But by the above $lim_D F' = \Omega B$.


##Categorical trace from homotopical span trace##

The [[categorical trace]] on a 1-[[endomorphism]] in a 2-category $C$ is the homotopy trace on the span given by that endomorphism.

This should be true quite generally, but here are the details just for the special case that connects to the above example:

Let $C = $ [[Grpd]] with the standard interval object $I = \{a \stackrel{\simeq}{\to} b\}$. This is a [[category of fibrant objects]] with respect to the [[folk model structure]]. 

Notice that [[natural transformation]]s $\eta : F \to G$ between two functors $F, G : C \to D$ are in bijection with commuting diagrams
$$
  \array{
     X &\stackrel{\eta}{\to}& [I,Y]
     \\
     \downarrow^{Id} && \downarrow^{d_0 \times d_1}
     \\
     X &\stackrel{F \times G}{\to}& Y \times Y
  }
  \,.
$$

Now, the homotopy trace on the span corresponding to an ednofunctor $F : B \to B$ is

$$
  hotr(F)
  =
  hotr\left(
    \array{
      && B
      \\
      & {}^{Id}\swarrow && \searrow^{F}
      \\
      B &&&& B
    }
  \right)
  =
  holim\left(
    \array{
      B &&&& B
      \\
      & {}_{Id \times Id}\searrow && \swarrow{F \times Id}
      \\
      && B \times B
    }
  \right)
  \,.
$$

Since we are in a category of fibrant objects the assumptions of the example discussed at [[homotopy limit]] apply and the above homotopy limit is again computed, up to weak equivalence, by the ordinary limit of

$$
  \cdots
  \stackrel{\simeq}{\to}
  lim
  \left(
    \array{
      [I,B] &&&& B
      \\
      & {}_{d_0 \times d_1}\searrow && \swarrow{Id \times F}
      \\
      && B \times B
    }
  \right)
  \,.  
$$

By the above, every cone over the pullback diagram with a functor $h : Q \to B$, on the right defines a natural transformation $h^*(Id_B \Rightarrow F)$. By the universal property of the limit, it _represents_ the collection of these transformations.


#Remarks#

* The dual notion is that of [[co-span co-trace]].

#References#

That the canonical trace on $Span$ is compatible with the interpretation of spans as linear maps in the context of [[groupoidification]], and that it corresponds under duality  (in terms of the [[co-span co-trace]]) to the gluing of ends of [[cobordism]]s was mentioned in

* Urs Schreiber, [(co)-traces](http://golem.ph.utexas.edu/category/2008/05/hopkinslurie_on_baezdolan.html#c021537)


[[!redirects span traces]]
