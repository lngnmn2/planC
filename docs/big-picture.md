I am already a quite old guy, at least other people threat me as one. This means that I have tried (and failed) quite a lot of things, and have got in return something what they call &ldquo;experience&rdquo;. At least I have read some, here and there.

When one &ldquo;studies&rdquo;, lets say, Indian or Buddhist philosophy (well, this is a *vast* subject) there is a distinct, recurring (again and again) common pattern &#x2013; the early intuitive and shared experience-based teachings (of the ancients) are getting systematically destroyed and transformed into incomprehensible verbiage vomit of abstract terminology.

All the &ldquo;famous commentators&rdquo; just introduced more and more &ldquo;primitive&rdquo; abstractions (which they think as refinements) and turned the teaching, pure and simple, into a scholastic shitfest. Moreover, most of them do not know when to stop, and are keeping producing more and more &ldquo;spiritual&rdquo; verbiage.

There is *always*, nowever, the end of a search, the end of knowledge, when the whole &ldquo;maze&rdquo; has been explored (and nothing more &ldquo;real&rdquo; that it itself has been found).

The rare insights of the Upanishads has been turned by &ldquo;commentators&rdquo; into abstract doctrines, the teaching of the Buddha has been turned into ritualistic mumbling, just like Brahmanas turned everything into endless sacrifice rituals.

You may think that such things (social movements which the pattern captures) happens only in the distant past, and now we are all rational and even &ldquo;scientific&rdquo; instead of speculative and too abstract. Hardly.

The early teachings of what we call &ldquo;Computer Science&rdquo; has been ruined and transformed (by &ldquo;creative&rdquo; idiots) into incomprehensible abstract bullshit in exactly the same way, turning everything into a syntactic vomit of unnecessary, redundant abstractions (which is the root of all evil).

This is not an exaggeration in the least. By the late 90s, with the emergence of the Haskell 98 standard (and the R5RS prior to it), as well as refinement of the ML (and then Ocaml) modules with functors, *everything* out there has been well-understood. The abstract interfaces, a generalization of ADTs, and corresponding small modules which hide all the (representation and implementation) details, has been placed at the center of what a non-bullshit programming (the science of managing complexity) is really.

At least 3 distinct traditions has been emerged from the Simply-Typed Lambda Calculus and ISWIM &#x2013; the ones of SML/Ocaml, Scheme and the most notably, of Miranda/Haskell. Erlang and Scala emerged as schisms of their own.

There are a few distinct &ldquo;patterns&rdquo; which are common of all of these traditions &#x2013; a minimal subset of special forms in a mostly functional language which is good-enough (even optimal) for everything. Technically, the intermediate language of the Glasgow Haskell Compiler, which corresponds to the *System F Omega*, is that &ldquo;core&rdquo;.

When one is looking at these special forms and is trying to draws the arrows between dots, one (if smart enough) would discover more distinct common patterns. These has been *partially* captured by the algorithm charting techniques from the 70s.

Unsurprisingly, if we add *the structural pattern matching* (on Algebraic Data Types), which all the ML tradition languages have, one will see &ldquo;the complete picture&rdquo; &#x2013; a better branching (more arrows going out). All the &ldquo;special forms&rdquo; are reducible to just a few universal patterns of &ldquo;arrows between dots&rdquo; (to which the Category Theory has arrived by another route).

Since the 90s, the smartest people (who gave us CLU, SML and Haskell) told us, that *this* is good-enough for everything and even that *this* is how to manage complexity and how to compute.

If one knows some very basic cell biology, one would see the very same patterns &ldquo;Out There&rdquo;, just as the early LISP guys did (when freshly discovered the actual structure of DNA was a big deal).

Unlike liberal arts &ldquo;educated&rdquo; people used to babble about &ldquo;boundless creativity&rdquo; (the word-marker of an idiot), we do not have endless structures. Actually, we have *sequences, tree-like structures and a lookup tables*, where a *partial* (and a total) function could be thought off (correctly represented as) a lookup table.

DNA transcription machinery do &ldquo;table lookups&rdquo; and produce sequential structures, which spontaneously fold themselves into &ldquo;stable forms&rdquo;.

Just like the early LISP procedures were made out of LIST structures (nested pairs with a &ldquo;CAR&rdquo; and a &ldquo;CDR&rdquo;), all other basic data structures (*alists*, *trees*) were made from just &ldquo;CONSes&rdquo;. This wasn&rsquo;t a mere coincidence, of course.

The next big idea is *Immutability* of all bindings &#x2013; both *symbol bindings* (in an environment, which were originally just bunch of nested *alists*) and *data bindings*. *Clojure* persued the immutability of bindings to its limit with a great success.

Guess what? Immutable *balanced trees* which represent (and implement) everything else (all the proper non-leaking ADTs), including &ldquo;flat&rdquo; sequences (the actual Machine Types such as arrays are grossly overhyped).

Again, an immutable *binding* (the old terminology was inspired by math and is so much better!) of a symbol to a value or of slots of a record type to a corresponding value is the most fundamental building block, just as in math itself. Unsurprisingly, the molecular structures which constitute the basis of Life Itself are &ldquo;supposed to be&rdquo; immutable (or at least stable-enough).

Then it has been realized that just *product-types, sum-types and function types* are enough for everything. Not just that, but they correspond to the most fundamental shapes &#x2013; sequences and lookup tables (alists), and to the logical notions of `AND` `OR` and `->`, which is, of course, not a random coincidence.

So, one begins to see (and so becomes a &ldquo;seer&rdquo;) the big picture of a small number of the universal &ldquo;forms&rdquo; which underlay almost everything (and the reccuring patterns of &ldquo;dots between arrows&rdquo; one level behind them). *All* your abstract types (ADTs) can be just properly *Algebraic* and even immutable.

And suddenly, someone like me discovered that Monads in Haskell (which is, just a type-class for a simple ADT of a Monoidal composition) corresponds to a the notion of a universal abstraction barrier, or of a cell-membrane.

The really smart guys (around Odersky) were generalized the *for-comprehensions* around Monadic composition, and this is where we are today.

Now, how many people have actually comprehended and realized all this? I know of no one else. You would be the first to learn all this from here.

The classic books about the classic languages are the source of the &ldquo;ancient&rdquo;, first intuitive, and then shared experience-based knowledge (because it properly captures some aspects of *What Is*), just, unsurprisingly, like the seers of Upanishads and the early Buddhists.

*L. C. Paulson. ML for the Working Programmer* is one of such classic books. The *&ldquo;Bird & Wadler&rdquo;* is another one (here I am showing you *the way*).
