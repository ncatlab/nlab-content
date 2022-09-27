
[[MetaLogicOfIdentifications-220925.jpg:file]]




<a href="https://ncatlab.org/nlab/files/BOZAPALIDES_theorie_formelle_bicategories.pdf">pdf</a>

\begin{tikzcd}
  \mathrm{Top}_{(0,1)}
  \ar[rr, "\mathrm{Sh}(-)"]
  \ar[d, "{\mathrm{forget}}"{pos=.9,yshift=5pt,sloped}]
  \ar[drr, phantom, "{\#}"]
  &&
  \mathrm{Top}_{(1,1)}
  \ar[d, "{\mathrm{forget}}"{pos=.9,yshift=5pt,sloped}]
  \\
  \mathrm{Cat}_{(0,1)}
  \ar[rr, hook]
  &&
  \mathrm{Cat}_{(1,1)}  
\end{tikzcd}


## Idea

In [[type theory]] -- where one understand every piece of data (every "[[term]]") to be assigned a specific [[type]] which specifies its operational behaviour -- *identity types* (maybe better: *identification types*) $Id_X$ are the types of those terms which serve as "witnesses" or "certificates" (see at "[[propositions  as types]]") of identification of terms of type $X$. 

What exactly this means depends on the nature of the ambient [[type theory]] and the choices for the [[inference rules]] of the identity types (see at *[[extensional type theory|extensional]]* and *[[intensional type theory]]*). In some setups (see  [below](#IdeaStrictIdentityTypes)), having a term of identity type means much the same as having an [[equality]] in [[classical mathematics]] ([[definitional equality]]), and for this (historical) reasons identity types are often denoted simply by equality signs, for better or worse.

But the power of the notion of identity types goes beyond this classical situation and results from the fact that they may give the notion of equality a [[constructive mathematics|constructive]] meaning ("[[propositional equality]]"). Taking this constructive principle of identity types to its logical conclusion, leads -- notably in [[Martin-Löf dependent type theory]] -- to identity types which themselves have identity types, reflecting identifications-of-identification, and so ever on, mimicking the structure of [[homotopies]] and [[homotopies of homotopies]] in [[homotopy theory]], whence one refers to type theories with such identity types also as *[[homotopy type theories]]*.

\linebreak

### ML Identity types
 {#IdeaMLIdentityTypes}

More in detail, the [[inference rules]] for identity types in [[Martin-Löf dependent type theory|Martin-Löf-]]/[[homotopy type theory]] may be understood as follows:

**(0) -- There is a notion of identitification.** To start with for every type $X$ and any [[pair]] $x_1, x_2 : X$ of its [[terms]], let's denote the *type of identifications* of $x_1$ with $x_2$ by $Id_X(x_1,x_2)$ (other common notation for identity types is "$x_1 =_{{}_X} x_2$" which, when adopted, requires authors to make up new symbols, like $\equiv$, for actual equalities).
In the jargon of [[dependent type theory]] this means that there is a [[type formation]] rule for identity types as shown on the left here:

<center>
<img src="/nlab/files/MetaLogicOfIdentifications-0-220927.jpg" width="700">
</center>

On the right we are indicating, here and in the following, the [[categorical semantics]] of the [[judgement]] on the left, under the [[relation between type theory and category theory]], specifically [[categorical model of dependent types|between dependent type theory and LCC category theory]]. The lay reader may take the diagrams shown on the right as intuitive illustrations of [[dependent types]] as [[bundles]] of types, their [[terms]] as [[sections]], etc. Technically, these are [[diagrams]] in some [[locally cartesian closed category|locally cartesian closed]] ([[locally cartesian closed model category|model]]) [[category]]. The archetypical example is the ([[classical model structure on simplicial sets|classical model structure on]]) [[SimplicialSets]] in which case all [[fibrations]] shown are [[Kan fibrations]] between [[Kan complexes]] which may be thought of as models for ([[left fibration|fibrations of]]) [[infinity-groupoid|$\infty$-groupoids]]. But the power of these identity types is that they may just as well be interpreted in much more general [[model categories]], such as the [[injective model structure on simplicial presheaves]] over any [[simplicial site]], modelling [[(infinity,1)-topos|$\infty$-toposes]] of [[infinity-stack|$\infty$-stacks]].

Now to consider three "self-evident" properties of the notion of identifications, expressed in type theoretic language:

\linebreak

**(I) -- All data is identified with itself.**  This "[[first law of thought]]" is the [[term introduction]]-rule for identity types:

<center>
<img src="/nlab/files/MetaLogicOfIdentifications-1-220927.jpg" width="700">
</center>

\linebreak

**(IIa) -- Substitution of identifications preserves computations.**  This is Leibniz's "[[salva veritate]]"-principle phrased operationally/constructively:

<center>
<img src="/nlab/files/MetaLogicOfIdentifications-2-220927b.jpg" width="700">
</center>

In [[homotopy type theory]] this has come to be known as *[[transport]]*, compatible with the fact that its [[categorical semantics]] is that of  path lifting in [[Kan fibrations]], which in the case of [[discrete fibrations]]  ([[covering spaces]]) underlying [[flat  connection|flat]] [[principal bundles]] or [[flat vector bundles]]  ("[[local systems]]") is the [[parallel transport]]/[[holonomy]]/[[monodromy]] of the corresponding [[flat connection]].

\linebreak

**(IIb) -- Substitution of identifications preserves computations.** This may seem  so obvious that it is left implicit by the logical forefathers, such as [in Leibniz writings](identity%20of%20indiscernibles#Lewis18),  but when thought of operationally/constructively this is more subtle than the previous two principles, since  in asserting reversibility of identifications we are speaking of *identifications of identifications*:

\begin{tikzcd}
  & 
  x
  \ar[
    dl, 
    "{ \scalebox{.6}{\clap{an identification}} }"{sloped, swap,  pos=.45},
    "{ }"{name=s,  pos=.83}
  ]
  \ar[
    dr, 
    "{ \scalebox{.6}{\clap{self-identification}} }"{sloped,  pos=.45},
    "{ }"{name=t, swap,  pos=.82}
  ]
  \ar[
    from=s, to=t,
    Rightarrow,
    "{ \scalebox{.6}{ 
      \clap{identification-of-identifications}
    } }"{swap}
  ]
  \\
  x'
  \ar[
    rr,
    "{
      \scalebox{.65}{reverse identification}
    }"{swap}
  ]
  &&
  x
\end{tikzcd}

In type  theory language, the existence of these identifications-of-identifications is the following [[judgement]] (with $\underset{x'  : X}{\coprod}$ denoting the [[dependent sum]]-type):

<center>
<img src="/nlab/files/MetaLogicOfIdentifications-3-220927.jpg" width="700">
</center>

\linebreak


**(J) $\Leftrightarrow$ (II) -- Id-induction.** 
Applying the above [[transport]]  rule (IIa) to the identifications-of-identifications provided by the reversal rule  (IIb) yields the following  "[[J-rule]]", which was not known to  the forefathers:

<center>
<img src="/nlab/files/MetaLogicOfIdentifications-4-220927.jpg" width="700">
</center>

(This "[[induction]]-rule" for identity types was proposed in [Martin-Löf 1975, §1.7 and p. 94 ](#MartinLof75), its modern rendering as a formal [[inference rule]] is due to [Nordström,  Petersson & Smith 1990,  §8.1](#NordströmPeterssonSmith90). It may be understood as the [[term  elimination rule]] or the [[induction]]=principle for identity types, whence also called "Id-elimination" or "Id-induction",  or similar.)

While the J-rule is naturally understood as the application of the transport rule (IIa) to the identifications-of-identification provided by the reversal rule (IIb), it also implies both these  rules, hence is equivalent to their combination (IIa and IIb). 

(This fact was briefly mentioned by [Coquand 2011, slides 26+28](#Coquand11) and amplified by [Ladyman & Presnell 2015](#LadymanPresnell15);  the detailed proof is spelled out by [Götz 2018, §4.2](#Götz18).) 

Moreover, the [[categorical semantics]]  of the [[J-rule]] is manifestly that of the [[left lifting property]] of $X \xrightarrow{diag} X^I$ against all [[fibrations]], which means that this rule manifestly prescribes the interpretation of identity types by "[[very good path space objects]] " in the sense of [[model category theory]] (cf. [Shulman 2012](#Shulman12) [III,, Slide 34](http://home.sandiego.edu/~shulman/hottminicourse2012/03models.pdf#page=34); [Riehl  2022,  §1.1](#Riehl22)). 

It is ultimately fact which connects identity types to the notion of [[homotopy]] in [[homotopy theory]],  hence to the interpretation of [[Martin-Löf dependent type theory]] as  "[[homotopy type theory]]" with [[categorical semantics]] in  [[locally cartesian closed (infinity,1)-category|locally cartesian closed  $\infty$-categories]].
 



### Other notion of identity types

Besides the Martin-Löf identity types [above](#IdeaMLIdentityTypes)  there are other version of identity types, such as

* [[cubical path types]]

* Swan identity types

* identity types in  [[higher observational type theory]]

Each kind of identity type also has one or more corresponding notions of [[dependent identity type]].  In some cases, such as cubical path types and higher observational identity types, the ordinary identity type is exactly a special case of the dependent one, where the dependence is constant or the base path is reflexivity.  In other cases, such as some versions of the Martin-Lof dependent identity type, one or both of these degenerate forms of dependent identity type don't reduce definitionally to the simple one, but are only equivalent to it.

Notably there are strict identity types:

### Strict identity types
  {#IdeaStrictIdentityTypes}

Since there are two notions of [[equality]] in type theory, there are similarly two notions of the J-rule in type theory. The **definitional J-rule** states that $J(x, x, \mathrm{refl}(x))$ is definitionally equal to $c(x)$ (i.e. $J(x, x, \mathrm{refl}(x)) = c(x)$). This is in  contrast to the **propositional J-rule** or **typal J-rule** above,  which states that there is a dependent term 
$$q(x):Id_{C(x,x,\mathrm{refl}(x))}(J(x, x, \mathrm{refl}(x)), c(x))$$

Identity types which satisfy the definitional J-rule could be called **strict identity types**, while identity types which only satisfy the propositional J-rule could be called **weak identity types**, in parallel with similar definitions for a (weak and strict) [Tarski universe](type+universe#TarskiStyle). Martin-Löf identity types come in both strict and weak flavours. However, most other identity types in the literature, such as cubical path types and higher observational identity types, are only weak identity types.


[[MetaLogicOfIdentifications-0-220927.jpg:file]]

[[MetaLogicOfIdentifications-1-220927.jpg:file]]

[[MetaLogicOfIdentifications-2-220927.jpg:file]]

[[MetaLogicOfIdentifications-2-220927b.jpg:file]]


[[MetaLogicOfIdentifications-3-220927.jpg:file]]

[[MetaLogicOfIdentifications-4-220927.jpg:file]]

spring


## Idea

play around with the editing functionality

## Definition

\begin{defn}(Title of defn). \label{defn_anchor} {#html_anchor} The **sandbox** is a box full of sand.
\end{defn}

One usually defines *waterboxes* analogous to  [[Sandbox#defn_anchor|this Definition]] (which could be on another page).

## A sandtable

| Sand | More sand |
| ----------- | ----------- |
| sand | sand |
| sand | sand |

How do "quotes" work? `quote', 'quote'.

How to do a list

- sand
- sand
- sand

* sand
* sand 
* sand

## Figures

make a responsive figure (that scales, but not too much):

<center>
<figure>
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b9/Hopf_Fibration.png/500px-Hopf_Fibration.png" alt="" style="width:80%; max-width: 400px; height:auto;">
<figcaption>Figure 1: The hopfy caption of the figure</figcaption>
</figure>
</center>

## Formulas

a $a \text{<} b$

## LaTeX punctuation

In view of Rembrandt, involutions on topological spaces are equivalently known as *[[topological G-spaces]]* for $G = $[[cyclic group of order 2|$\mathbb{Z}/2$]]. The 

<a href="http://ncatlab.org/nlab/show/HomePage"><div style="float:right;margin:0 20px 10px 20px;"><img width = "250" src="http://i.stack.imgur.com/1hvpz.png" alt="nLab banner" /></div></a>


