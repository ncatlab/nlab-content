
> under construction


## Idea

Given an ordinary [[category]] $C$, a pasting diagram in $C$ is nothing but a collection of sequences of composable morphisms in $C$

$$
  a_1 \stackrel{f_1}{\to} a_2 \stackrel{f_2}{\to}
  \cdots
  \stackrel{f_n}{\to} a_{n+1}
  \,.
$$

We think of these arrows as not yet composed, but _pasted_ together at their objects, such as to form a sequence.

Then in an [[n-category]] a pasting diagram is similarly a collection of [[k-morphism|n-morphism]] with a prescribed way how they are to fit together at their boundaries, subject to some conditions which guarantee that it can be uniquely composed or "pasted together" to form a single $n$-morphism.

An simple example of a pasting diagram in a 2-category is

$$
  \array{
    a &\to& b &\to& c
    \\
    \downarrow &\swArrow& \downarrow &\swArrow& \downarrow
    \\
    d &\to& e &\to& f
  }
  \,.
$$

If this is to be composed into a single 2-morphism we read this diagram explicitly as the vertical composite of the 2-morphism

$$
  \array{
    a &\to& b &\to& c
    \\
    && \downarrow &\swArrow& \downarrow
    \\
     && e &\to& f
  }
$$

with the 2-morphism

$$
  \array{
    a &\to& b && 
    \\
    \downarrow &\swArrow& \downarrow && 
    \\
    d &\to& e &\to& f
  }
  \,.
$$

On the other hand, the following diagram is _not_ a pasting diagram: 

$$
  \array{
    a &\to& b &\to& c
    \\
    \downarrow &\neArrow& \downarrow &\swArrow& \downarrow
    \\
    d &\to& e &\to& f
  }
  \,.
$$

Thus, the formal definition of pasting diagram will include conditions which impose a consistent "directionality" of the cells so they can be pasted together.

## References

A formal definition and discussion of pasting diagrams in [[strict omega-categories]] is in

* [[Sjoerd Crans]], _Pasting presentation for Omega-categories_ ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.48.4342))

* Sjoerd Crans, _Pasting schemes for the monoidal biclosed structure on $\omega$-$\mathbf{Cat}$_ ([web](http://crans.fol.nl/papers/thten.html), [ps](http://crans.fol.nl/papers/thten.ps.gz), [[thten.pdf|pdf:file]])

[[!redirects pasting diagrams]]
[[!redirects pasting]]