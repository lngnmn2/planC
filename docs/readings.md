- [The Architecture Of Complexity](#orgebb5564)
- [Discrete-time signal processing (Alan V. Oppenheim)](#orgabb897b)
- [Time series](#org162fe12)



<a id="orgebb5564"></a>

# The Architecture Of Complexity

This is, perhaps, the most important paper (for actually smart people).

The date is **1962**, so this is just 2 years after John McCarthy published his LISP paper for the first time.

All the fine people supposedly have read this, B. Liskov, Guy L. Steele, Gerald Sussman, P. Norvig, SPJ.

It has been written by a theoretician. Theoreticians, in general, does not care about precision and rigor, so every single assertion could be independently verified by anyone, but they sometimes have so-called &ldquo;insights&rdquo; and properly capture important generalities.

This short paper basically says that you have to design your program as a set of *layered embedded DSLs*, so it **will be** as robust as possible and **will be** developed *faster*, if one uses &ldquo;bottom-up process&rdquo; (*after* &ldquo;top-down&rdquo; problem domain decomposition) in prototyping.

The notion of &ldquo;stable intermediate forms&rdquo; is, indeed, *universal*. So is the notion of *partitioning* and of a *hierarchy of layers*, which is what a complex system decomposes into (atoms, molecules, aminoacids, proteins are obviously form distinct layers and have actual &ldquo;abstraction barriers&rdquo; at each level).

Another universal and fundamental notion in this short paper is of a *heuristic-based back-tracking search as a universal strategy of problem-solving*. He did not use these terms, but he talks abot &ldquo;trial-and-error search process&rdquo; and &ldquo;*selectivity* based on heuristics and rules of thumb&rdquo;.

This is exactly what happens in human societies. Instead of so-called &ldquo;free will&rdquo; individuals are just bouncing around within their social, economic and genetic *constraints*, trying this and that and &ldquo;seeing what sticks&rdquo;.

But the &ldquo;stable intermediate forms&rdquo; (which are *reused* (!) and your own data-types, functions, modules) and the layered architecture (of embedded DSLs) was a *revelation*.

LISP guys got it. They even got *homoiconicity* from cell biology. Everything &#x2013; enzymes, which are just particularly folded proteins, and the &ldquo;data&rdquo; (other proteins) &#x2013; has been made from *sequences* of the same 20 aminoacids.

The only thing that &ldquo;missed&rdquo; is the subtle notion from Haskell, where the monadic code *form actual membranes* with &ldquo;pumps&rdquo; and &ldquo;portals&rdquo;, and the I/O code (and other effects) tent to stay &ldquo;at the edges&rdquo;.

*Every Monad defines and implicit abstraction barrier* (using Kleisli arrows, which we call `return` or &ldquo;lifting&rdquo; in general), but his is another story, this time by me.

[The Architecture Of Complexity (Herbert A. Simon, 1962)](https://faculty.sites.iastate.edu/tesfatsi/archive/tesfatsi/ArchitectureOfComplexity.HSimon1962.pdf)


<a id="orgabb897b"></a>

# Discrete-time signal processing (Alan V. Oppenheim)

The most dense books, but the fundamental concepts and proven techniques has to be extracted from them.

This is the essence of learning &#x2013; to extract the right understanding from poorly written books.


<a id="org162fe12"></a>

# Time series

Very difficult to find a definitive, conscise well-written non-bullshit book.

My general heuristic is to look for something from the *MIT Press* first.
