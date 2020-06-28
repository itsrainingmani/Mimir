tags: #clojure , #fp , #groundup 
links: [[202006231444 Clojure from the Ground Up Ch2]]

Symbols are names for things and when evaluated, Clojure replaces the symbols with their corresponding values.

Define a meaning for a symbol within a specific expr with let

let applies only within the local expr. It can override any existing defintions for symbols.

multiple bindings are evaluated in order. later bindings can use earlier ones

(def astronauts []) ;; => #'ground-up.core/astronauts
(count astronauts) ;; => 0

(def astronauts ["Sally Ride" "Guy Bluford"])
(count astronauts) ;; => 2
The value of astronauts depends on when we evaluated it. Redefining names this way changes the meaning of expressions everywhere in a program.
Good for REPL work. But could be dangerous in production
Idiomatic way is to use def to set up a program initially and only change those defs with careful though

Clojure introspection:

`type` gives you the concrete type of an object. If `type` isn't being useful, use `supers` to get all the supertypes of the object. Supertypes is the set of all types that includes the given `type`. 
We can check if a given object is a function with `fn?`. We can get the documentation for a function with `doc`. Want to find the associated metadata for an object? Simply use `(meta #'obj)`. Confused how a function is implemented? Fret not, `source` is here to save the day.

Almost every function in a programming language is made up of other simpler functions. However there are certain constructs that cannot be reduced further. In Clojure, `def ` and `let` are these types of special forms.