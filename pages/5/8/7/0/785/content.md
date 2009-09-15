# Idea #

A **homotopy pullback** is the appropriate notion of [[pullback]] in the context of [[homotopy theory]]. They model the [[limit in quasi-categories|quasi-category pullbacks]] in the [[(infinity,1)-category]] that is [[presentable (infinity,1)-category|presented]] by a given [[homotopical category]].  It is a special case of the notion of [[homotopy limit]].  Since pullbacks are also called fiber products, homotopy pullbacks are also called **homotopy fiber products**.


# Definition #

As with all homotopy limits, there is both a _local_ and a _global_ notion of homotopy pullback.

The _global_ definition says that the homotopy pullback of a a [[co-span|cospan]] $X \to Z \leftarrow Y$ in a [[category with weak equivalences]] $C$ is its image under the right [[derived functor]] of the [[base change]] functor $pb: C^{\to \leftarrow} \to C$.

The _local_ definition says that the homotopy pullback of $X \to Z \leftarrow Y$ in a category with a notion of [[homotopy]] consists of a square
$$
  \array{
   P & \to& Y
   \\
    \downarrow && \downarrow
   \\
   X &\to& Z
  }
$$
that [[commutative square|commutes]] up to [[homotopy]], and such that for any other square
$$
  \array{
   T & \to& Y
   \\
    \downarrow && \downarrow
   \\
   X &\to& Z
  }
$$
that commutes up to homotopy, there exists a morphism $T\to P$ making the two triangles commute up to homotopy, and similarly for homotopies and higher homotopies.  In other words, there is an equivalence
$$Map(T,P) \simeq HoSq(T,X\to Z\leftarrow Y)$$
between the space of maps $T\to P$ and the space of homotopy commutative squares with vertex $T$.

In good situations, such as when $X,Y,Z$ are [[fibrant object|fibrant]] in a [[model category]], the two constructions agree up to weak equivalence.

Note that in both cases, there is a canonical map from the actual pullback $X\times_Z Y$ to the homotopy pullback $X\times_Z^h Y$.  In the global case this comes by the definition of a derived functor; in the local case it comes because a commutative square is, in particular, a homotopy commutative one.


# Concrete construction

Suppose now that $Z$ has a [[path object]] $Z^I$ that represents homotopies into $Z$.  (For instance, this is often the case when $C$ is a [[closed monoidal homotopical category]] with an [[interval object]] $I$.)  Then we can consider the (ordinary) [[limit]]
$$
  \array{
     X \times_{Z}^h Y
     &\to&\to& \to& Y
     \\
     \downarrow
     &&&& 
     \downarrow
     \\
     \downarrow
     &
     &
     Z^I
     &\stackrel{d_1}{\to}&
     Z
     \\
     \downarrow
     &
     &
     \downarrow^{d_0}
     \\
     X
     &
     \to
     &
     Z
  }
  \,.
$$
or equivalently as the ordinary pullback
$$\array{X\times_Z^h Y & \to & Z^I\\
  \downarrow && \downarrow \\
  X\times Y & \to & Z\times Z.}
$$
In good situations, this will be a (local) homotopy pullback of $X \to Z \leftarrow Y$.  This is the case when $C = $ [[Top]] with its canonical [[interval object]] $[0,1]$, and also in many [[model category|model categories]] (when $X,Y,Z$ are fibrant) and [[category of fibrant objects|categories of fibrant objects]].  For details on the latter case, see [section 5](http://ncatlab.org/schreiber/files/nacqFeb14.pdf#page=21) of [[schreiber:Nonabelian cocycles and their sigma model QFTs]].

The canonical morphism $X \times_{Z} Y \to X \times_Z^h Y$ here is induced by the section $Z \to Z^I$.

The homotopy pullback constructed in this way is an example of a _strict homotopy limit_, as mentioned at [[homotopy limit]].  In such a case, one can say that an arbitrary homotopy-commutative square
$$
  \array{
   W & \to& Y
   \\
    \downarrow && \downarrow
   \\
   Y &\to& X
  }
$$
is a homotopy pullback square if the induced morphism from $W$ to the strict homotopy pullback is a [[weak equivalence]].

# Fibration sequences #

Of particular interest are

[[!redirects homotopy pullbacks]]
