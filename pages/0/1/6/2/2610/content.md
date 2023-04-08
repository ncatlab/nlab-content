

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[homological algebra|homological]] [[algebra]], what came to be known &lbrack;[Bass (1963)](#Bass63)&rbrack; as the *Eilenberg swindle* (in honor of [[Samuel Eilenberg]]) is an argument (originally due to [Mazur (1961)](#Mazur61)) proving that the [[Grothendieck group]] (the 0th [[algebraic K-theory]] group $K_0$) of many [[abelian categories]] is [[trivial group|trivial]]. 

The idea of the "swindle" is essentially the following [Hilbert hotel](https://en.m.wikipedia.org/wiki/Hilbert%27s_paradox_of_the_Grand_Hotel)-type argument:

In an [[abelian category]] $A$ with [[countable set|countable]] [[direct sums]], we have for any [[object]]  $X \in A$ an [[isomorphism]] 

$$
  X 
    \oplus   \bigoplus_{i=1}^{\infty} 
  X 
  \,\simeq\,  \bigoplus_{i=1}^{\infty} 
  X 
  \,,
$$

which implies $[X]=0$ in $K_0(A)$.

This is the reason that, for instance, one has to restrict oneself to categories of *[[finitely generated module|finitely generated]]* ([[projective modules|projective]]) [[modules]] (which lack infinite direct sums) in defining (nontrivial) [[algebraic K-theory]] groups $K_0$ of a [[ring]].


## References

The earliest known appearance of Eilenberg's swindle in writing is in Lemma 3 of

* {#Mazur61} [[Barry C. Mazur]], _On embeddings of spheres_,  Acta Mathematica **105** 1–2 (1961) 1–17   &lbrack;[doi:10.1007/BF02559532](https://doi.org/10.1007%2FBF02559532)&rbrack;

The earliest attribution to [[Samuel Eilenberg]] as well as the use of the term “swindle” is in §1 of

* {#Bass63} [[Hyman Bass]], _Big projective modules are free_, Illinois Journal of Mathematics **7** (1963) 24–31  &lbrack;[doi:10.1215/ijm/1255637479](https://doi.org/10.1215%2Fijm%2F1255637479)&rbrack;
