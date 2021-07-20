
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The _classical [[model category]] structure on [[pointed topological spaces]]_ $Top^{\ast/}_{Quillen}$ is the [[model structure on pointed objects]] of the [[classical model structure on topological spaces]] $Top_{Quillen}$ under the point (a [[pointed model category]]).

Equipped with the [[smash product]] this is a [[monoidal model category]].

## Properties

### Cofibrant generation

Recall that the generatic cofibrations of the [[classical model structure on topological spaces]] are 

$$
 I_{Top} 
  \coloneqq
 \left\{
    S^{n-1} \overset{\iota_n}{\longrightarrow} D^n
 \right\}_{n \in \mathbb{N}}
$$

and the generating acylic cofibrations are

$$
 J_{Top} 
  \coloneqq
 \left\{
    D^n \overset{(id,\delta_0)}{\longrightarrow} D^n \times I
 \right\}_{n \in \mathbb{N}}
  \,.
$$

Write

$$
  (-)_+
  \;\colon\;
  Top \longrightarrow Top^{\ast/}
$$

for the operation of freely adjoining a basepoint.

+-- {: .num_prop}
###### Proposition

The [[coslice model structure]] $(Top_{Quillen})^{\ast/}$ is itself [[cofibrantly generated model category|cofibrantly generated]], with generating cofibrations

$$
  I_{Top^{\ast/}}
  = 
 \left\{
    S^{n-1}_+ \overset{(\iota_n)_+}{\longrightarrow} D^n_+
 \right\}
$$

and generating acyclic cofibrations

$$
  J_{Top^{\ast/}}
  = 
 \left\{
    D^n_+ \overset{(id, \delta_0)_+}{\longrightarrow} (D^n \times I)_+
 \right\}
  \,.
$$

=--

This is a special case of a general statement about cofibrant generation of [[coslice model structures]], see [this proposition](model+structure+on+an+over+category#ModelStructureInheritsGoodProperties).


## Related concepts

* [[model structure on topological spaces]]

  * [[classical model structure on topological spaces]]

    * [[classical model structure on pointed topological spaces]]

  * [[Strøm model structure]]

  * [[model structure on Delta-generated topological spaces]]



## References

Textbook accounts:

* {#Hovey99} [[Mark Hovey]], Cor. 2.4.20 in: _[[Model Categories]]_, Mathematical Surveys and Monographs, Volume 63, AMS (1999) ([ISBN:978-0-8218-4361-1](https://bookstore.ams.org/surv-63-s), [doi:10.1090/surv/063](https://doi.org/http://dx.doi.org/10.1090/surv/063), [pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/hovey-model-cats.pdf), [Google books](http://books.google.co.uk/books?id=Kfs4uuiTXN0C&printsec=frontcover))

