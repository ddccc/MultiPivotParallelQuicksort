The paper "Boosting 1, 2 & 3 Pivot Quicksort through Hybridization and
Parallelization" describes the performance of 1-pivot FourSort,
2-pivot FiveSort, 3-pivot SixSort against the competion.  A design
pattern for the parallelization of these algorithms is described also.

The abstract::

Quicksort's quadratic worst case is a thing of the past through
hybridization with heapsort. Onepivot quicksort benefits from further
hybridization by using slow and fast 'collapsing the walls' loops,
which respectively focus on minimizing comparisons using index checks
versus maximizing speed by relying on sentinels that block running
into an (initialized) segment.  Recognizing 'troublesome'
distributions and forwarding them to a Dutch Flag algorithm member
that puts elements equal to the pivot in the middle leads to further
hybridization. We show a favorable 0.86 timing ratio against the best
one-pivot competitor we have identified on uniform distributions and a
0.90 timing ratio on a family of 'troublesome' distributions. Our
two-pivot version has an additional algorithm member, which compares
favorable against the only competitor identified. The comparison count
of our two-pivot hybrid, while better than the competitor, is still
unfavorable against our one-pivot hybrid. This result is consistent
with our optimistic, best case complexity analysis. Our three-pivot
hybrid replaces the two-pivot member with one that partitions a
segment in four regions. This one compares also favorable, 0.81 timing
ratio, against the only competitor we have identified. A fourth topic
is a design pattern using the C pthread package with which we
parallelized our novel hybrids. Favorable speed ups are reported for
the number of threads in the range 2-7. Replacing pairwise swapping by
the single element moving technique, using finite state machine
control logic in some of our algorithm members, and using two-gap
array layouts have been key design decisions for the achieved speedups
on the varying distributions. Timing tests on three generation
machines with different caching architectures showed only minimal
differences.
