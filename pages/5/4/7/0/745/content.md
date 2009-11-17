#Idea#

The comma category of two functors $f : C \to E$ and $g : D \to E$ is like an [[arrow category]] of $E$ where all arrows have their [[source]] in the image of $f$ and their [[target]] in the image of $g$ (and the morphisms between arrows keep track of how these sources and targets are in these images).


# Definition #

If $f:C\to E$ and $g:D\to E$ are [[functors]], their **comma category** is the category $(f/g)$ whose

* [[objects]] are triples $(c,d,\alpha)$ where $c\in C$, $d\in D$, and $\alpha:f(c)\to g(d)$ is a morphism in $E$, and whose

* [[morphisms]] from $(c_1,d_1,\alpha_1)$ to $(c_2,d_2,\alpha_2)$ are pairs $(\beta,\gamma)$, where $\beta:c_1\to c_2$ and $\gamma:d_1\to d_2$ are morphisms in $C$ and $D$, respectively, such that $\alpha_2 . f(\beta) = g(\gamma) . \alpha_1$.

$$
  \array{
    f(c_1)
    &\stackrel{f(\beta)}{\to}&
    f(c_2)
    \\
    \downarrow^{\alpha_1}
    &&
    \downarrow^{\alpha_2}
    \\
    f(d_1)
    &\stackrel{g(\gamma)}{\to}&
    f(d_2)    
    \\
    \\
    (c_1,d_1, \alpha_1)
    &\stackrel{(\beta,\gamma)}{\to}&
    (c_2,d_2, \alpha_2)
  }
$$

Another common notation for the comma category is $(f\downarrow g)$.  The original notation, from which the terminology is derived, is $(f,g)$, but this is rarely used any more; see the discussion below.


## Definition in terms of pullbacks ##

Let $I = \{a \to b\}$ be the (directed) [[interval object|interval category]] and $E^I = Funct(I,E)$ the [[functor category]]. 

The comma category is the [[pullback]]

$$
  \array{
    (f/g) 
    &\to&
    E^I
    \\
    \downarrow && \downarrow^{d_0 \times d_1}
    \\
    C \times D
    &\stackrel{f \times g}{\to}&
    E \times E
  }
$$

(in the 1-category of categories).

Compare this with the construction at [[generalized universal bundle]] and with the definition of [[loop space object]]. 

Alternatively, the comma category is the "lax pullback" -- or rather the [[comma object]] (see the discussion at [[2-limit]]) of the pullback diagram, 

$$
  \array{
    && C
    \\
    && \downarrow^f
    \\
    D &\stackrel{g}{\to}& E
  }
$$


i.e. the universal cone that commutes up to a natural transformation

$$
  \array{
    (f/g) &\to& C
    \\
    \downarrow &\Downarrow& \downarrow^f
    \\
    D &\stackrel{g}{\to}& E
  }
$$

In terms of the imagery of loop spaces objects, the comma category is the category of [[interval object|directed paths]] in $E$ which start in the image of $f$ and end in the image of $g$.


# Examples #

* If $f$ and $g$ are both the identity functor of a category $C$, then $(f/g)$ is the category $C ^{\mathbf{2}} $ of arrows  in $C$.

* If $f$ is the identity functor of $C$ and $g$ is the inclusion $1\to C$ of an object $c\in C$, then $(f/g)$ is the [[over category|slice category]] $C/c$.

* Likewise if $g$ is the identity and $f$ is the inclusion of $c$, then $(f/g)$ is the [[under category|coslice category]] $c/C$.


# 2-categorical properties #

The comma category $(f/g)$ comes with a canonical 2-cell in the square

+--{: style="text-align:center"}
[[!include comma category/2cell]]
=--
which is universal in the [[2-category]] [[Cat]]; that is, it is an example of a [[2-limit]] (in fact, it is a [[strict 2-limit]]).  Squares with the same universal property in an arbitrary 2-category are called _comma squares_ and their top left vertex is called a [[comma object]].

# Further properties #

* [[functors and comma categories]]

# Discussion about terminology #

The terminology "comma category" is a holdover from the original notation $(f,g)$ for such a category, which generalises $(x,y)$ or $C(x,y)$ for a [[hom-set]].

+--{.query}
It\'s a very natural notation, as it generalises the notation $(x,y)$ (or $[x,y]$ as is now more common) for a [[hom-set]].  But personally, I like $(f \rightarrow g)$ (or $(f \searrow g)$ if you want to differentiate from a cocomma category, but that seems an unlikely confusion), as it is a category of arrows from $f$ to $g$.
&#8212;[[Toby Bartels]]

[[Mike Shulman|Mike]]:  Perhaps.  I never write $(x,y)$ for a hom-set, only $A(x,y)$ or $hom_A(x,y)$ where $A$ is the category involved, and this is also the common practice in nearly all mathematics I have read.  I have seen $[x,y]$ for an internal-hom object in a [[closed monoidal category]], and for a hom-set in a [[homotopy category]], but not for a hom-set in an arbitrary category.

I would be okay with calling the comma category (or more generally the [[comma object]]) $E(f,g)$ or $hom_E(f,g)$ _if_ you are considering it as a discrete fibration from $A$ to $B$.  But if you are considering it as a _category_ in its own right, I think that such notation is confusing.  I don't mind the arrow notations, but I prefer $(f/g)$ as less visually distracting, and evidently a generalization of the common notation $C/x$ for a [[over category|slice category]].

_Toby_: Well, I never stick '$E$' in there unless necessary to avoid ambiguity. I agree that the slice-generalising notation is also good. I\'ll use it too, but I edited the text to not denigrate the hom-set generalising notation so much.

_Mike_: The main reason I don't like unadorned $(f,g)$ for either comma objects or hom-sets is that it's already such an overloaded notation.  My first thought when I see $(f,g)$ in a category is that we have $f:X\to A$ and $g:X\to B$ and we're talking about the pair $(f,g):X\to A\times B$ &#8212; surely also a natural generalization of the _very_ well-established notation for ordered pairs.

_Toby_: The notation $(f/g/h)$ for a [[double comma object]] makes me like $(f \to g \to h)$ even more!

_Mike_: I'd rather avoid using $\to$ in the name of an object; talking about projections $p:(f\to g)\to A$ looks a good deal more confusing to me than $p:(f/g)\to A$.

_Toby_: I can handle that, but after thinking about it more, I\'ve realised that the arrow doesn\'t really work.  If $f, g: A \to B$, then $f \to g$ ought to be the set of transformations between them.  (Or $f \Rightarrow g$, but you can\'t keep that decoration up.) 

[[Mike Shulman|Mike]]: Let me summarize this discussion so far, and try to get some other people into it.  So far the only argument I have heard in favor of the notation $(f,g)$ is that it generalizes a notation for hom-sets.  In my experience that notation for hom-sets is rare-to-nonexistent, nor do I like it as a notation for hom-sets: for one thing it doesn't indicate the category in question, and for another it looks like an ordered pair.  The notation $(f,g)$ for a comma category also looks like an ordered pair, which it isn't.  I also don't think that a comma category is very much like a hom-set; it happens to be a hom-set when the domains of $f$ and $g$ are the point, but in general it seems to me that a more natural notion of hom-set between functors is a set of natural transformations.  It's really the _fibers_ of the comma category, considered as a fibration from $C$ to $D$, that are hom-sets.  Finally, I don't think the notation $(f,g)$  scales well to [[double comma objects]]; we could write $(f,g,h)$ but it is now even less like a hom-set.

[[Urs Schreiber|Urs]]: to be frank, I used it without thinking much about it. Which of the other two is your favorite? By the way, Kashiwara-Schapira use $M[C\stackrel{f}{\to} E \stackrel{g}{\leftarrow} D]$. Maybe $comma[C\stackrel{f}{\to} E \stackrel{g}{\leftarrow} D]$? Lengthy, but at least unambiguous. Or maybe ${}_f {E^I}_g$? 

[[Zoran Skoda]]: $(f/g)$ or $(f\downarrow g)$ are the only two standard notations nowdays, I think the original $(f,g)$ which was done for typographical reasons in archaic period is abandonded by the LaTeX era. $(f/g)$ is more popular among practical mathematicians, and special cases, like when $g = id_D$) and $(f\downarrow g)$ among category experts...other possibilities for notation should be avoided I think. 

[[Urs Schreiber|Urs]]: sounds good. I'll try to stick to $(f/g)$ then.

[[Mike Shulman|Mike]]: There are many category theorists who write $(f/g)$, including (in my experience) most Australians.  I prefer $(f/g)$ myself, although I occasionally write $(f\downarrow g)$ if I'm talking to someone who I worry might be confused by $(f/g)$.

[[Urs Schreiber|Urs]]: recently in a talk when an over-category appeared as $C/a$ somebody in the audience asked: "What's that quotient?". But $(C/a)$ already looks different. And of course the proper $(Id_C/const_a)$ even more so. 

Anyway, that just to say: i like $(f/g)$, find it less cumbersome than $(f\downarrow g)$ and apologize for having written  $(f,g)$ so often.

_Toby_:  I find $(f \downarrow g)$ more self explanatory, but $(f/g)$ is cool.  $(f,g)$ was reasonable, but we now have better options.

=--

# Further reading #

[a low-tech description with several special cases identified in somewhat archaic terminology](http://toby.bartels.name/notes/#comma)

[[!redirects comma categories]]
