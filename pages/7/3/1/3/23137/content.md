
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

(...)


## Definition

\begin{definition}\label{QuillenNegation}
**(weak orthogonal class/Quillen negation)**
\linebreak
Given a [[class]] $M \;\subset\; Mor(\mathcal{C})$ of [[morphisms]] in a [[category]] $\mathcal{C}$, its 

* *left weak orthogonal class* or *left [[Quillen negation]]*

  $\multiscripts{^&solb;}{M}{} \;\subset\; Mor(\mathcal{C})$ 

  (also denoted $M Proj$ or similar, for *$M$-[[projective morphisms]]*)

or 

* *right weak orthogonal class* or *right [[Quillen negation]]* 


  $\multiscripts{}{M}{^&solb;} \;\subset\; Mor(\mathcal{C})$  

  (also denoted $M Inj$ or similar, for *$M$-[[injective morphisms]]*)

is the [[class]] of [[morphisms]] in $\mathcal{C}$ which have the left, respectively right, [[lifting property]] with respect to each morphism in the class $M$:

$$
  M^{&solb;} 
  \;\coloneqq\;
  \Big\{ 
    p \,\in\, Mor(\mathcal{C})
    \;\big\vert\; 
   \underset{i \in M}{\forall}
   \; i \,&solb;\, p
  \Big\}, 
  \;\;\;\;\;
  {}^{&solb;}M 
  \;\coloneqq\;
  \Big\{ 
    i \,\in\, Mor(\mathcal{C})
    \;\big\vert\; 
   \underset{p \in M}{\forall}
   \; i \,&solb;\, p
  \Big\}
  \,.
$$ 

\end{definition}

## Properties

\begin{proposition}
**(closure properties)**
\linebreak
  A right weak-orthogonal class $C^{&solb;}$ is always closed under  [[retracts]], [[pullbacks]], (small) [[product|products]] (whenever they exist in the category) and [[composition]] of morphisms, and contains all [[isomorphisms]] of C. 

Meanwhile, a left weak-orthogonal class ${}^{&solb;}M$ is closed under [[retracts]], [[pushout]], (small) [[coproduct]] and [[transfinite composition]] ([[filtered colimits]]) of morphisms (whenever they exist in the category), and also contains all [[isomorphisms]].
\end{proposition}
This **proof** is straightforward, see for instance [here](ClosurePropertiesOfInjectiveAndProjectiveMorphisms) at *[[injective or projective morphism]]*.

\begin{remark}
It is clear that 
$$
  C \;\subset\;
  \big({}^{&solb;}M\big)^{&solb;}
  \,,
  \;\;\;
  C \;\subset\;
  \multiscripts{^&solb;}{\big(M^{&solb;}\big)}{}
  \,.
$$
\end{remark}


## Related entries

* [[lifting property]]

* [[separation axioms in terms of lifting properties]]

## Examples

\begin{example}
In the category [[Set]] of [[sets]], the right [[Quillen negation]] 
of the "simplest non-[[surjection]]" $\varnothing \to \ast$ (the unique [[map]] from the [[empty set]] to the [[singleton set]]) is the class of [[surjections]]:

$$
  \big\{
    \varnothing \to \ast
  \big\}^{&solb;}
  \;=\;
  \big\{
    f \;\big\vert\; f \; \text{is surjective}
  \big\}
  \,.
$$

The left and right Quillen negations of $\{x_1,x_2\} \to \ast$ (the "simplest non-[[injection]]") are both precisely the class of [[injections]],  
$$
  {}^{&solb;}
  \big\{
    \{x_1,x_2\}
    \longrightarrow 
    \ast
  \big\} 
  \;=\; 
  \big\{
    \{x_1,x_2\}  \longrightarrow \ast
  \big\}^{&solb;} 
  \;=\; 
  \big\{ f \;\big\vert\; f \; \text{ is injective } \big\}
  \,.
$$

\end{example}


## References

Left/right weak orthogonal classes are discussed, for instance, in any text on [[model category]]-theory, see the references [there](model+category#References).

Discussion with an eye towards [[separation axioms in terms of lifting properties]] and amplifying the logical aspect of conceptual negation:

* [[Misha Gavrilovich]], *Remarks on Shelah's classification theory and Quillen's negation* ([arXiv:2010.08791](https://arxiv.org/abs/2010.08791))

[[!redirects Quillen negations]]

[[!redirects orthogonal class]]
[[!redirects orthogonal classes]]

[[!redirects left orthogonal class]]
[[!redirects left orthogonal classes]]
[[!redirects right orthogonal class]]
[[!redirects right orthogonal classes]]


[[!redirects weak orthogonal class]]
[[!redirects weak orthogonal classes]]

[[!redirects left weak orthogonal class]]
[[!redirects left weak orthogonal classes]]
[[!redirects right weak orthogonal class]]
[[!redirects right weak orthogonal classes]]




