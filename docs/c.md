- [No idea how bad everything is](#org45a4564)



<a id="org45a4564"></a>

# No idea how bad everything is

In the preface to the Second Edition of the classic The C Programming Language book K&R clearly stated that &ldquo;C deals with the same sort of objects that most computers do, namely characters, numbers and addresses&rdquo;.

Everything was more or less OK back in the 1988. The smallest addressable chunk of memory was a byte. Characters were fit into a single byte. There were simple common (informal) *easy* rules for using `0` or `-1` as *markers* or for signalling an error. Life was seemingly easy.

&ldquo;Simple&rdquo; *null-terminated strings of bytes* everywhere, strings are *arrays*, not lists. Clever bits of special syntax for arrays access and modification. Everything was *easy*. Machine types as *bounded* sub-sets of integers and reals. Characters (and almost everything else) were just a set of binary numbers (which represent them), including any enums themselves.

Everything has been programmed in terms of representation, which very little of a proper abstraction (just like Lisp guys did with `car` and `cdr`). Proper ADTs (as by Barbara Liskov) were rare and even frowned upon. *The C programmers knew the representation of everything and the special value for nothing* (me).

Mathematicians would have already been alarmed about using an ordinary member of a set as a special case, instead of having a well-defined *sum-type* or a *disjoint union* &#x2013; the traditional and well-understood way mathematics deals with &ldquo;distinct possibilities&rdquo;.

This is actually a matter of principle. One obviously can partition a set further into subsets using *such-that* clauses with *predicates* and logical operators. `forall x, except x=0` is *easy* but stupid. Just as `forall x, except -1`, which means something else. These rules are stated informally and cannot be checked by a type-checker, unlike a tagged disjoint unions, which form the basis of proper sum-types.

Mathematicians favor (and seek) *uniformity*. They also favor and seek well-understood common (or even universal) *algebraic structures* which *emerge* again and again through different branches of mathematics (for a reason &#x2013; it has something to do with the underlying structure of the Universe itself).

This conscious and deliberate seeking for uniformity is what determine or establish the beauty and elegance of Functional Languages.

-   values are just &ldquo;what they are&rdquo; and are *immutable* like atoms (yes, yes, I know).
-   everything is an expression, which *denotes* (and can be *reduced* to) a value.
-   everything is an immutable *binding* of a symbol to a value (*names* does not change).
-   everyhing thus is uniformly passed (and returned) by a reference (which is immutable).
-   every compound data structure (a data binding) is immutable and *persistent*.
-   the same data structures denote (and represent) the expressions of a language itself.
-   just 3 algebraic data types (a sum, product and an arrow) are enough for everything.
-   etc.

This emergent, even spontaneous uniformity is due to orthogonal but complimentary set of universal rules. The resulting behavior of the system is definitely at a higher level (more sophisticated) than just &ldquo;combination&rdquo; (a sum) of individual parts.

Some questions just never arise in principle:

-   where in memory the datum is stored (irrelevant)
-   who and when will &ldquo;free&rdquo; the storage?
-   do I pass by a pointer (or a reference)?
-   when I &ldquo;allocate and return a pointer&rdquo;, then what?
-   who &ldquo;owns&rdquo; the data at a &ldquo;memory location&rdquo;?
-   how many pointers are pointing to it?
-   how do I make a copy of the [compound] data?
-   what if there is a resource handler (a descriptor) in there?
-   what if the data must be moved to another location?
-   etc.

Notice that the seemingly &ldquo;universal&rdquo; answer of Stroustrup, to wrap everything into a user-defined type (an ADT) which &ldquo;owns&rdquo; the data and does initialization and freeing (the infamous RAII) simply does not work. To be precise &#x2013; it works *only* when there is no concurrent access (with a preemptive multitasking) to a *shared state*, otherwise the state becomes *invalidated* in a non-deterministic way.

The [ignored] pragmatic theoreticians, like Joe Armstrong, who explicitly stated that unrestricted shared state and preemptive (a potential context switch at any moment, *between any two consequent* machine instructions in a code block) multitasking are *mutually exclusive*, had the right (the only correct) understanding.

Ignorance of this *universal principle* basically destroyed `C++` (which was seemingly literally impossible just a couple of years ago), giving the narcissistic overconfidence of the &ldquo;creator&rdquo;.

This, by the way, is not an abstract statement &#x2013; *an unrestricted concurrent destructive updates to an unprotected mutable state do not arise in biology as a pattern*. It is that universal and fundamental. Cells have membranes, especially the ones around nucleus, for this very purpose &#x2013; to protect its internal state (its specialization) and to restrict &ldquo;destructive updates&rdquo; to its &ldquo;information&rdquo;.

The &ldquo;`refs`&rdquo; of the classic ML-family language were a discovery, not an invention. ADTs are central to programming just as membranes are central to biology.

Languages like *Rust* (all the socially constructed &ldquo;correct pronoun&rdquo; bullshit aside) were the first *systematic* attempt to *restrict* the possible behavior of references (at most one exclusive mutable reference at a time, which behaves like *&rsquo;refs&rsquo;* in the classic functional languages) and values by explicitly adding the notion of an ownership, show clearly how bad things really are.

Understanding *precisely* what Rust did *and why* makes one a much better programmer. In short, it restricts the set of all possible expressions, just like the Simply Typed Lambda Calculus did to the way too general (and prone to paradoxes) original formalism.

Yes, it has some sort of RAII, but more importantly, in principle, it switches to a *move semantics by default* &#x2013; the previous location becomes *automatically* &ldquo;invalidated&rdquo; and *inaccessible* to any code after the assignment statement (a compile-time error). One has to verbosely write down how to *copy*, instead how to *move* a value (between memory locations).

biology, sequences, explicit start and stop markers, no counting (and counters) in principle multiframe, structural pattern-mathing, encoding and reading (!)
