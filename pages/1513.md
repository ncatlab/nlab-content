+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Separated presheaf

### Idea 

The condition that a [[presheaf]] be a [[sheaf]] may be seen as a condition of unique existence.  A presheaf is separated if it satisfies the uniqueness part.

### Definition 

Let $S$ be a [[site]].

Recall that a [[sheaf]] on $S$ is a presheaf $A \in PSh_S$ such that for all [[local isomorphism]]s $Y \to X$ the induced morphism  $PSh_S(X,A) \to PSh_S(Y,A)$ (under the [[hom-functor]] $PSh_S(-,A)$) is an [[isomorphism]].  (For an arbitrary class of morphisms $V$, the corresponding condition is called being a [[local object]].)  
It is sufficient to check this on the [[dense monomorphism]]s instead of all local isomorphisms.  This is equivalent to checking [[cover]]ing [[sieve]]s.


+-- {: .num_defn}
###### Definition

A [[presheaf]] $A \in PSh(S)$ is called **separated** (or a **monopresheaf**) if for all [[local isomorphism]]s $Y \to X$ the induced morphism $Hom(X,A) \to Hom(Y,A)$ is a [[monomorphism]].

More generally, for a class $V$ of arrows in a category $C$, an object $A\in C$ is $V$-**separated** if for all morphisms $Y\to X$ in $V$, the induced morphism $Hom(X,A)\to Hom(Y,A)$ is a monomorphism.

=--


+-- {: .num_remark}
###### Remark

As for sheaves, it is sufficient to check the separation condition on the [[dense monomorphism]]s, hence on the [[sieve]]s.

For $\{p_i : U_i \to U\}$ a [[covering]] family of an object $U \in S$, the condition is that if $a,b \in A(U)$ are such that for all $i$ we have $A(p_i)(a) = A(p_i)(b)$ then already $a = b$.

=--

+-- {: .num_remark}
###### Remark

The definition generalizes to any system of [[local isomorphisms]] on any [[topos]], such as that obtained from any [[Lawvere-Tierney topology]], or equivalently any [[subtopos]].

=--

### Example

+-- {: .num_example #ConstantPresheafOnSiteWithAllInhabitedCoverings}
###### Example

Let $(S,J)$ be a [[site]] for which every $J$-[[covering family]] is [[inhabited]]. Then for any [[set]] $X$, the [[constant presheaf]] $S\ni a \mapsto X$ is separated.

=--

See also at _[[locally connected site]]_.


### Properties


+-- {: .num_prop}
###### Proposition

The full [[subcategory]]

$$
  i : Sep(S) \hookrightarrow PSh(S)
$$

of separated presheaves in a presheaf category is 

* a [[reflective subcategory]];

* a [[quasitopos]]. 

=--

Being a reflective subcategory means that there is a [[left adjoint]] functor to the inclusion

$$
  (L_{sep} \dashv i) : Sep(S) \stackrel{\overset{L_{sep}}{\leftarrow}}{\hookrightarrow} 
  PSh_S
  \,.
$$

+-- {: .num_defn}
###### Definition

For $A \in PSh_S$ the **separafication** $L_{sep}A$ of $A$ is the presheaf that assigns equivalence classes
$$L_{sep}A : U \mapsto A(U)/\sim_U,$$
where $\sim_U$ is the [[equivalence relation]] that relates two elements $a \sim b$ iff there exists a [[covering]] $\{p_i : U_i \to U\}$ such that $A(p_i)(a) = A(p_i)(b)$ for all $i$.

This construction extends in the evident way to a functor
$$L_{sep} : PSh(S) \to Sep(S).$$

=--

+-- {: .num_prop}
###### Proposition

This functor $L_{sep}$ is indeed a [[left adjoint]] to the inclusion $i : Sep(S) \hookrightarrow PSh(S)$.

=--

+-- {: .proof}
###### Proof

Let $A \in PSh(S)$ and $B \in Sep(S) \hookrightarrow PSh(S)$. We need to show that morphisms $f : A \to B$ in $PSh_C$ are in natural bijection with morphisms $L_{sep} A \to B$ in $Sep(S)$.

For $f$ such a morphism and $f_U : A(U) \to B(U)$ its component over any object $U \in S$, consider any covering $\{U_i \to U\}$, let $S(U_i) \to U$  be the corresponding [[sieve]] and consider the [[commuting diagram]]
$$
  \array{
    \{(a_i \in A(U_i)) | \cdots \}
    &\to& 
   \{(b_i \in F(U_i)) | \cdots \}
    \\ 
    \uparrow && \uparrow
    \\
    A(U) &\stackrel{f_U}{\to}& B(U)
  }
$$
obtained from the naturality of $PSh_S(S(U_i) \to U, A \stackrel{f}{\to} B)$.

If for $a,a' \in A(U)$ two elements that are not equal their restrictions to the cover become equal in that  $\forall i :  a|_{U_i} = a'|_{U_i}$, then also $f(a|_{U_i}) = f(a'|_{U_i})$ and since the right vertical morphism is monic there is a _unique_ $b \in B(U)$ mapping to the latter. The commutativity of the diagram then demands that $f(a) = f(a') = b$.

Since this argument applies to all covers of $U$, we have that $f_U$ factors uniquely through the projection map $A(U) \to A(U)/\sim_U =: L_{sep}(U)$ onto the quotient. Since this is true for every object $U$ we have that $f$ factors uniquely through $A \to L_{sep}A$.

=--


## Biseparated presheaf

### Idea

Often one is interested in separated presheaves with respect to one [[coverage]] that are sheaves with respect to another coverage. These are called _biseparated presheaves_ . 

This typically arises if a [[reflective subcategory]]
$$C \stackrel{\stackrel{}{\leftarrow}}{\hookrightarrow} Sh(S)$$
of a [[sheaf topos]] is given. This is the [[localization]] at a set $W$ of morphisms in $Sh(S)$, with $C$ the full subcategory of all [[local object]]s $c$: objects such that $Sh_(S)(w,c)$ is an isomorphism for all $w \in W$. A $W$-separated object is then called a _biseparated presheaf_ on $S$ and their collection $BiSep(S)$ factors the reflective inclusion as
$$
  C 
    \stackrel{\leftarrow}{\hookrightarrow}
  BiSep(S) 
    \stackrel{\leftarrow}{\hookrightarrow}
  Sh(S).
$$

### Definition

+-- {: .num_defn}
###### Definition

A **bisite** is a [[small category]] $S$ equipped with two [[coverage]]s: $J$ and $K$ such that $J \subset K$.

A presheaf $A \in PSh_S$ is called $(J,K)$-**biseparated** if it is

* a [[sheaf]] with respect to $J$;

* a separated presheaf with respect to $K$.

Write 
$$
  BiSep_{(J,K)}(S) \hookrightarrow Sh_J(S) \hookrightarrow PSh(S)
$$ 
for the full [[subcategory]] on biseparated presheaves.

=--


### Examples

[[Diffeological spaces]] are biseparated presheaves
for the bisite structure on [[cartesian spaces]],
where $J$ is the usual topology of open covers
and $K$ is the topology given by the families
$$\coprod_{u\in U}\mathbf{R}^0 \to U$$
for every [[cartesian space]] $U$.

The [[sheaf]] condition with respect to $J$ yields a [[smooth set]],
whereas the [[separated presheaf]] condition with respect to $K$
makes it into a [[diffeological space]].


### Properties

+-- {: .num_prop}
###### Proposition

Biseparated presheaves form a [[reflective subcategory]] of all sheaves
$$
  BiSep_{(J,K)}(S)
  \stackrel{\stackrel{L^K_{sep}}{\leftarrow}}{\hookrightarrow}
  Sh_J(S)
  \,.
$$

=--

See [[quasitopos]] for the proof.

## Related concepts

* **separated presheaf**

* [[separated (2,1)-presheaf]]

* [[separated (∞,1)-presheaf]]

## References

The general theory of biseparated presheaves and Grothendieck quasitoposes is in section C.2.2 of

* [[Peter Johnstone]], [[Sketches of an Elephant]] .

A concrete description of separafication appears on page 43 of

* [[Angelo Vistoli]], _Notes on Grothendieck topologies,
fibered categories and descent theory_ ([pdf](http://homepage.sns.it/vistoli/descent.pdf#Page=43))

category: sheaf theory

[[!redirects monopresheaf]]
[[!redirects separated presheaves]]
[[!redirects separated object]]
[[!redirects separated objects]]
[[!redirects biseparated presheaf]]
[[!redirects biseparated presheaves]]
[[!redirects biseparated object]]
[[!redirects biseparated objects]]