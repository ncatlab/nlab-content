
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents 
{: toc}


##Statement
 {#Statement}

+-- {: .num_theorem Comprehensive Factorization System }
###### Theorem

Let $E$ be the class of [[final functors]] and $M$ be the class of [[discrete fibrations]]. Then $(E,M)$ is an [[orthogonal factorization system]] of [[Cat]], called the **comprehensive factorization system**.

=--

+-- {: .proof}
###### Proof

Let $F:C\to D$ be a functor.  Define $K:D\to Set$ as the left Kan extension of the constant presheaf $C\to Set$ at the singleton along $F$.  Explicitly, $K(d)$ is the set of connected components of $F/d$. Let $E=\int K$, so an object of $E$ is an ordered pair $(d, [\alpha:Fc\to d])$ where $[\alpha]$ denotes the connected component of $(c,\alpha)$.  Then it is not hard to verify that $e:C\to E$ mapping $c\mapsto (Fc,[id_{fc}])$ is final, the canonical $m:E\to D$ is a discrete fibration, and $F=me$.

Now we show that $E$ and $M$ are replete subcategories of $Cat$.  Clearly they include all isomorphisms.

If functors $F:C\to D$ and $G: D\to E$ are final, then we show that $G\circ F$ is final.  For $e\in E$, there is a element $(d,\alpha:e\to Gd)$ of $e/G$, and thence an element $(c,\beta:d\to Fc)$ of $d/F$, so we obtain an element $(c, e \stackrel{\alpha}{\to} Gd \stackrel{G\beta}{\to} GFc)$ of $e/GF$.  Now we must show that any two elements $(c,\gamma:e\to GFc),(c',\gamma':e\to GFc')$ are connected.  Since $G$ is final, elements $(Fc,\gamma)$ and $(Fc',\gamma')$ of $e/G$ are connected.  It suffices to consider the case of a zig-zag of length one: a morphism $f:Fc\to Fc'$ such that 

```
<nowiki>\[
    \begin{xymatrix}
        e \ar[r]^\gamma \ar[dr]_{\gamma'} & GFc \ar[d]^{Gf} \\ & GFc'
    \end{xymatrix}
\]</nowiki>
```

By finality of $F$, the elements $(c,id:Fc\to Fc)$ and $(c', f:Fc\to Fc')$ of $Fc/F$ are connected.  A zig-zag path between them, by precomposition with $\gamma$, becomes a zig-zag path between $(c,\gamma)$ and $(c',\gamma')$.  So $G\circ F$ is final.

The proof that discrete fibrations form a subcategory is omitted.

Now we must show that the lifting problem

```
<nowiki>\[
\begin{xymatrix}
A \ar[r]^f \ar[d]_e & X \ar[d]^m \\
B \ar[r]_g \ar@{-->}[ru]^h & Y \\
\end{xymatrix}
\]</nowiki>
```

has a unique solution $h$ when $e\in E$ and $m\in M$.

We prove uniqueness first.  For $b\in B$, let $(a,\alpha:b\to e(a))\in b/e$.  Then $h(\alpha)$ must be the unique lifting of $g(\alpha)$, and $h(b)$ the domain of this lifting, proving uniqueness of $h$ on objects.  For $\beta:b\to b'$ in $B$, $h(\beta)$ must be the unique lifting of $g(\beta)$, so $h$ is unique (if it exists).

Now we must show that this $h$ is well-defined, functorial, and a solution to the lifting problem.  If $(a',\alpha':b\to e(a'))$ is another element of $b/e$, then WLOG let $u:a\to a'$ such that

```
<nowiki>\[
\begin{xymatrix}
b \ar[r]^\alpha \ar[dr]_{\alpha'} & e(a) \ar[d]^{e(u)} \\
& e(a')
\end{xymatrix}
\]</nowiki>
```

Lifting this diagram, we see that $g(\alpha)$ and $g(\alpha')$ must lift to morphisms with identical domain, so $h$ is well-defined on objects.

For $\beta:b\to b'$ in $B$, let $\alpha:b'\in e(a)$, and by the diagram

```
<nowiki>\[
\begin{xymatrix}
b \ar[r]^\beta \ar[dr]_{\alpha\circ\beta} & b' \ar[d]^\alpha \\
& e(a)
\end{xymatrix}
\]</nowiki>
```

we see that $g(\beta)$ and $g(\alpha\circ\beta)$ must lift to morphisms with identical domains, so $h(\beta)$ has domain $h(b)$.

Functoriality now follows easily from uniqueness of lifting for a discrete fibration, and it is not hard to show that $h$ is a solution to the lifting problem.

=--

## References

* [[Ross Street]], [[R. F. C. Walters]], The Comprehensive Factorization of Functor

* [[Fosco Loregian]], [[Emily Riehl]], Categorical Notions of Fibration

* [[Clemens Berger]], [[Ralph M. Kaufmann]], Comprehensive Factorization Systems

[[!redirects comprehensive factorization systems]]