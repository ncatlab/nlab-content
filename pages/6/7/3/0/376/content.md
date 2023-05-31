
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category Theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

A **locally cartesian closed category** is a [[category]] $C$ whose [[slice categories]] $C/x$ are all [[cartesian closed category|cartesian closed]]. 

If a locally cartesian closed category $C$ has a [[terminal object]], then $C$ is itself cartesian closed and in fact [[finitely complete category|has all finite limit]]s (because, cartesian products in $C/x$ are pullbacks in $C$); often this requirement is included in the definition.

Equivalently, a locally cartesian closed category $C$ is a category with [[pullbacks]] (and a [[terminal object]], if required) such that each [[base change]] functor $f^*: C/y \to C/x$ has a [[right adjoint]] $\Pi_f$, called the _[[dependent product]]_. (This equivalence is discussed in detail [below](#EquivalentCharacterizations).)

In particular, such pullbacks preserve all [[colimits]]. Therefore, if a locally cartesian closed category [[finitely cocomplete category|has finite colimits]], it is automatically a [[coherent category]] and in fact a [[Heyting category]].


## Properties

### Cartesian closure in terms of base change and dependent product
 {#EquivalentCharacterizations}

We show how the [[dependent product]] and the [[internal hom]] in the [[slice categories]] may be used to express each other.

#### In category theory

+-- {: .num_prop #DependentProductImpliesLocalCartesinClosure}
###### Proposition

Let $\mathcal{C}$ be a [[category]] with [[pullbacks]] that has all [[dependent products]] $\prod_\bullet$,  equivalently that every morphism $f : E \to X$ in $\mathcal{C}$ induces an [[adjoint triple]]

$$
  \mathcal{C}_{/E}
    \stackrel{\overset{\sum_f}{\longrightarrow}}{\stackrel{\overset{f^*}{\longleftarrow}}{\underset{\prod_f}{\longrightarrow}}}
  \mathcal{C}_{/X}
  \,.
$$

Then the [[internal hom]] in a slice $\mathcal{C}_{/X}$ exists and is given by 

$$
  [\langle E \stackrel{f}{\longrightarrow} X\rangle \; ,\;  -]_{\mathcal{C}_{/X}}
  \simeq
  \prod_f \circ f^* 
  \,.
$$


=--

+-- {: .proof}
###### Proof

By the discussion at _[[overcategory]]-[Limits and colimits](overcategory#LimitsAndColimits)_ the product in the slice $\mathcal{C}_{/X}$ of two objects $\langle E_1 \stackrel{f_1}{\longrightarrow} X\rangle$ and $\langle E_2 \stackrel{f_2}{\longrightarrow} X\rangle$ is given by the [[pullback]] $f_1^* E_2 = f_2^* E_1$ in $\mathcal{C}$, regarded again as a morphism over $X$. More formally this means that the product with $\langle E \stackrel{f}{\to} X\rangle $ is given by the composite

$$ 
  (-) \times_{\mathcal{C}_{/X}} \langle E \stackrel{f}{\to} X\rangle
  \;\;\;:\;\;\; 
  \mathcal{C}_{/X}
    \stackrel{f^*}{\to}
  \mathcal{C}_{/E}
    \stackrel{\sum_f}{\to}
  \mathcal{C}_{/X}
$$

of the pullback along $f$ with the [[dependent sum]] along $f$. By the above [[adjoint triple]] both these morphisms have [[right adjoints]] and so the composite of the right adjoints is the right adjoint of the composite, hence is the [[internal hom]]:

$$
  \mathcal{C}_{/X}
    \stackrel{\prod_f}{\leftarrow}
  \mathcal{C}_{/E} 
    \stackrel{f^* }{\leftarrow} \mathcal{C}_{/X}
  \;\;\;:\;\;\;
  [\langle E\stackrel{f}{\to} X \rangle, -]_{\mathcal{C}_{/X}}
  \,.
$$


=--

+-- {: .num_example }
###### Example

In the slice category $Set/X$, the inner hom is explicitly given by
$$ [\langle E \stackrel{f}{\to} X \rangle, \langle F \stackrel{g}{\to} X \rangle]_{Set/X} = \{ (x,h) | x \in X, h : f^{-1}(x) \to g^{-1}(x) \}. $$

=--

+-- {: .num_prop #DependentProductInTermsOfSliceInternalHom}
###### Proposition

If for a [[category]] $\mathcal{C}$ every [[slice category]] is a [[cartesian closed category]], then for every morphism $f : X \to Y$ in $\mathcal{C}$ the [[dependent product]] $\prod_f$ exists and is given on an object $E \stackrel{p}{\to} X$ by the [[pullback]]

$$
  \array{
    \prod_f \langle E \stackrel{p}{\to} X\rangle &\to& [\langle X \stackrel{f}{\to}Y\rangle, \langle E \stackrel{p}{\to}X \stackrel{f}{\to} Y\rangle]_{\mathcal{C}_{/Y}}
    \\
    \downarrow && \downarrow
    \\
    Y &\stackrel{\bar id}{\to}& [\langle X \stackrel{f}{\to}Y \rangle,\langle X \stackrel{f}{\to}Y \rangle]_{\mathcal{C}_{/Y}}
  }
$$

in $\mathcal{C}_{/Y}$, where the bottom morphism is the [[adjunct]] of

$$
  Y \times_{\mathcal{C}_{/Y}} \langle X \stackrel{f}{\to} Y\rangle \simeq \langle X \stackrel{f}{\to}Y\rangle \stackrel{id}{\to} \langle X \stackrel{f}{\to}Y\rangle
  \,.
$$

=--

+-- {: .proof}
###### Proof

It is sufficient to check the $(f^* \dashv \prod_f)$-[[adjunction]] [[hom set]]-[[natural isomorphism]]

$$
  \mathcal{C}_{/Y}( \langle F \stackrel{}{\to} Y\rangle , \prod_f \langle E \stackrel{p}{\to} X\rangle)
  \simeq
  \mathcal{C}_{/X}(f^* \langle F \stackrel{}{\to} Y\rangle, \langle E \stackrel{p}{\to} X\rangle)
  \,,
$$

natural in $\langle F \stackrel{}{\to}Y \rangle$.

Since the [[hom functor]] $\mathcal{C}_{/Y}(\langle F \stackrel{}{\to} Y\rangle, -)$ preserves [[limits]] and hence [[pullbacks]], the expression on the left is exhibited as the pullback

$$
  \array{
    \mathcal{C}_{/Y}(\langle F \stackrel{}{\to} Y\rangle, \prod_f \langle E \stackrel{p}{\to} X\rangle) &\to& 
  \mathcal{C}_{/Y}(\langle F \stackrel{}{\to} Y\rangle, [\langle X \stackrel{f}{\to}Y \rangle,\langle E \stackrel{p}{\to}X \stackrel{f}{\to} Y\rangle]_{\mathcal{C}_{/Y}})
    \\
    \downarrow && \downarrow
    \\
    * &\stackrel{}{\to}& \mathcal{C}_{/Y}(\langle F \stackrel{}{\to} Y\rangle,[\langle X \stackrel{f}{\to}Y \rangle,\langle X \stackrel{f}{\to}Y \rangle]_{\mathcal{C}_{/Y}})
  }
$$

in [[Set]]. Using the $((-) \times_{\mathcal{C}_{/Y}} \langle X \stackrel{f}{\to}Y\rangle \dashv [\langle X \stackrel{f}{\to}Y\rangle, -]_{\mathcal{C}_{/Y}})$-adjunction  this is equivalently

$$
  \array{
    \mathcal{C}_{/Y}(\langle F \stackrel{}{\to} Y\rangle, \prod_f \langle E \stackrel{p}{\to} X\rangle) 
    &\to& 
  \mathcal{C}_{/Y}(\langle F \stackrel{}{\to} Y\rangle \times_{\mathcal{C}_{/Y}} \langle X \stackrel{f}{\to}Y \rangle, \langle E \stackrel{p}{\to}X \stackrel{f}{\to} Y\rangle)
    \\
    \downarrow && \downarrow
    \\
    * &\stackrel{}{\to}& 
    \mathcal{C}_{/Y}(\langle F \stackrel{}{\to} Y\rangle \times_{\mathcal{C}_{/Y} }\langle X \stackrel{f}{\to}Y \rangle ,
   \langle X \stackrel{f}{\to}Y \rangle)
  }
  \,.
$$

This pullback now manifestly computes 
$\mathcal{C}_{/X}(f^* \langle F \to Y\rangle, \langle E \stackrel{p}{\to} X\rangle)$.

=-- 

+-- {: .num_prop #slicelcc}
###### Proposition 
If $C$ is locally cartesian closed (i.e., if every slice $C/X$ is cartesian closed), then every slice $C/X$ is also locally cartesian closed. 
=-- 

+-- {: .proof} 
###### Proof 
The slice of a slice is a slice, i.e., for every $f \colon X \to Y$ there is an equivalence 

$$(C/Y)/(f \colon X \to Y) \simeq C/X$$ 

whence the statement immediately follows. 
=-- 

+-- {: .num_prop #pres} 
###### Proposition 
If $C$ is locally cartesian closed (and has a terminal object), then the pullback functor $X \times - \colon C \to C/X$ preserves both finite products and exponentials up to isomorphism. 
=-- 

+-- {: .proof} 
###### Proof 
Clearly $X \times - \colon C \to C/x$, being right adjoint to the forgetful functor $\sum_X \colon C/X \to C$, preserves limits, hence it preserves finite products in particular. 

Let $\phi \colon A \to X$ be any morphism. From the pullback diagram 

$$\array{
A \times Z & \stackrel{\phi \times 1}{\to} & X \times Z \\
 _\mathllap{\pi_A} \downarrow & & \downarrow _\mathrlap{\pi_X} \\
A & \underset{\phi}{\to} & X
}$$ 

we conclude $A \times_X (X \times Z) \cong A \times Z$, seen as an object over $X$ via $\phi \circ \pi_A \colon A \times Z \to X$. Thus arrows in the slice $C/X$ of the form 

$$A \times_X (X \times Z) \to X \times Y$$ 

are in natural bijection with arrows in $C$ of the form 

$$A \times Z \stackrel{\langle \phi \circ \pi_A, g\rangle}{\to} X \times Y$$ 

which in turn are in natural bijection with arrows in the slice $C/X$ of the form 

$$A \stackrel{\langle \phi, \tilde{g} \rangle}{\to} X \times Y^Z$$ 

(where $\tilde{g} \colon A \to Y^Z$ is obtained by [[currying]] $g \colon A \times Z \to Y$ in $C$). This proves that $X \times - \colon C \to C/x$ preserves exponentials. 
=-- 

+-- {: .num_cor} 
###### Corollary 
For any $f \colon X \to Y$ in $C$, the base change $f^\ast \colon C/Y \to C/X$ preserves exponentials. In other words, the dependent sum functor $\sum_f$ and the dependent product functor $\prod_f$ satisfy [[Frobenius reciprocity]]. 
=-- 

+-- {: .proof} 
###### Proof 
This is by combining proposition \ref{slicelcc} and proposition \ref{pres}, and recalling that the pullback functor 

$$C/Y \to (C/Y)/(f \colon X \to Y) \simeq C/X$$ 

is identified with the pullback functor $f^\ast \colon C/Y \to C/X$. 
=-- 

This state of affairs may be summarized in terms of the notion of _[[hyperdoctrine]]_:


+-- {: .num_prop}
###### Proposition

If $C$ is a category with [[finite limits]], then it is locally cartesian closed precisely if regarded as an $C$-[[indexed category]] (by forming [[slice categories]]) it is a [[hyperdoctrine]].

=--

For a proof of the statement in this form, see for instance ([Freyd](#Freyd)).

#### In type theory
 {#RelationCartesianClosureBaseChangeInTypeTheory}

We formulate some of the above considerations in the [[syntax]] of
[[dependent type theory]].

+-- {: .num_prop }
###### Proposition

Let 

$$
  \array{
     X &&&& A
     \\
     & {}_{\mathllap{\phi}}\searrow && \swarrow_{\mathrlap{c}}
     \\
     && 
     B
  }
$$

be two [[display maps]]. Then the 
[[category theory|category theoretic]] identification

$$
  [X,A]_{B} = \prod_\phi \phi^* \langle A \stackrel{c}{\to} B\rangle
$$

from prop. \ref{DependentProductImpliesLocalCartesinClosure} is the [[categorical semantics]] of the [[dependent type theory]] [[syntax]]

$$
  b : B \vdash X(b) \to A(b) : Type
  \;\;\;
  =_{def}
  \;\;\;
  b : B \vdash \prod_{x : X(b)} A(\phi(x))
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

While equivalent under the [[relation between type theory and category theory]], the latter expression almost verbatim expresses the evident idea that:

 (collection of internal homs parameterized over $B$) 
  = 
 ( collection of sections of the pullback of $A$ to $X$ )

=--

+-- {: .proof}
###### Proof

By definition, the [[display map]] on the right is expressed as the [[dependent type]]

$$
  b : B \vdash A(b) : Type
  \,,
$$

the pullback $\phi^* \langle A \to B\rangle$ is expressed by [[substitution]]

$$
   x : X \vdash A(\phi(x)) : Type
$$

and next the [[dependent product]] $\prod_\phi \phi^* \langle A \to B\rangle$ by

$$
   b : B  \vdash \prod_{x : X(b)} A(\phi(x)) : Type
  \,.
$$

Now on the right $\phi(x) =_{def} b$, formally because $\phi$ is equivalently the projection $pr_1$ out of $X$ expressed as the [[direct sum]]

$$
  \frac{(b,x) :  \sum_{b : B} X(b)}
   { pr_1(b,x) =_{def} b =_{def} \phi(x)  : B}
  \,.
$$

Inserting this in the above expression makes it [[definitional equality|definitionally equal]] to

$$
   b : B  \vdash \prod_{x : X(b)} A(b) : Type
  \,.
$$

This is now a [[dependent product]] over a type that does not actually depend
on the context $B$, and hence by definition this is the [[dependent type|dependent]] [[function type]]

$$
  b : B \vdash X(b) \to A(b) : Type  
  \,.
$$

which expresses the internal hom in the slice over $B$.

=--



### Internal logic

The [[internal logic]] of locally cartesian closed categories is an [[extensional type theory|extensional]] form of [[dependent type theory]].  In particular, the [[dependent product]] $\Pi_f$ represents an extensional [[dependent product type]] in the internal logic.

### Almost local cartesian closure

There are categories which are cartesian closed and not locally cartesian closed, but in which for some $f$ the  base change functor $f^*: C/y \to C/x$ has a right adjoint. This includes $Cat$, $Gpd$, and the category of [[crossed complex]]es; in the latter two cases, it is necessary and sufficient for $f$ to be a [[fibration]], while in $Cat$ it is sufficient for $f$ to be a fibration or an opfibration.

## Examples

+-- {: .num_prop}
###### Proposition

Every [[sheaf topos]] is locally cartesian closed.

=--

+-- {: .proof}
###### Proof

By [[Giraud's theorem]], in a sheaf topos [[pullbacks]] preserve [[colimits]].
With the [[adjoint functor theorem]] this implies that for every morphism $f : X \to Y$, the pullback functor $f^* : \mathcal{C}_{/Y} \to \mathcal{C}_{/X}$ has a [[right adjoint]] $\prod_f$. By prop. \ref{DependentProductImpliesLocalCartesinClosure} this yields the local cartesian closure.
 
=--

More generally, every [[quasitopos]] is locally cartesian closed.

## Related concepts

* [[cartesian closed category]]

* [[cartesian closed functor]], [[locally cartesian closed functor]]

* [[locally cartesian closed enriched category]]

* [[cartesian closed model category]], [[locally cartesian closed model category]]

* [[cartesian closed (∞,1)-category]], [[locally cartesian closed (∞,1)-category]]


## References

A standard textbook account is around corollary A1.5.3 in 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_

The relation between local cartesian closure and base change/[[hyperdoctrine]] structure is sometimes attributed to

* [[Peter Freyd]], _Aspects of topoi_, Bull. Australian Math. Soc. 7 (1972), 1-76.
 {#Freyd}

A discussion of [[dependent type theory]] as the [[internal language]] of locally cartesian closed categories is in 

* [[R. A. G. Seely]], _Locally cartesian closed categories and type theory_, Math. Proc. Camb. Phil. Soc. (1984) 95 ([pdf](http://www.math.mcgill.ca/rags/LCCC/LCCC.pdf))

Related literature includes

* [[Marta Bunge]],  and [[Susan Niefield]],   _Exponentiability and single universes_ J. Pure Appl. Algebra 148 (2000) 217--250.

* [[François Conduché]],   _Au sujet de l'existence d'adjoints &#224; droite aux foncteurs "image r&#233;ciproque" dans la cat&#233;gorie des cat&#233;gories_ (French)  C. R. Acad. Sci. Paris S&#233;r. A-B  275  (1972), A891--A894.

* J. Howie, _Pullback functors and crossed complexes_ , Cahiers Topologie G&#233;om. Diff&#233;rentielle, 20 (1979) 281--296.



[[!redirects locally cartesian closed categories]]
[[!redirects LCCC]]
[[!redirects lccc]]

[[!redirects locally Cartesian closed category]]
[[!redirects locally Cartesian closed categories]]

[[!redirects local cartesian closure]]
