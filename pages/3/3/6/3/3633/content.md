<div class="rightHandSide toc">
[[!include physicscontents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Wick rotation is a method for finding a solution to a problem in Minkowski space from the solution to a related problem in Euclidean space.  It is motivated by the observation that the Minkowski metric (with the -1,1,1,1 convention) and the four-dimensional Euclidean metric are equivalent if the time components of either are allowed to have complex values.

### Example

Consider the Minkowski metric with the -1,1,1,1 convention for the tensor:

$ds^{2}= -(dt)^{2} + (dx)^{2} + (dy)^{2} + (dz)^{2}$

and the four-dimensional Euclidean metric:

$ds^{2}= d\tau^{2} + (dx)^{2} + (dy)^{2} + (dz)^{2}$.

Notice that if $d t=i\cdot d\tau$, the two are equivalent.

## Method

A typical method for employing Wick rotation would be to make the substitution $t=i\tau$ in a problem in Minkowski space.  The resulting problem is in Euclidean space and is sometimes easier to solve, after which a reverse substitution can be performed, yielding a solution to the original problem.

Technically, this works for any four-vector comparison between Minkowski space and Euclidean space, not just for space-time intervals.