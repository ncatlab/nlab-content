
#Contents#
* automatic table of contents goes here
{:toc}


## Idea

The **bar construction** takes a [[monad]] $(T, \mu, \epsilon)$ equipped with an algebra-over-a-monad $(A, \rho)$ to the (augmented) [[simplicial object]]

$$
  \cdots
  \stackrel{\to}{\stackrel{\to}{\to}}
  T T A
  \stackrel{\stackrel{\mu \cdot Id_A}{\to}}{\stackrel{T \cdot \rho}{\to}}
  T A \stackrel{\rho}{\to} A
  \,.
$$

This simplicial object typically serves as an acyclic replacements or [[homological resolution]] of $A$.

For the moment, see the reference below for details.


## Special cases

### For differential graded (Hopf) algebras

See [[bar and cobar construction]].


## References

* [[Todd Trimble]], _On the Bar Construction_ ([blog](http://golem.ph.utexas.edu/category/2007/05/on_the_bar_construction.html))


[[!redirects bar constructions]]