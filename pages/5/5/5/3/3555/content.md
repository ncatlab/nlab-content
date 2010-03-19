#Contents#
* automatic table of contents goes here
{:toc}

## Idea

If an [[(∞,1)-topos]] $\mathbf{H}$ is that of [[(∞,1)-category of (∞,1)-sheaves|(∞,1)-sheaves]] on (the [[site]] of [[category of open subsets|open subsets]] of) a [[paracompact space|paracompact]] [[topological space]] -- $\mathbf{H} = Sh_{(\infty,1)}(X)$ --  then its **shape** is the _strong shape_ of $X$ in the sense of [[shape theory]]: a [[pro-object]] $Shape(X)$ in the category of [[CW-complex]]es.

It turns out that $Shape(X)$ may be extracted in a canonical fashion from just the [[(∞,1)-topos]] $Sh_{(\infty,1)}(X)$, and in a way that makes sense for any [[(∞,1)-topos]]. This then gives a definition of shape of general $(\infty,1)$-toposes.

## Definition



For every [[(∞,1)-topos]] $\mathbf{H}$ there is the [[terminal object|terminal]] [[geometric morphism]]

$$
  (LConst \dashv \Gamma) : \mathbf{H} \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}
  \infty Grpd
$$

where [[∞Grpd]] is the $(\infty,1)$-topos of [[∞-groupoids]],  $\Gamma$ is the [[global section]]s [[(∞,1)-functor]] and $LConst$ is the [[constant ∞-stack]] functor.

+-- {: .un_def}
###### Definition
**(shape of an $(\infty,1)$-topos)**

The **shape** of $\mathbf{H}$ is the composite functor

$$
  Shape(\mathbf{H}) := \Gamma \circ LConst
  \;\;:\;\;
  \infty Grpd \stackrel{LConst}{\to}
  \mathbf{H}
  \stackrel{\;\;\Gamma\;\;}{\to}
  \infty Grpd
$$

regarded as an object 

$$
  Shape(\mathbf{H})
  \in
  Pro(\infty Grpd)^{op}
  :=
  Func_{lex}(\infty Grpd, \infty Grpd)^{op}
$$

in the [[full subcategory]] of finite [[limit]] preserving [[(∞,1)-functors]].

=--


## Examples

### Shape of a topological space

For a discussion of how the $(\infty,1)$-topos theoretic shape of $Sh_{(\infty,1)}(X)$ relates to the ordinary shape-theoretic _strong shape_ of the topological space $X$ see [[shape theory]].


### Shape of an essential retract {#Retract}

The following is trivial to observe, but may be useful to note.

+-- {: .un_lemma}
###### Observation

Let $(f_! \dashv f^* \dashv f_*) : \mathbf{H} \stackrel{\overset{f_!}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}} \mathbf{B}$ be an [[essential geometric morphism]] of $(\infty,1)$-toposes that exhibits $\mathbf{B}$ as an essential [[retract]] of $\mathbf{H}$ in that 

$$
  (Id \dashv Id)
  \;\;
  \simeq
  \;\;
  \mathbf{B}
    \stackrel{\overset{f_!}{\leftarrow}}{\underset{f^*}{\to}} 
  \mathbf{H}
    \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}} 
  \mathbf{B}
  \,.
$$

Then the shape of $\mathbf{B}$ is equivalent to that of $\mathbf{H}$.

=--

+-- {: .proof}
###### Proof

Since $\infty Grpd$ is the [[terminal object]] under [[geometric morphism]] of Grothendieck $(\infty,1)$-toposes we have

$$
  \begin{aligned}
    (\infty Grpd \stackrel{LConst_{\mathbf{B}}}{\to} \mathbf{B} 
     \stackrel{\Gamma_\mathbf{B}}{\to} \infty Grpd)
    &\simeq
    (\infty Grpd 
      \stackrel{LConst_{\mathbf{B}}}{\to} 
      \mathbf{B} 
      \stackrel{f^*}{\to} \mathbf{H}   
     \stackrel{f_*}{\to} \mathbf{B}
     \stackrel{\Gamma_\mathbf{B}}{\to}
     \infty Grpd)
    \\
    &\simeq
    (\infty Grpd 
     \stackrel{LConst_\mathbf{H}}{\to} 
     \mathbf{H} 
      \stackrel{\Gamma_\mathbf{H}}{\to}
      \infty Grpd)    
  \end{aligned}
  \,.
$$

=--


+-- {: .un_example}
###### Example

In the discussion at [[schreiber:path ∞-groupoid]] it is claimed that the $(\infty,1)$-toposes of [[∞-stack]]s on a [[site]] of _geometrically contractible objects_ (all constant $(\infty,1)$-presheaves satisfy [[descent]] over covers of representables) is a [[locally contractible (∞,1)-topos]] with the property that 

$$
  (f_! \dashv f^* \dashv f_*) 
  :=
  \mathbf{H}
  \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}}
  \infty Grpd
$$ 

exhibits $\infty Grpd$ as an essential retract of $\mathbf{H}$ in the above sense. This means that such $\mathbf{H}$ have the _shape of the point_ .

=--



## References

The definition of shape of $(\infty,1)$-toposes is due to

* [[Bertrand Toen]] and [[Gabriele Vezzosi]],  _Segal topoi and stacks over Segal categories_ , in Proceedings of the
Program _Stacks, Intersection theory and Non-abelian Hodge Theory_ , MSRI, Berkeley, January-May 2002 ([arXiv:math/0212330](http://arxiv1.library.cornell.edu/abs/math/0212330)).

The relation to [[shape theory]] of topological spaces is further discussed in section 7.1.6 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

[[!redirects shape of an (∞,1)-topos]]