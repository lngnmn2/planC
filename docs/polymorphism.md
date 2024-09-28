There is something very deep and profound behind the abstract notion of so-called *currying* (after Haskell B. Curry).

The trick, William Poter, is to think of a multiargument functions as being &ldquo;a syntactic sugar&rdquo; for a bunch of *nested* lambdas (closures), each of which *captures its single argument* and return another lambda (closure).

```scheme
(define plus (lambda (x)
               (lambda (y)
                 (+ x y))))

;; application is "explicit"
((plus 2) 3)
```

It is not a random coincidence that both definition and application expressions are explicitly *nested*.

Notice that there are always two distinct aspects &#x2013; a mathematical abstraction (on paper) and its representation (and implementation) inside a computer (in terms of some programming language).

In *Haskell* this is just

```haskell
> let plus = \x -> \y -> x + y
> plus 2 3
```

In classic languages (such as *ML*, *Haskell* and *Ocaml*) a multiargument function (both definition and application) is just a *syntactic sugar*, which &ldquo;desugars&rdquo; into a *nested lambdas* expression. So, in a pseudo-Haskell: `\x y ->` becomes `\x -> \y ->` and `f x y` becomes `(f x) y`.

It is not a random coincidence that the *type signature* looks like a path on a graph `a -> a -> a`:

```haskell
> :t plus
plus :: Num a => a -> a -> a
```

and as &ldquo;nested&rdquo; *implications*. These are just different abstract notions are of the same underlying universal phenomena.

Another &ldquo;universal&rdquo; notion of *Partial Application* comes &ldquo;naturally&rdquo; &#x2013; one just applies a function to a fewer arguments, just like a *partially filled enzyme* (which performs its &ldquo;action&rdquo; only when all necessary and sufficient &ldquo;slots&rdquo; are filled with particular molecular structures, usually *in any order*, or strictly in a particular order, which means that it will &ldquo;wait&rdquo; for a certain molecule to bind and potentially transform the shape of the enzyme in such a way that another &ldquo;slot&rdquo; will open). These things are so deep&#x2026;

In *Haskell*, just like in math, *any* function can be partially applied.

```haskell
> :t plus 2
plus 2 :: Num a => a -> a
> (plus 2) 3
5
```

This is not just a &ldquo;trick&rdquo; or a &ldquo;hack&rdquo;. A *partially applied* `map` *&ldquo;crosses an abstraction barrier&rdquo;* and yields a function *on lists*.

```haskell
> :t map (+1)
map (+1) :: Num b => [b] -> [b]
```

and more generally

```haskell
> :t fmap (+1)
map (+1) :: (Functor f, Num b) => f b -> f b
```

Switch the order of arguments of `fmap`, and then partially apply it to a particular &ldquo;context&rdquo; or an abstract &ldquo;container&rdquo;, and one will have a function which expects a &ldquo;transformation&rdquo; (a function) and returns a modified &ldquo;context&rdquo; or a &ldquo;container&rdquo;.

```haskell
> :t flip fmap
flip fmap :: Functor f => f a -> (a -> b) -> f b
```

Add the Functor laws (associativity of composition and left and right identities) and you will have essentially this:

```haskell
> :t (>>=)
(>>=) :: Monad m => m a -> (a -> m b) -> m b
```

Yes, there are lots of implementation details, such that a `Monad` is defined as a *type-class*, which defines an &ldquo;composition operator&rdquo; and an &ldquo;arrow&rdquo;:

```haskell
> :t return
return :: Monad m => a -> m a
```

and this particular kind of a *&ldquo;Kleisli arrow&rdquo;* is what the `(>>=)` requires.

The main point is that with just *nesting (function composition)* and *partial application* could yield something bigger than its parts.

Unfortunately, *Scheme* does not support partial application, but one can use another *wrapper* function, so *any* function could be *partially applied* (at least once).

```scheme
(define partially (lambda f . xs)
  (lambda ys
    (apply f (append xs ys)))
```

Now look.

Traditionally, in some languages *partial application* is expressed syntactically just as:

```scala
xs.map(f)
```

The semantics is exactly as `(map f) xs`, which, again, is &ldquo;given just `f` a *closure*, which captured `f`, is returned&rdquo; and it is being applied to `xs`".

So, what if the first partial application is not of a *formal parameter*, but of a *type* for an *&ldquo;implicit&rdquo;* type-parameter (type-variable)?

Suddenly, expressions like

```rust
fn min<T: Ord>(x: T, y: T) -> T {}
```

begin to look as what they really are.

Types have their own types (or the universe of types is being *partitioned* according to particular &ldquo;such that&rdquo; *constraints*), and a *&ldquo;partially applied to a particular type&rdquo;* genetic function *&ldquo;yields a concrete function on that type&rdquo;*.

These &ldquo;such that constraints&rdquo; is what a *type-class* (or a trait) defines *for types*, plus some additional rules or &ldquo;laws&rdquo; defined informally somewhere else.

Of course, in *Haskell* &ldquo;parameterized type-constructors&rdquo; can be *partially applied* to types to yield another type-constructors (which when fully saturated will yield a &ldquo;concrete type&rdquo;).

This is what a proper parametric polymorphism with type-classes (or traits) looks like. Notice that there is nothing &ldquo;arbitrary or random&rdquo; out there. The very same universal notions (from the Lambda Calculus), just at a type level.

And this is where we (the scholars of the classic languages) currently are.
