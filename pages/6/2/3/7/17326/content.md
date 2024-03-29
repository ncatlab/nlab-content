

+-- {: .num_prop #MonoidalStructureOnHomotopyCategoryOfMonoidalModelCategory}
###### Proposition

Let $(\mathcal{C}, \otimes, I)$ be a [[monoidal model category]]. Then the [[left derived functor]] of the tensor product exists and makes the [[homotopy category of a model category|homotopy category]] into a [[monoidal category]] $(Ho(\mathcal{C}), \otimes^L, \gamma(I))$.

If in in addition $(\mathcal{C}, \otimes)$ satisfies the [[monoid axiom in a monoidal model category|monoid axiom]], then the [[localization]] functor $\gamma\colon \mathcal{C}\to Ho(\mathcal{C})$ carries the structure of a [[lax monoidal functor]]

$$
  \gamma
  \;\colon\;
  (\mathcal{C}, \otimes, I)
   \longrightarrow
  (Ho(\mathcal{C}), \otimes^L , \gamma(I))
  \,.
$$

=--

+-- {: .proof}
###### Proof

Consider the explicit model of $Ho(\mathcal{C})$ as the category of fibrant-cofibrant objects in $\mathcal{C}$ with left/right-homotopy classes of morphisms between them (discussed at _[[homotopy category of a model category]]_).

A [[derived functor]] exists if its restriction to this subcategory preserves weak equivalences. Now the [[pushout-product axiom]] implies that on the subcategory of cofibrant objects the functor $\otimes$ preserves acyclic cofibrations, and then the preservation of all weak equivalences follows by [[Ken Brown's lemma]]. 

Hence $\otimes^L$ exists and its [[associativity]] follows simply by restriction. It remains to see its [[unitality]].

To that end, consider the construction of the localization functor $\gamma$ via a fixed but arbitrary choice of (co-)fibrant replacements $Q$ and $R$, assumed to be the identity on (co-)fibrant objects. We fix notation as follows:

$$
\emptyset \underoverset{\in Cof}{i_X}{\longrightarrow} Q X \underoverset{\in W \cap Fib}{p_x}{\longrightarrow} X
\;\;\,,\;\;
X \underoverset{\in W \cap Cof}{j_X}{\longrightarrow} R X \underoverset{\in Fib}{q_x}{\longrightarrow} \ast
  \,.
$$

 
Now to see that $\gamma(I)$ is the [[tensor unit]] for $\otimes^L$, notice that in the [[zig-zag]]

$$
  (R Q I) \otimes (R Q X)
    \overset{j_{Q I} \otimes (R Q X)}{\longleftarrow}
  (Q I) \otimes (R Q X)
    \overset{(Q I)\otimes j_{Q X}}{\longleftarrow}
  (Q I) \otimes (Q X)
    \overset{p_I \otimes (Q X)}{\longrightarrow}
  I \otimes Q X
    \simeq
  Q X
$$

all morphisms are weak equivalences: For the first two this is due to the [[pushout-product axiom]], for the third this is due to the unit axiom on a monoidal model category. It follows that under $\gamma(-)$ this zig-zig gives an isomorphism

$$
  \gamma(I) \otimes^L \gamma(X)\simeq \gamma(X)
$$

and similarly for tensoring with $\gamma(I)$ from the right.

To exhibit lax monoidal structure on $\gamma$, we need to construct a [[natural transformation]]

$$
  \gamma(X) \otimes^L \gamma(Y) \longrightarrow \gamma(X \otimes Y)
$$

and show that it satisfies the the appropriate [[associativity]] and [[unitality]] condition.

By the definitions at _[[homotopy category of a model category]]_, the morphism in question is to be of the form

$$
  (R Q X) \otimes (R Q Y) \longrightarrow R Q (X\otimes Y)
$$


To this end, consider the [[zig-zag]]

$$
  (R Q X) \otimes (R Q Y)
   \underoverset{\in Cof \cap W}{j_{Q X} \otimes R Q Y}{\longleftarrow}
  (Q X) \otimes (R Q Y)
    \underoverset{\in Cof \cap W}{(Q X) \otimes  j_{Q Y} }{\longleftarrow}
  (Q X) \otimes (Q Y)
    \overset{p_X \otimes (Q Y)}{\longrightarrow}
  X \otimes (Q Y)
    \overset{Y \otimes p_Y}{\longrightarrow}   
  X \otimes Y
  \,,
$$

and observe that the two morphisms on the left are weak equivalences, as indicated, by the [[pushout-product axiom]] satisfied by $\otimes$.

Hence applying $\gamma$ to this zig-zag, which is given by the two horizontal part of the following digram

$$
  \array{
    (R Q X) \otimes (R Q Y) &\longleftarrow& R( Q X \otimes Q Y ) &\longrightarrow& R Q (X \otimes Y)
    \\
    \uparrow^{\mathrlap{id}} && \uparrow^{\mathrlap{j_{Q X \otimes Q Y}}} && \uparrow^{\mathrlap{j_{Q(X \otimes Y)}}}
    \\
    \downarrow^{\mathrlap{id}} && \downarrow^{\mathrlap{id}} && \downarrow^{\mathrlap{p_{X\otimes Y}}}
    \\
    (R Q X) \otimes (R Q Y)
     &\underoverset{\in Cof \cap W}{j_{Q X} \otimes j_{Q Y}}{\longleftarrow}&
    (Q X) \otimes (Q Y)
      &\overset{p_X \otimes p_Y}{\longrightarrow}&
    X \otimes Y
  }
  \,,
$$

and inverting the first two morphisms, this yields a natural transformation as required. 


To see that this satisfies associativity if the monoid axiom holds, tensor the entire diagram above on the right with $(R Q Z)$ and consider the following [[pasting]] composite:

$$
  \array{
    (R Q X) \otimes (R Q Y) \otimes (R Q Z) &\longleftarrow& R( Q X \otimes Q Y ) \otimes (R Q Z) &\longrightarrow& (R Q (X \otimes Y)) \otimes (R Q Z)
    \\
    \uparrow^{\mathrlap{id}} && \uparrow^{\mathrlap{j_{Q X \otimes Q Y} \otimes id }} && \uparrow^{\mathrlap{j_{Q(X \otimes Y)}\otimes id }}
    \\
    && && Q(X \otimes Y) \otimes (R Q Z) &\overset{id \otimes j_{Q Z}}{\longleftarrow}& Q(X\otimes Y) \otimes (Q Z)
    \\
       \downarrow^{\mathrlap{id}} && \downarrow^{\mathrlap{id}} 
    && 
      \downarrow^{\mathrlap{p_{(X\otimes Y)} \otimes id }} 
    &(\star)& 
     \downarrow^{\mathrlap{p_{(X \otimes Y)} \otimes id}}
    \\
    (R Q X) \otimes (R Q Y) \otimes (R Q Z)
     &\underoverset{\in Cof \cap W}{j_{Q X} \otimes j_{Q Y} \otimes id}{\longleftarrow}&
    (Q X) \otimes (Q Y) \otimes (R Q Z)
      &\overset{p_X \otimes p_Y \otimes id}{\longrightarrow}&
    X \otimes Y \otimes (R Q Z)
      &\underset{id \otimes j_{Q Z}}{\longleftarrow}&
    X\otimes Y \otimes Q Z 
      &\overset{id \otimes p_Z}{\longrightarrow}& 
    X \otimes Y \otimes Z  
  }
  \,,
$$

Observe that under $\gamma$ the total top [[zig-zag]] in this diagram gives

$$
  (\gamma(X) \otimes^L \gamma(Y)) \otimes^L \gamma(Z)
  \to \gamma(X\otimes Y)\otimes^L \gamma(Z)
  \,.
$$

Now by the [[monoid axiom in a monoidal model category|monoid axiom]] (but not by the pushout-product axiom!), the horizontal maps in the square in the bottom right (labeled $\star$) are weak equivalences. This implies that the total horizontal part of the diagram is a [[zig-zag]] in the first place, and that under $\gamma$ the total top zig-zag is equal to the image of that total bottom zig-zag. But by functoriality of $\otimes$, that image of the bottom zig-zag is 

$$
  \gamma(p_X \otimes p_Y \otimes p_Z) 
  \circ 
  \gamma(j_{Q X} \otimes j_{Q Y} \otimes j_{Q Z})^{-1}
  \,.
$$

The same argument applies to left tensoring with $R Q Z$ instead of right tensoring, and so in both cases we reduce to the same morphism in the homotopy category, thus showing the associativity condition on the transformation that exhibits $\gamma$ as a lax monoidal functor.

=--
