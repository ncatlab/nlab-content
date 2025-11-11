[[!redirects reader monad]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In a [[cartesian closed category]]/[[type theory]] $\mathcal{C}$, given any [[object]]/[[type]] $B$ there is a [[monad]]

$$
  Maps(B,-) \colon \mathcal{C} \to \mathcal{C}
$$

given by forming the [[internal hom]] out of $B$, hence the "space of functions" out of $B$. This is sometimes called the _function monad_.  Its [[unit of a monad|unit]] is given by sending values to [[constant functions]] with that value, and the monad operation is given by evaluating on the [[diagonal]].

In the context of [[monads in computer science]] this monad is called the _reader monad_ or _environment monad_. It serves to write programs in which all operations may "read in" a state of type $B$ (an "environment" variable).

## Definition
 {#Definition}

We first describe the reader monad explicitly

* [in components](#DefinitionInComponents)

as a monad on $\mathcal{C} =$ [[Sets]].

Then we describe it, more generally as the monad induced by a right [[base change]] [[adjoint functor|adjunction]]

* [via base change](#DefinitionViaBaseChange).

In this form the construction makes more sense  generally (see for instance the *[[quantum reader monad]]*).

We write 

$$
  Maps(-,-) 
    \;\colon\; 
  \mathcal{C}^{op} 
    \times
  \mathcal{C}
    \longrightarrow
  \mathcal{C}
$$

for the corresponding [[internal hom]]. In [[Sets]] this is the operation of forming [[function sets]].

\linebreak

Fix $B \in \mathcal{C}$. 


### In components
 {#DefinitionInComponents}


1. The [[underlying]]-[[functor]] of the $B$-reader monad is

   $$
     \bigcirc_B \;\colon\; D \;\mapsto\; Maps(B,D)
     \,.
   $$

1. The [[unit of a monad|unit of the monad]] is given by constructing [[constant functions]]:

   $$
     \begin{array}{ccc}
       D 
       &
         \xrightarrow{
           \;\;
           \eta^{\bigcirc_B}_D
           \;\;
         }
       &
       Maps(B,D)
       \\
       d 
       &\mapsto&  
      \big(
         b \;\mapsto\; d
      \big)
      \mathrlap{ \;=\; const_d }
     \end{array}
   $$

1. The monad [[multiplication]] is given by "evaluating [[diagonal map|diagonally]]:

   $$
     \begin{array}{ccc}
       Maps\big(
         B ,\,
         Maps(B,D)
       \big)
       &\xrightarrow{\;\;\; 
          \mu^{\bigcirc_B} 
       \;\;\;}&
       Maps(B,D)
       \\
       f(-)(-)
       &\mapsto&
       \big(
         b
         \;\mapsto\;
         f(b)(b)
       \big)
       \mathrlap{\,.}
     \end{array}
   $$

To check that this definition satisfies the [[monad]]-[[axioms]]:

**[[unitality]]**:

$$
  \begin{array}{ccc}
  Maps(B,D)
  &\xrightarrow{\;\;\;  
     \eta^{\bigcirc_B}_{Maps(D,B)}
  \;\;\;}&
  Maps\big(
    B, Maps(B,D)
  \big)
  &\xrightarrow{\;\;\;
    \mu^{ \bigcirc_B }_{D}
  \;\;\;}&
  Maps(B,D)
  \\
  \big(
    b' \mapsto f(b')
  \big)
  &\mapsto&
  \Big(
    b \mapsto 
    \big(
      b' \mapsto f(b')
    \big)
  \Big)
  &\mapsto&
  \big(
    b \mapsto f(b)
  \big)
  \end{array}
$$

and

$$
  \begin{array}{ccc}
  Maps(B,D)
  &\xrightarrow{\;\;\;  
     Maps\big(
       B,
       \eta^{\bigcirc_B}_{D}
     \big)
  \;\;\;}&
  Maps\big(
    B, Maps(B,D)
  \big)
  &\xrightarrow{\;\;\;
    \mu^{ \bigcirc_B }_{D}
  \;\;\;}&
  Maps(B,D)
  \\
  \big(
    b \mapsto f(b)
  \big)
  &\mapsto&
  \Big(
    b \mapsto 
    \big(
      b' \mapsto f(b)
    \big)
  \Big)
  &\mapsto&
  \big(
    b \mapsto f(b)
  \big)
  \end{array}
$$

**[[associativity]]**:

$$
  \begin{array}{ccc}
    Maps\Big(
      B,
      Maps\big(B,
        Maps(B,D)
      \big)
    \Big)
    &\xrightarrow{\;\;\;
      \mu^{\bigcirc_B}_{
        Maps(B,D)
      }
    \;\;\;}&
    Maps\big(B,
      Maps(B,D)
    \big)
    &\xrightarrow{\;\;\;
      \mu^{\bigcirc_B}_{
        D
      }
    \;\;\;}&
    Maps(B,D)
    \\
    \Big(
      b \mapsto
      \big(
        b' \mapsto 
        (b'' \mapsto f(b, b', b''))
      \big)
    \Big)
    &\mapsto&
    \big(
      b' \mapsto 
      (b'' \mapsto f(b', b', b''))
    \big)
    &\mapsto&
    \big( 
      b'' \mapsto f(b'', b'', b'')
    \big)
  \end{array}
$$

and

$$
  \begin{array}{ccc}
    Maps\Big(
      B,
      Maps\big(B,
        Maps(B,D)
      \big)
    \Big)
    &\xrightarrow{\;\;\;
      Maps\big(
        B,
        \mu^{\bigcirc_B}_{
          D
        }
      \big)
    \;\;\;}&
    Maps\big(B,
      Maps(B,D)
    \big)
    &\xrightarrow{\;\;\;
      \mu^{\bigcirc_B}_{
        D
      }
    \;\;\;}&
    Maps(B,D)
    \\
    \Big(
      b \mapsto
      \big(
        b' \mapsto 
        (b'' \mapsto f(b, b', b''))
      \big)
    \Big)
    &\mapsto&
    \big(
      b' \mapsto 
      (b'' \mapsto f(b', b'', b''))
    \big)
    &\mapsto&
    \big( 
      b'' \mapsto f(b'', b, b)
    \big)
  \end{array}
$$


### Via base change
 {#DefinitionViaBaseChange}

For $B \in Sets$, write $\mathcal{C}_B$ for the category of $B$-[[indexed sets]] $(D_b)_{b \colon B}$ of [[objects]] of $\mathcal{C}$. (More generally, if $\mathcal{C}$ is a [[locally cartesian closed category]] ([[categorical semantics for dependent type theory]]), take $\mathcal{C}_B$ be the [[slice category]] over $B$.)

The right [[base change]] [[adjoint functor|adjunction]] ([[context extension]] $\dashv$ [[dependent product]]) is

$$
  \begin{array}{ccc}
    \mathcal{C}_B
    &
      \underoverset
        {\underset{(p_B)_\ast = \prod_{B}}{\longrightarrow}}
        {\overset{ (p_B)^\ast }{\longleftarrow}}
        {\;\;\; \bot \;\;\;}
    &
    \mathcal{C}
    \\
    (D_b)_{b \colon B}
    &\mapsto&
    \prod_{b \colon B} D_b
  \end{array}
$$


Under the evident identification of [[maps]] $f \colon B \to D$ with [[tuples]] $\big( f(b) \big)_{b \colon B}$, the reader monad is the monad induced from this [[adjoint pair|adjunction]]:

$$
  \bigcirc_B
  \;\simeq\;
  (p_B)_\ast
  (p_B)^\ast
  \,.
$$



\begin{remark}
One may also think of this as being the [[polynomial functor]] associated with this span:

$$
  \ast \leftarrow B \rightarrow \ast \rightarrow \ast
  \,.
$$
\end{remark}
\begin{remark}
The [[comonad]] obtained by composing the other way around, $(p_B)^\ast (p_B)_\ast$, is the [[modal operator]] usually called _[[necessity]]_
\end{remark}

From the [[universal property]] of the [[Cartesian product]], one finds that:

The **[[adjunction unit]]** is

$$
  \begin{array}{ccc}
    b \colon B
    \; \vdash \;
    &
    D 
    &\xrightarrow{\;\;\;
      id_D
    \;\;\;}& 
    D
    \\
    && \updownarrow
    \\
    &
    D
    &\xrightarrow{\;\;\;
      \eta^{ \bigcirc_B }_D
    \;\;\;}&
    \prod_{b \colon B} D
    \\
    &
    d &\mapsto& (d, \cdots, d)
  \end{array}
$$

The **[[adjunction counit]]** is:

$$
  \begin{array}{ccc}
    &
    \prod_{b' \colon B} 
    D_{b'}
    &\xrightarrow{\;\;\;
      id
    \;\;\;}& 
    \prod_{b' \colon B} 
    D_{b'}
    \\
    && \updownarrow
    \\
    b \colon B
    \;\dashv\;
    &
    \prod_{b' \colon B} 
    D_{b'}
    &\xrightarrow{\;\;\;
      \epsilon^{ \star_B }_D
    \;\;\;}&
    D_{b}
    \\
    &
    (d_{b'})_{b' \colon B} 
    &\mapsto& 
    d_{b}
  \end{array}
$$

The adjunction unit is clearly the [[unit of a monad|monad unit]].

The adjunction counit gives the [[multiplication]] on the monad:

$$
  \begin{array}{ccc}
    \prod_{b \colon B}
    (p_B)^\ast
    \prod_{b' \colon B}
    (p_B)^\ast
    D
    &\xrightarrow{\;\;\;
      \prod_{b \colon B}
      \big(
         \epsilon^{\star_B}
      \big)
      (p_B)^\ast
    \;\;\;}&
    \prod_{b' \colon B}
    (p_B)^\ast
    C
    \\
    \big(
      (f_{b'})_{b}
    \big)_{b', b \colon B}
    &\mapsto&
    \big(
      (f_{b})_{b}
    \big)_{b \colon B}    
  \end{array}
$$



## Properties


### Relation to coreader- and state monad
 {#RelationToCoreaderAndState}

In a [[cartesian closed category]]/[[type theory]] $\mathcal{C}$, the reader monad $[B,-] \colon \mathcal{C}\to \mathcal{C}$ is [[right adjoint]] to the [[coreader comonad]] $B\times (-)$.

The composite of [[coreader comonad]] followed by [[reader monad]] is the *[[state monad]]* $[B,B \times (-)]$
This monad models the situation where a program may not only depend on a immutable parameter $b \colon B$ but may be allowed to *change* it.

Just as the [[coreader comonad]] canonically becomes a monad when $B$ is a [[monoid]], so the reader monad becomes a comonad in that case, and then it is sometimes called the "traced comonad".


### Relation to random variables in probability theory
 {#RelationToRandomVariables}

It makes sense to think of $[B,-]$ as producing spaces of [[random variables]] ([Verdier 14](#Verdier14)) depending on [[possible worlds]] $b \in B$ &lbrack;[Toronto & McCarthy 10b, slide 24](#TorontoMcCarthy10b)&rbrack;. 

(While, from the perspective of [[modal type theory]], its siblings $W^\ast \prod_W$ and $W^\ast \sum_W$ may be called _[[necessity]]_ and _[[possibility]]_, respectively).

>  The intuition behind the Reader monad, for a mathematician, is perhaps stochastic variables. A stochastic variable is a function from a probability space to some other space. So we see a stochastic variable as a monadic value. &lbrack;[Verdier 14](#Verdier14)&rbrack;

> you could interpret this by regarding random variables as reader monad computations. &lbrack;[Toronto & McCarthy 10b, slide 35](#TorontoMcCarthy10b)&rbrack;

[Toronto & McCarthy 10a, 2.2](#TorontoMcCarthy10a), [Toronto 14, 6.2](#Toronto14) call the function monad the _random variable idiom_.

This is also brought out by the relation of *linear* reader algebras to [[quantum measurement]], see [below](#QuantumReaderMonad). For more see also at *[[nondeterministic computation]]* the section *[Via indefiniteness effects](nondeterministic+computation#FormalizationViaIndefinitenessEffects)*.


### Free modules over the reader monad
 {#FreeModules}

For $B$ a [[set]], the [[Kleisli category]] for the $B$-reader monad has $B$-[[tuples]] of [[functions]] as [[morphisms]]:


\begin{imagefromfile}
    "file_name": "KleisliCatOfReaderMonad-221108.jpg",
    "width": "600",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}



(On the left we are showing the situation of the [[comparison functor]] and on the right we are using the ["bind"-notation](monad+in+computer+science#BasicIdea) from [[monads in computer science]].)

### General modules over the reader monad
 {#AlgebrasForTheReaderMonad}

An [[algebra over a monad|algebra]] of the reader monad on an object $A$ consists of a single operation $r : A^B \to A$ subject to a constancy law $r(\lambda b. a) = a$ and a diagonal law $r(\lambda b. r(\lambda b'. a(b,b'))) = r(\lambda b. a(b,b))$. This algebraic structure captures equations for a [[computational effect]] of being able to query a fixed global parameter of type $B$, hence the name "reader monad". The operation $r$ is interpreted as "reading the parameter $B$ and using it to decide how to proceed". The constancy law says that reading the parameter itself is not observable and the diagonal law says that if we read the parameter multiple times we get the same answer. See (See also [MO:a/868317](https://math.stackexchange.com/a/868317/58526).) for a further discussion of the algebras.

A special case is when $B$ is a 2 element set, where the $B$-reader algebras on $Set$ correspond to [[idempotent]] [[semigroups]], also known as _[[rectangular band|rectangular bands]]_. 

But the definition of the reader monad makes sense also for other [[hyperdoctrines]] such as for [[dependent linear types]]: For the resulting "linear" or "quantum" version of the reader monad the situation is different, see  [below](#QuantumReaderMonad).


## Examples

### Quantum reader monad
 {#QuantumReaderMonad}


As remarked [above](#AlgebrasForTheReaderMonad), while the $B$-[[reader monad]] on [[toposes]] such as [[Set]] is induced from the [[base change]] [[adjunction]] as $\bigcirc_B(-) \,\coloneqq\, \underset{B}{\prod} \big( B \times (-) \big)$, the functor $\underset{B}{\prod} \;\colon\; Set_{/B} \xrightarrow{\phantom{--}} Set$ is *not* in general a [[monadic functor]], so that $B$-reader-[[algebras over a monad|algebras]] are not in general [[equivalence of categories|equivalent]] to $B$-[[indexed sets]].

However, this situation changes for $B$-readers analogously defined in other [[hyperdoctrines]]. 

We discuss the example of the reader monad induced by  $B$-[[dependent linear types]] which have [[biproducts]], such as $B$-[[indexed sets]]  of [[vector spaces]] (these we may think of as "[[quantum reader monad|quantum reader monads]]", see the discussion at *[Quantum Modal Logic](necessity+and+possibility#ModalQuantumLogic)*). We follow [CQTS (2022)](#CQTS22):

\begin{proposition}
\label{QuantumBReaderAlgebrasAreBDependentLinearTypes}
**(quantum $\bigcirc_B$-algebras are $B$-[[dependent linear types]])**
\linebreak
For $B \;\in\;$ [[FiniteSets]], the [[category]] of [[algebra over a monad|algebras]] for the $B$-[[reader monad]]

$$
  \array{
    \bigcirc_B 
    \colon
    &
    Vect 
    &\xrightarrow{\phantom{---}}&
    Vect 
    \\
    &
    \mathscr{H}
    &\mapsto&
    Maps\big(B, \mathscr{H} \big)
    \mathrlap{
      \;
      \simeq
      \;
      \underset{b \colon B}{\bigoplus}
      \mathscr{H}
    }
  }
$$

on the category [[Vect]] of [[vector spaces]] (over any given [[ground field]]) is [[equivalence of categories|equivalent]] to that of [[vector bundles]] over $B$ (hence to $B$-[[indexed sets]] of [[vector spaces]]):
$$
  EM\big(
    \bigcirc_B 
  \big)
  \;\;\simeq\;\;
  Vect_B
  \,.
$$

\end{proposition}
\begin{proof}
 We state first an abstract proof and then a concrete proof.

Abstractly, observe that [[Vect]] has (finite) [[biproducts]] (given by the [[direct sum]] of vector spaces) which together with the assumption that $B$ is [[finite set|finite]] implies that $\underset{B}{\prod} \;\colon\; Vect_B \xrightarrow{\;} Vect$:

1. is not only a [[right adjoint]] but also a [[left adjoint]] (hence an [[ambidextrous adjunction|ambidextrous adjoint]] to [[pullback of vector bundles]] along $B \to \ast$), [[left adjoints preserve colimits|hence]] in particular it [[preserved colimit|preserves]] all [[colimits]];

1. is a [[conservative functor]] (since the $B$-components of any morphism of vector bundles over $V$ can still be extracted via ([[coprojection|co-]])[[projections]] from their image under forming the [[biproduct]] over $B$).

Therefore the conditions for the [[monadicity theorem]] are met (see [there](monadicity+theorem#CrudeMonadicityTheorem)), implying that the functor is [[monadic functor]], which in turn implies the claim.

\linebreak

Alternatively, we now check the claim more concretely by unwinding what it means for a vector space to carry $\bigcirc_B$-algebra structure and for a linear map between vector spaces to be a [[homomorphism]] for this structure:

First observe that the $\bigcirc_B$-[[monad]] product $\mu \;\colon\; \bigcirc_B \bigcirc_B \xrightarrow{\mu} \bigcirc_B$ on a [[vector space]] $\mathscr{H} \,\in\, Vect$ is explicitly given by:

$$
  \array{
  \underset{b \colon B}{\bigoplus}
  \;
  \underset{b' \colon B}{\bigoplus}
  \;
  \mathscr{H}
  &
  \xrightarrow{\;\; \mu^{\bigcirc}_{\mathscr{H}} \;\;}
  &
  \underset{b'' \colon B}{\bigoplus}
  \mathscr{H}
  \\
  \big(
     \psi_{b,b'}
  \big)_{b,b' \colon B}
  &\mapsto&
  \big(
    \psi_{b'' ,b''}
  \big)_{b'' \colon B}
  }
$$

and that a $\bigcirc_B$-algebra structure on $\mathscr{H}$ is a [[linear map]] of this form:

\[
  \label{MapsUnderlyingAlgebraStructureOverLinearReaderMonad}
  \rho^\bigcirc_{\mathscr{H}}
  \;\colon\;
  \underset{b \colon B}{\oplus}
  \mathscr{H}
  \xrightarrow{\phantom{-}(P_b)_{b \colon B}\phantom{-}}
  \mathscr{H}  
  \,.
\]

Of such maps, the $\bigcirc_B$-action property ([here](algebra+over+a+monad#eq:ActionProperty)) demands that the following two linear maps are equal:

$$
  \array{    
    &
    \underset{b \colon B}{\bigoplus}
    \;
    \underset{b' \colon B}{\bigoplus}
    \;
    \mathscr{H}
      &\xrightarrow{\; \mu^\bigcirc_{\mathscr{H}}  \;}&
    \underset{b'' \colon B}{\bigoplus}
    \mathscr{H}
      &\xrightarrow{\; \rho^\bigcirc_{\mathscr{H}} \;}&  
    \mathscr{H}
    \\
    &
    \big(
       \psi_{b,b'}
    \big)_{b,b' \colon B}    
    &\mapsto&
    \big(
       \psi_{b'',b''}
    \big)_{b'',b'' \colon B}    
    &\mapsto&
    \underset{b'' \colon B}{\sum}
    P_{b''}(\psi_{b'',b''})
    \\
    \text{and}
    &
    \\
    &
    \underset{b \colon B}{\bigoplus}
    \;
    \underset{b' \colon B}{\bigoplus}
    \;
    \mathscr{H}
      &\xrightarrow{\; \bigcirc \rho^\bigcirc_{\mathscr{H}}  \;}&
    \underset{b'' \colon B}{\bigoplus}
    \mathscr{H}
      &\xrightarrow{\; \rho^\bigcirc_{\mathscr{H}} \;}&  
    \mathscr{H}
    \\
    &
    \big(
       \psi_{b,b'}
    \big)_{b,b' \colon B}    
    &\mapsto&
    \big(
       \underset{b \colon B}{\sum}
       P_{b}(\psi_{b,b'})
    \big)_{b' \colon B}    
    &\mapsto&
    \underset{b, b' \colon B}{\sum}
    P_{b'}\big(P_{b}(\psi_{b,b'})\big)
    \mathrlap{\,.}
  }
$$

By considering the value of these maps on [[tuples]] of [[vectors]] $\big(\psi_{b,b'}\big)_{b,b' \colon B}$ which are non-[[zero]] only for single elements $(b,b') \in B \times B$ one finds that the above condition is equivalent to the following condition:

$$
  \underset{
    b, b' \colon B
  }{
    \forall
  } 
  \;\;\;\; 
    P_b \circ P_{b'} 
  \;=\; 
  \left\{
    \array{
      P_b &\text{if} \; b = b'
      \\
      0  & \text{otherwise}
      \,.
    }
  \right.
$$

Moreover, the $\bigcirc_B$-[[unit of a monad|unit]] $\id \xrightarrow{\;\; \eta^{\bigcirc_B} \;\;} \bigcirc_B$ is given by the [[diagonal map]] into the [[biproduct]]

$$
  \array{
    \mathscr{H}
    &\xrightarrow{\;\;
      \eta^{\bigcirc_B}_{\mathscr{H}}
    \;\;}
    &
    \underset{b \colon B}{\bigoplus}
    \mathscr{H}
    \\
    \psi
    &\mapsto&
    (\psi_b \coloneqq \psi)_{b \colon B}
  }
$$

so that the unitality property ([here](algebra+over+a+monad#eq:UnitProperty)) of the $\bigcirc_B$-algebra structure $(P_b)_{b \colon B}$ demands equivalently that the [[composition|composite]]

$$
  \array{
    \mathscr{H}   
    &\xrightarrow{\; \eta^{\bigcirc_B}_{\mathscr{H}} \;}&
    \underset{b \colon B}{\bigoplus}
    \mathscr{H}
    &\xrightarrow{\; \rho^{\bigcirc_B}_{\mathscr{H}} \;}&
    \mathscr{H}
    \\
    \psi
    &\mapsto&
    \big( 
      \psi
    \big)_{b \colon B}
    &\mapsto&
    \underset{b \colon B}{\sum}
    \;
    P_b(\psi)
  }
$$

is the [[identity function]] on $\mathscr{H}$, hence that this system of [[projection operators]] is "complete" in that

$$
  \underset{b \colon B}{\bigoplus} P_b
  \;=\;
  id_{\mathscr{H}}
  \,.
$$


In summary, this means that for $B$-[[tuples]] of [[linear maps]] $(P_b \colon \mathscr{H} \to \mathscr{H})_{b \colon B}$ as in (eq:MapsUnderlyingAlgebraStructureOverLinearReaderMonad) to constitute a $\bigcirc_B$-module structure is equivalent to them being
systems of orthogonal linear [[projection operators]], whose [[images]] 

$$
  \mathscr{H}_b \;\coloneqq\; im(P_b) \;\subset\; \mathscr{H}
$$

[[linear span|span]]$\;$ $\mathscr{H}$ under [[direct sum]]:

$$
  \mathscr{H}
  \;\simeq\;
  \underset{b \colon B}{\bigoplus}
  \mathscr{H}_b
  \,.
$$

Such structures, of course, are exactly the images under the right [[base change]] $\underset{B}{\prod} \;\colon\; Vect_B \longrightarrow{\;} Vect$ of $B$-[[indexed sets]] of vector spaces.

Finally, the [[homomorphism]]-property on a [[linear map]] $\mathscr{H} \xrightarrow{\phi} \mathscr{H}'$ between the underlying vector spaces of two such $\bigcirc_B$-modules demands that the following [[commuting diagram|diagram commutes]]:

$$ 
  \array{
    \underset{b \colon B}{\bigoplus}
    \mathscr{H}
    &\xrightarrow{\;\;\;
      \underset{b \colon B}{\oplus}
    \;\;\;}&
    \underset{b \colon B}{\bigoplus}
    \mathscr{H}
    \\
    \mathllap{
      {}^{
      \big(
        P_b 
      \big)_{b \colon B}
      }
    }
    \big\downarrow
    &&
    \big\downarrow
    \mathrlap{
      {}^{
      \big(
        P'_b 
      \big)_{b \colon B}
      }
    }
    \\
    \mathscr{H}
    &
    \underset{\phantom{---} \phi \phantom{---} }
      {\longrightarrow}
    &
    \mathscr{H}'
    \,.
  }
$$ 

The $B$-indexed components of this condition require that $\phi$ [[commutator|commutes]] with all these [[projection operators]], in that

$$
  b \colon B
  \;\;\;\;
  \vdash
  \;\;\;\;
  P'_b \circ \phi
  \;=\;
  \phi \circ P_b
  \,.
$$

But this evidently means that $\phi$ itself is the image under the [[direct sum]]-[[functor]] 
$$
  \phi
  \;=\;
  \underset{b \colon}{\oplus}
  \phi_b
$$
of a $B$-[[tuple]] of [[linear maps]] between the $B$-indexed component spaces:
$$
  b \colon B
  \;\;\;
  \colon
  \;\;\;
  \mathscr{H}_b \longrightarrow \mathscr{H}'
  \,.
$$
This is the defining property of morphisms in $Vect_B$ and hence shows that $\bigcirc_B$-algebra homomorphisms are equivalently morphisms of $B$-[[indexed sets]] of vector spaces, hence that the two [[categories]] are [[equivalence of categories|agree]].
\end{proof}

\begin{example}\label{FreeQuantumReaderAlgebras}
**(free quantum $\bigcirc_B$-algebras and quantum measurement bases)**
\linebreak
  The *[free](algebra+over+a+monad#FreeAlgebras)* $\bigcirc_B$-algebras in [[Vect]] are those whose underlying vector space is of the form $\bigcirc_B \mathscr{B} = \underset{b \colon B}{\bigoplus} \mathscr{B}$ for any $\mathscr{B} \,\in \, Vect$, hence, under the equivalence of Prop. \ref{QuantumBReaderAlgebrasAreBDependentLinearTypes}, are those $B$-[[dependent linear types]] which happen to assign the same vector space $\mathscr{B}$ for all $b \colon B$.

But [[homomorphisms]] of such free $\bigcirc_B$-algebras are still allowed to be non-trivially $B$-dependent families of linear maps. This is directly a special case of Prop. \ref{QuantumBReaderAlgebrasAreBDependentLinearTypes} but is also immediate under the [Kleisli equivalence](Kleisli+category#KleisliEquivalence) from observing that $\bigcirc_B$-[[Kleisli morphisms]] are of the following form: 
$$
  \array{
    \mathscr{B}
    &\xrightarrow{
      \big(
        \phi_b
      \big)_{b \colon B}
    }&
    \underset{b \colon B}{\bigoplus}
    \mathscr{B}'
    \,.
  }
$$

In [[quantum information theory]] the $\bigcirc_B$-algebras in [[complex vector spaces]] which are free on the [[tensor unit]] $\mathbb{C} \,\in\, \mathbb{C} Vect$ (the [[dimension of a vector space|1-dimensional]] [[complex vector space]]) play the role of  ([[finite dimensional vector space|finite dimensional]] [[complex vector spaces]] [[underlying]]) [[Hilbert space]] [[space of quantum states|of quantum states]] which are [[linear space|spanned]] by the set $B$ regarded as a "[[quantum measurement]] [[linear basis|basis]]".

For example, the [[dependent linear type]] of [[qbits]] is the free $\bigcirc_B$-algebra $\bigcirc_{Bool} \mathbb{C}$ spanned by the [[intuitionistic type theory|classical type]] [[Bool]] $= \{0,1\}$ of [[bits]], reflecting the two canonical [[quantum measurement]]-outcomes ($\vert 0\rangle$, $\vert 1 \rangle$) of [[qbits]]. 


{#QuantumMeasurementAsIndefinitenessHandling} Curiously, from this one finds that *[[quantum measurement]] is exactly indefiniteness handling*

where 

* "indefiniteness" is understood as the the effect/[[modality]] expressed by the reader monad $\bigcirc_B$ (see [here](necessity+and+possibility#RelationToPotentiality)),

* "handling" is understood as *effect handling* in the sense of effect-[[monads in computer science]] (see [here](monad+in+computer+science#MonadModulesInIdeaSection));

namely:

\begin{imagefromfile}
    "file_name": "QMeasurementViaIndefinitenessHandling-221109c.jpg",
    "width": "730",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


Notice that this process may be understood as the "[[dynamic lifting]]" of [[quantum measurement]]-results into the [[context]] (here: $B = $ [[Bool]]) of the ambient [[dependent linear type theory]].

For more on this see at *[[quantum circuits via dependent linear types]]*.
\end{example}

\linebreak

This naturally relates to the discussion of [[quantum measurement]] via [[Frobenius algebra]]-structures which is popular in the context of [[quantum information theory via dagger-compact categories]] -- as follows:

\begin{remark}\label{QuantumrReaderMonadIsFrobenius}
**(quantum reader monad is Frobenius)**
\linebreak
Since the [[direct sum]] of [[vector spaces]] is a [[biproduct]] and using our running assumption that $B$ is a [[finite set]], it follows that the [[underlying]] [[functor]] of the quantum [[reader monad]] from Prop. \ref{QuantumBReaderAlgebrasAreBDependentLinearTypes} coincides with that of the [[coreader comonad]], and hence that the quantum reader monad is a *[[Frobenius monad]]* (see there).
\end{remark}

\begin{remark}\label{QuantumReaderMonadIsSpecialFrobeniusWriterMonad}
**(quantum reader monad is special Frobenius writer monad)**
\linebreak
  Consider the $B$-[[indexed set|indexed]] the [[direct sum]] $k^{\otimes^B}$ of the [[ground field]] with itself as a $k$-[[associative algebra|algebra]] and write

$$
  {k^{\otimes^B}}\text{-}Writer
  \;\colon\;
  Vect \to Vect
$$

for the [[writer monad]] corresponding to this [[monoid object]] in [[Vect]]: The monad which acts by forming the [[tensor product]] $Writer_{k^{\otimes^B}}(V) \;\coloneqq\; V \otimes \big( k^{\otimes^B} \big) $ and whose monad multiplication and [[unit of a monad]] are induced from the [[multiplication]] and [[unit]] in this monoid.

The above proof of Prop. \ref{QuantumBReaderAlgebrasAreBDependentLinearTypes} shows at once that this [[writer monad]] is [[isomorphism|isomorphic]] to the $B$-reader monad:
$$
  \bigcirc_B
  \;\simeq\;
  Writer_{k^{\otimes^B}}
  \,.
$$ 
Now the [[module over a monad|monad modules]] over a [[writer monad]] are just the ordinary [[modules]] over the corresponding [[monoid]], so that 
$$
  \bigcirc_B Mod(Vect)
  \;\simeq\;
  \big(
    k^{\otimes^B} 
  \big)Mod(Vect)
  \,.
$$
This provides a rather transparent re-derivation of and alternative perspective on Example \ref{FreeQuantumReaderAlgebras}.


[[formal duality|Dually]], as in Prop. \ref{QuantumReaderMonadIsFrobenius}, the quantum [[coreader comonad]] is isomorphic to the [[coreader comonad]] corresponding to the [[coalgebra]]-[[structure]] on $k^{\otimes^B}$.
Hence, as a [[Frobenius monad]] (Prop. \ref{QuantumReaderMonadIsFrobenius}), the quantum reader corresponds to $k^{\otimes^B}$ regarded as a [[Frobenius algebra]], in fact as a commutative and special Frobenius algebra. In this form the quantum  reader monad is prominent in the literature on [[quantum information theory via dagger-compact categories]] &lbrack;[Coecke & Pavlović (2008), §1.5.1](#CoeckePavlović08), [Coecke & Paquette (2008), §2.3](#CoeckePaquette08)&rbrack;.
\end{remark}

\[
  \label{EquivalencesOfTheQuantumReaderMonad}
\]
\begin{imagefromfile}
    "file_name": "QuantumReaderFrobeniusMonad-221112.jpg",
    "width": "600",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}



## Related concepts

[[!include reader-writer (co)monads -- table]]

* [[state monad]]

* [[quantum reader monad]]

* [[maybe monad]]

* [[continuation monad]]



## References

### General

As a [[monad in computer science]]:

* {#Verdier14} [[Olivier Verdier]], _[The Reader and Writer Monads and Comonads](http://www.olivierverdier.com/posts/2014/12/31/reader-writer-monad-comonad/)_, 2014

* {#Milewski19} [[Bartosz Milewski]] §21.2.3 in: *Category Theory for Programmers*, Blurb (2019) &lbrack;[pdf](https://github.com/hmemcpy/milewski-ctfp-pdf/releases/download/v1.3.0/category-theory-for-programmers.pdf), [github](https://github.com/hmemcpy/milewski-ctfp-pdf), [webpage](https://bartoszmilewski.com/2014/10/28/category-theory-for-programmers-the-preface/), [ISBN:9780464243878](https://www.blurb.com/b/9621951-category-theory-for-programmers-new-edition-hardco)&rbrack;


* [[Tarmo Uustalu]], p.22 of: *Monads and Interaction Lecture 1* &lbrack;[pdf](https://cs.ioc.ee/~tarmo/mgs21/mgs1.pdf), [[Uustalu-Monads1.pdf:file]]&rbrack;, lecture notes for [MGS 2021](https://staffwww.dcs.shef.ac.uk/people/G.Struth/mgs21.html) (2021):


See also:

* Wikipedia, _[Environment monad](http://en.wikipedia.org/wiki/Monad_%28functional_programming%29#Environment_monad)_.

* {#TorontoMcCarthy10a} [[Neil Toronto]], [[Jay McCarthy]], _From Bayesian notation to pure Racket, via measuretheoretic probability_ , in _Implementation and Application of Functional Languages_, 2010 ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.298.4274))

* {#TorontoMcCarthy10b} [[Neil Toronto]], [[Jay McCarthy]], _From Bayesian Notation to Pure Racket_, talk notes 2010 ([pdf](http://jeapostrophe.github.io/home/static/toronto-2010ifl-slides.pdf))

* {#Toronto14} [[Neil Toronto]], _Useful Languages for Probabilistic Modeling and Inference_, PhD Thesis, 2014 ([pdf](http://cs.umd.edu/~ntoronto/papers/toronto-2014diss.pdf), [slides](http://cs.umd.edu/~ntoronto/papers/toronto-2014diss-slides.pdf))



A treatment of _opacity_ in [[linguistics]] via the function monad

* [[Gianluca Giorgolo]], [[Ash Asudeh]], _Monads as a Solution for Generalized Opacity_, [paper](https://www.aclweb.org/anthology/W14-1403/)

* [[Gianluca Giorgolo]], [[Ash Asudeh]], _Perspectives_, Semantics and Pragmatics, vol. 9, [paper](http://semprag.org/article/view/sp.9.21)



### On linear types
 {#ReferencesOnLinearTypes}

The [[quantum reader monad]] -- implicitly, in its incarnation as the $k^B$-DualWriter monad -- is highlighted in the literature [[quantum information theory via dagger-compact categories]] as formalizing "classical structures" (namely linear bases for [[quantum measurement]]):

* {#CoeckePavlović08} [[Bob Coecke]], [[Duško Pavlović]], §1.5.1 of: *Quantum measurements without sums*, in [[Louis Kauffman]], [[Samuel Lomonaco]] (eds.), *Mathematics of Quantum Computation and Quantum Technology*, Taylor & Francis (2008) 559-596 &lbrack;[arXiv:quant-ph/0608035](https://arxiv.org/abs/quant-ph/0608035), [doi:10.1201/9781584889007](https://doi.org/10.1201/9781584889007)&rbrack;

* {#CoeckePaquette08} [[Bob Coecke]], [[Eric Oliver Paquette]], §2.3 in: *POVMs and Naimark's theorem without sums*, Electronic Notes in Theoretical Computer Science **210** (2008) 15-31 &lbrack;[arXiv:quant-ph/0608072](https://arxiv.org/abs/quant-ph/0608072), [doi:10.1016/j.entcs.2008.04.015](https://doi.org/10.1016/j.entcs.2008.04.015)&rbrack;

* [[Bob Coecke]], [[Eric Paquette]], [[Dusko Pavlovic]], Def. 2.8 in: *Classical and quantum structures* (2008) &lbrack;[pdf](http://www.comlab.ox.ac.uk/files/627/RR-08-02.pdf), [[Coecke-Paquette-Pavlovic-CQS.pdf:file]]&rbrack;


The account above follows:

* {#CQTS22} [[CQTS]], *[Quantum Data Types via Linear HoTT](https://ncatlab.org/schreiber/show/QDataInLHoTT#QTML2022)*, talk at *[Workshop on Quantum Software](https://quasar.unina.it/qtml2022/workshop.php)* @ *[QTML 2022](https://quasar.unina.it/qtml2022.html)* (Nov 2022) &lbrack;[pdf](/schreiber/files/QuantumDataInLHoTT-221117.pdf)&rbrack;



[[!redirects reader monads]]

[[!redirects function monad]]
[[!redirects function monads]]

[[!redirects environment monad]]
[[!redirects environment monads]]