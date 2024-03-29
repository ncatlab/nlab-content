
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The _state monad_ is the name for the [[monad in computer science]] which is used to implement the functionality of read/write on a global "mutable state" (a global variable) in the context of [[functional programming languages]].

A [[functional program]] with 

1. input of ([[data type|data-]])[[type]] $X$, 

1. output of [[type]] $Y$ 

1. and "mutable state" of [[type]] $W$ 

   (e.g. the state of a "random access memory" device, cf. [Yates (2019), p. 26 & Fig. 1.10](#Yates19)) 

{#IsClearly} is clearly a [[function]] ([[morphism]]) of [[function type]] between the [[product types]] with $W$ (also known as a *[[Mealy machine]]*, see [there](Mealy+machine#MealyMachinesAsEffectfulMaps) and cf. [Oliveira & Miraldo 2016, p. 462](#OliveiraMiraldo16)): 

$$
  prog 
    \;\colon\;
  X \times W 
    \longrightarrow 
  Y \times W
  \,.
$$ 

Now, under the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) of the ([[Cartesian product]] $\dashv$ [[internal hom]])-[[adjoint functor|adjunction]], this is equivalently given by its [[adjunct]], which is a function into the [[function type]] $[-,-]$ ([[internal hom]]):

$$
  X \longrightarrow [W, W \times Y ]
 \,.
$$

Here the operation $[W, W\times (-)]$ is the [[monad]] on the type system which is induced by the above [[adjunction]]; and this latter function is naturally regarded as a morphism in the [[Kleisli category]] of this monad. 

{#RAM} In the context of [[monad (in computer science)|monads in computer science]], this is called the _state monad_ for mutable states of type $W$, such as for a data type $W$ of  Random-Access-Memory:

<center>
<img src="/nlab/files/State-Effectful-Program-230804.jpg" width="600">
</center>


## Definition
 {#Definition}

Concretely, with the [[underlying]] functor being

$$
  W State \;\colon\; D \,\mapsto\, \big[W,\, W \times D \big]
$$

the join operation of the $W$-state monad is given by [[evaluation]] on the intermediate $W$-variable, hence the bind operation is given as follows:

\begin{imagefromfile}
    "file_name": "StateMonadBinding-230828.jpg",
    "width": 750,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

To see more in detail how this encodes access to a global variable $w \colon W$ in the sense of [[programming languages]] consider the following operations which isolate the processes of reading from and writing to that variable, respectively:

$$
  \array{
    read &\colon& W State(W)
    \\
    read &\equiv& w \mapsto (w,w)
  }
  \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
  \array{
    write &\colon& W \to W State(\ast)
    \\
    write &\equiv& w \mapsto (w' \mapsto w)
  }
$$

With these, for instance the procedure 
$$
  \array{
    inc &\colon& \mathbb{N}State(\ast)
    \\
    inc &\equiv& n \mapsto n+1 
  }
$$
which first reads-in the state of a global natural number variable and then overwrites it by its increment may be constructed as shown (on the right in [do-notation](monad+in+computer+science#DoNotation)) here:

\begin{imagefromfile}
    "file_name": "StatefulNumberIncrementInDONotation-230828.jpg",
    "width": 560,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

(This is essentially the example from [Benton, Hughes & Moggi 2002 p. 68 & 71](#BentonHughesMoggi02))


## Properties

### Realization in dependent type theory

In a [[locally Cartesian closed category]]/[[dependent type theory]] $\mathbf{H}$, then to every type $W$ is associated its [[base change]] [[adjoint triple]]

$$
  \mathbf{H}_{/W}
   \stackrel{\overset{\sum_W}{\longrightarrow}}{\stackrel{\overset{W^\ast}{\longleftarrow}}{\underset{\prod_W}{\longrightarrow}}}
  \mathbf{H}
  \,.
$$

In terms of this the state monad is the composite

$$
  State = \prod_W W^\ast \sum_W W^\ast
$$

of [[context extension]] followed by [[dependent sum]], followed by [[context extension]], followed by [[dependent product]].

Here $\prod_W W^\ast = [W,-]$ is called the _[[function monad]]_ or _[[reader monad]]_ and $\sum_W W^\ast = W \times (-)$ is the _[[coreader comonad]]_.


## Related concepts

* [[Mealy machine]]

* [[maybe monad]]

* [[continuation monad]]

* [[function monad]] (reader monad)

* [[coreader comonad]]

* [[writer monad]]

* [[QRAM]]

* [[store comonad]] 


## References 

Original discussion of the state/side-effect monad as a [[monad in computer science]]:

* {#Moggi91} [[Eugenio Moggi]], Exp. 1.1 in: *Notions of computation and monads*, Information and Computation, **93** 1 (1991) &lbrack;<a href="https://doi.org/10.1016/0890-5401(91)90052-4">doi:10.1016/0890-5401(91)90052-4</a>, [pdf](http://www.disi.unige.it/person/MoggiE/ftp/ic91.pdf)&rbrack;


* [[Philip Wadler]], Section 2.3 in: *Monads for functional programming*, in M. Broy (eds.) *Program Design Calculi* NATO ASI Series, **118** Springer (1992) &lbrack;[doi;10.1007/978-3-662-02880-3_8](https://doi.org/10.1007/978-3-662-02880-3_8), [pdf](https://homepages.inf.ed.ac.uk/wadler/papers/marktoberdorf/baastad.pdf)&rbrack;

* {#BentonHughesMoggi02} [[Nick Benton]], [[John Hughes]], [[Eugenio Moggi]], Ex. 42 in: *Monads and Effects*, in: *Applied Semantics*, Lecture Notes in Computer Science **2395**, Springer (2002) 42-122 &lbrack;[doi:10.1007/3-540-45699-6_2](https://doi.org/10.1007/3-540-45699-6_2)&rbrack;

* {#PlotkinPower02} [[Gordon Plotkin]], [[John Power]], Section 3 of: *Notions of computation determine monads* In: M. Nielsen, U. Engberg, (eds.) FOSSACS 2002. LNCS, Lecture Notes in Computer Science **2303**,  Springer (2002) 342-356 &lbrack;[doi:10.1007/3-540-45931-6_24p](https://doi.org/10.1007/3-540-45931-6_24)&rbrack;

Exposition:

* {#Milewski19} [[Bartosz Milewski]], §21.2.5 in: *Category Theory for Programmers*, Blurb (2019) &lbrack;[pdf](https://github.com/hmemcpy/milewski-ctfp-pdf/releases/download/v1.3.0/category-theory-for-programmers.pdf), [github](https://github.com/hmemcpy/milewski-ctfp-pdf), [webpage](https://bartoszmilewski.com/2014/10/28/category-theory-for-programmers-the-preface/), [ISBN:9780464243878](https://www.blurb.com/b/9621951-category-theory-for-programmers-new-edition-hardco)&rbrack;

On the [[module of a monad|modules]] ("algebras") of the state monad:

* [[François Métayer]], *State monads and their algebras* &lbrack;[arXiv:math/0407251](https://arxiv.org/abs/math/0407251)&rbrack;


Concrete applications via implementation in [[Haskell]]:

* {#Yates19} Ryan Yates, *Improving Haskell Transactional Memory* (2019) &lbrack;[hdl:1802/35367](https://hdl.handle.net/1802/35367), [pdf](file:///C:/Users/us13/Downloads/Yates_rochester_0188E_11946.pdf)&rbrack;

Lecture notes:

* [[Tarmo Uustalu]], p.24 of: *Monads and Interaction Lecture 1* &lbrack;[pdf](https://cs.ioc.ee/~tarmo/mgs21/mgs1.pdf), [[Uustalu-Monads1.pdf:file]]&rbrack;, lecture notes for [MGS 2021](https://staffwww.dcs.shef.ac.uk/people/G.Struth/mgs21.html) (2021):


In the generality of the *local* state monad:

* [Plotkin & Power (2002), Sec. 4](#PlotkinPower02)

* [[Paul-André Melliès]], *Local States in String Diagrams*, In: G. Dowek (eds.) *Rewriting and Typed Lambda Calculi* RTA TLCA 2014, Lecture Notes in Computer Science **8560**, Springer (2014) &lbrack;[doi:10.1007/978-3-319-08918-8_23](https://doi.org/10.1007/978-3-319-08918-8_23)&rbrack;

Explicit understanding of [[Kleisli morphisms]] for the state moand as [[Mealy machines]]:

* {#OliveiraMiraldo16} José Nuno Oliveira, Victor Cacciari Miraldo, p. 462 in: *A practical approach to state-based system calculi*, Journal of Logical and Algebraic Methods in Programming **85** 4 (2016) 449-474 &lbrack;[doi:10.1016/j.jlamp.2015.11.007](https://doi.org/10.1016/j.jlamp.2015.11.007)&rbrack;

and (almost):

* {#PeroneKarachalias23} Marco Perone, Georgios Karachalias, *Composable Representable Executable Machines* &lbrack;[arXiv:2307.09090](https://arxiv.org/abs/2307.09090)&rbrack;



[[!redirects state monads]]

[[!redirects local state monad]]
[[!redirects local state monads]]

[[!redirects random access memory]]
[[!redirects random access memories]]

[[!redirects RAM]]
[[!redirects RAMs]]

