## Progress graphs

# Contents
* automatic table of contents goes here
{:toc}
## Idea. 
**Progress graphs** are a simple model for a certain aspect of concurrency theory in Computer Science. The basic idea is to give a description of what can happen when several processes are modifying shared resources.  Given a shared resource, $a$, we consider it as a semaphore which controls its behaviour with respect to processes. (This is a bit like the counter or token used in some old single track railway systems to prevent two trains being on the same stretch of line at the same time.) We are not worried exactly how the resource is used merely the 'locking' and 'unlocking' of the access to that resource.  For instance, $a$ may be a shared variable, so a semaphore is used to ensure that only one process can write on it at a time. (Editing pages in the n-Lab is another example!)

Our system will have $n$ deterministic sequential processes $Q_1, \ldots, Q_n$ Each will be abstracted as a sequence of 'locks' (denoted $P$) or 'unlocks' (denoted $V$) applied to shared resources (denoted $a$ with suffices and superfixes to distinguish them), so $Q_i = R^1a^1_i.R^2a^2_i\ldots R^{n_i}a^{n_i}_i$, as so one. Here each $R$ is an occurrence of a $P$ or a $V$.

There is a natural way to understand the possible behaviours of the concurrent execution of these processes. We associate to each process a different coordinate  direction in the topological space, $\mathbb{R}^n$. The state of the system correponds to a point in $\mathbb{R}^n$ whose $i^{th}$ coordinate describes the state or  'local time' of the  $i^{th}$ process.

(To be continued... with a PICTURE!)


##References##

(This entry is adapted from the treatment of the idea in the following paper:)

 *  [[Eric Goubault]], [[Some geometric perspectives in concurrency theory]], 
