Quite roughly speaking, a topos is a [[category]] that resembles the category of sets and functions enough that we can use it as a 'universe' to do mathematics in.  For a longer introduction, try:

* John Baez, [Topos Theory in a Nutshell](http://math.ucr.edu/home/baez/topos.html).

A quick formal definition is that an **(elementary) topos** is a category which

1. has [[finitely complete category|finite limits]],
1. is [[cartesian closed category|cartesian closed]], and
1. has a [[subobject classifier]] $\Omega$.

There are alternative ways to state the definition.  For instance, from finite limits and _[[power object]]s_ $\Omega^X$ we can construct all exponentials and the subobject classifier $\Omega = \Omega^1$.

In a way, however, these concise definitions can be misleading, because a topos has a great deal of other structure, which plays a very important role but just happens to follow automatically from these basic axioms.  Most important are that a topos is [[locally cartesian closed category|locally cartesian closed]], has finite [[colimit]s, and is a [[Heyting category|Heyting]] [[pretopos]].  This implies that it has an [[internal logic]], and the presence of exponentials and power objects means that this logic is [[higher order logic|higher order]].

Some of the most important examples of toposes are [[Grothendieck topos]]es, which are the categories of [[sheaf|sheaves]] on [[site]]s.  The word "topos" was originally used only to mean Grothendieck's sort.
