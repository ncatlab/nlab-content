
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


# The Tychonoff Theorem
* table of contents
{: toc}

## Statement 

The **Tychonoff theorem** is a basic [[theorem]] in the field of [[topology]], 
It states that the  [[product topological space]], with its [[Tychonoff topology]], of an arbitrary [[set]] of [[compact topological spaces]] is itself [[compact space|compact]].

The Tychonoff theorem implies for instance the [[Heine-Borel theorem]].

Spellings of the author of the theorem vary, other common uses are _Tihonov_ and _Tikhonov_. The theorem is named after &#1040;&#1085;&#1076;&#1088;&#1077;&#1081; &#1053;&#1080;&#1082;&#1086;&#1083;&#1072;&#1077;&#1074;&#1080;&#1095; &#1058;&#1080;&#1093;&#1086;&#1085;&#1086;&#1074;, whose name becomes Tihonov in the transliteration used in slavistics or 'Andrey Nikolayevich Tikhonov' in modern English (BGN/PCGN) transliteration, 
but he originally published in German as 'A.N. Tychonoff'. 

In its [[classical mathematics|classical]] form, the Tychonoff theorem is equivalent to the [[axiom of choice]]. (Compare the statement of the axiom of choice: a product of sets is [[inhabited set|inhabited]] if each set is inhabited.) 

Notice that no [choice](axiom+of+choice#Variants) whatsoever is needed to prove the analogous theorem for [[locales]]: even in [[constructive mathematics]], a [[Cartesian product]] of locales is compact if each of the locales is compact.  From that perspective, the statement equivalent to the axiom of choice is this: a product of locales is [[spatial locale|spatial]] if each of the locales is spatial.  Either of these may be considered a Tychonoff theorem for locales.

To prove the Tychonoff theorem for [[Hausdorff topological spaces]] only, the full [[axiom of choice]] is not needed; the [[ultrafilter theorem]] (and possibly [[excluded middle]]) are enough.


## Proof via ultrafilter convergence 

One method of proof uses [[ultrafilter]] [[convergence]]. Let $\langle X_\alpha \rangle_{\alpha \in A}$ be a family of compact spaces. 

1. Every ultrafilter $U_\alpha$ on the underlying set of $X_\alpha$ converges to some point $x_\alpha$. (Consider the collection of all closed sets belonging to $U_\alpha$. Finite subcollections have nonempty intersection, so by compactness the intersection of the collection is also nonempty. Let $x_\alpha$ be a point belonging to that intersection. Every closed set disjoint from $x_\alpha$ belongs to the complement of $U_\alpha$, hence every open set containing $x_\alpha$ belongs to $U_\alpha$, i.e., $U_\alpha$ converges to $x_\alpha$.)

1. Let $U$ be an ultrafilter on $\prod_\alpha X_\alpha$. Since the set-of-ultrafilters construction $S \mapsto \beta S$ is [[functor]]ial, we have a push-forward ultrafilter $U_\alpha = \beta(\pi_\alpha)(U)$ on each $X_\alpha$, where $\pi_\alpha$ is a projection map. Choose a point $x_\alpha$ to which $U_\alpha$ converges. Then it is easily checked that $U$ converges to the point $\langle x_\alpha \rangle$ in the product space.

1. Since every ultrafilter $U$ on $\prod_\alpha X_\alpha$ converges to a point, the product is compact. (If it were not, then we could find a collection of nonempty closed sets whose intersection is empty, but closed under finite intersections. This collection generates a filter which is contained in some ultrafilter $U$, by the [[ultrafilter theorem]]. Since every ultrafilter $U$ converges to some $x$, it cannot contain any closed set in the complement of $x$, hence cannot contain some closed set in the original collection, contradiction.) 

+-- {: .num_remark #TyCH} 
###### Remark 
The axiom of choice is used in step 2 to combine the $x_\alpha$ into a single family $\langle x_\alpha \rangle$; if the $X_\alpha$ were Hausdorff, then the $x_\alpha$ would be unique, and we would not need the axiom of choice at this step.  The ultrafilter theorem is used in step 3, and this is the only other place where a choice principle is needed. In other words, working over a choice-free set theory like [[ZFC|ZF]] or even BZ (bounded Zermelo set theory), the ultrafilter principle (UF) implies the Tychonoff theorem for Hausdorff spaces. 
=-- 

+--{.query}

[[Todd Trimble|Todd]]: Regarding the need for [[excluded middle]]: it's not so clear that there's any direct argument. For it's at this point where we have to use the ultrafilter theorem, in order to produce a witnessing ultrafilter. Witness to what? The statement as it stands involves universal quantification over ultrafilters, so the witness would be in view of a contradiction.

 [[Toby Bartels|Toby]]: Note that we use excluded middle in two places for a proof by contradiction; I\'ll try to remove these if possible. ([[Todd Trimble|Todd]]: I've rearranged the argument in the first step; the first formulation I gave looked unnecessarily "choice-y".) 
 
[[Todd Trimble|Todd]]: Yes, although I'm not too fussed about using indirect arguments, since in a topos, excluded middle follows from AC. I don't know whether it also follows from a weaker choice principle equivalent to the ultrafilter theorem, but I guess I wouldn't be surprised if it did. 

_Toby_:  As far as I know, UF and EM are independent (although I\'m not certain).  So I\'m interested in whether the Hausdorff case requires EM as well as UF.

_Todd_: I wrote John Bell about this, and he kindly responded. Apparently you are right: UF (or BPIT) implies only a weakened version of EM: $\neg x \vee \neg\neg x = 1$. He referred me to his paper <a href="http://publish.uwo.ca/~jbell/BOOLCON.pdf">Boolean Algebras and Distributive Lattices Treated Constructively</a>, for this (among much else). 

_Toby_:  Great, hard results!  Although I\'m not sure that his ultrafilter theorem is the same as mine, since he talks about ultrafilters in arbitrary distributive lattices, while I would use [[ultrafilter|a constructively stronger definition]] of ultrafilter in a powerset.  But I should be able to figure out what carries over, now that I have a result to go for.
=--


## Proof of converses

Now we will prove that the Tychonoff theorem implies the axiom of choice, while the Tychonoff theorem for Hausdorff spaces implies the ultrafilter theorem.  This is done by judicious choice of examples.

**Tychonoff theorem implies axiom of choice**: let $\{X_\alpha\}_{\alpha \in A}$ be a family of nonempty sets. Let $Y_\alpha$ be obtained by adjoining a point $p$ to $X_\alpha$. Topologize $Y_\alpha$ by taking the nontrivial open sets to be $X_\alpha$ and $\{p\}$. Then $Y_\alpha$ is compact; assuming Tychonoff, $Y = \prod_\alpha Y_\alpha$ is compact. For each $\alpha$, put 

$$K_\alpha = \{y \in Y: y_\alpha \in X_\alpha\}$$ 

Then $K_\alpha$ is closed, and any finite intersection of the $K_\alpha$ is nonempty (use $p$ in all but finitely many components). Hence 

$$\prod_\alpha X_\alpha = \bigcap_\alpha K_\alpha$$ 

is nonempty as well, by compactness. Thus the axiom of choice follows. 

**Tychonoff theorem for Hausdorff spaces implies ultrafilter theorem**: let $F$ be a filter on a set $X$, i.e., a filter in the Boolean algebra $P X$. An ultrafilter $U$ containing $F$ is tantamount to a Boolean algebra map $2^X \to 2$ which sends all of $F$ to $1$, or equivalently to a Boolean algebra map $\phi: B = 2^X/F \to 2$. Thus it suffices to prove the following result: 

+-- {: .num_prop #nonempty} 
###### Proposition 
For every (non-terminal) Boolean algebra $B$, there exists a homomorphism $B \to 2$. 
=-- 

+-- {: .proof} 
###### Proof 
Let $|B|$ denote the underlying set of $B$. The set of all functions $f: |B| \to 2$ is a $|B|$-indexed product of copies of $2$; considering $2$ as a compact Hausdorff space, this set is compact Hausdorff, assuming the Tychonoff theorem for Hausdorff spaces. For each finite subset $S \subseteq |B|$, let $K_S$ be the [[subspace]] of functions $f: |B| \to 2$ for which the equations 

$$f(x \wedge y) = f(x) \wedge f(y) \qquad f(\neg x) = \neg f(x)$$ 

hold for all $x, y \in S$. As the space $2^{|B|}$ is Hausdorff, $K_S$ being defined by an equalizer is a closed subspace, and it is easy (and classical) that it is nonempty: the subalgebra $B(S) \subseteq B$ generated by $S$ is finite and in particular [[atom|atomic]] and thus admits a homomorphism $f: B(S) \to 2$ defined by $f(x) = 1$ iff $a \leq x$ for some given atom $a$, and then we can take $f(b) = 1$ for any $b$ outside $B(S)$. By compactness of $2^{|B|}$, the intersection of all the $K_S$ is nonempty, and this is precisely the set of Boolean algebra maps $\phi: B \to 2$. 
=-- 

* This proof may be seen as a classical illustration of the [[compactness theorem]] for propositional logic. We may think of a Boolean algebra $B$ as a Lindenbaum algebra for a [[propositional logic|propositional]] [[theory]], and a Boolean algebra map $\phi: B \to 2$ as a [[model]] for that theory. A model exists iff a model exists for every theory generated by a finite subset of propositions, by the compactness theorem. In fact, the proof above suggests the topological provenance of the term "compactness theorem". 

## Tychonoff theorem for locales 

Given the close connection between the Tychonoff theorems and choice principles, it may come as a surprise that the Tychonoff theorem for [[locales]] -- the product of a small collection of compact locales is compact, equivalently that the coproduct of a small collection of compact [[frames]] is compact -- may be proved without the [[axiom of choice]] and even [[constructive mathematics|constructively]]. 

More details to appear at [[Tychonoff theorem for locales]]. 

## References

* Wikipedia, _[Tychonoff's theorem](https://en.wikipedia.org/wiki/Tychonoff%27s_theorem)_


[[!redirects Tihonov's theorem]]
[[!redirects Tihonov theorem]]
[[!redirects Tihonov's topology]]