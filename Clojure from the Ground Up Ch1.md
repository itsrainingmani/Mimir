tags: #clojure, #groundup, #fp
links: [[Emacs Keybinds & Workflow]] [[Clojure Intro]]

https://aphyr.com/posts/301-clojure-from-the-ground-up-welcome

Clojure is a modern dialect of Lisp. Expressive, Concise with powerful meta-programming.
It has well designed core library (Also access to the Java ecosystem and functions). Emphasizes Type Safety (runtime). Interactive REPL allows you to rapidly iterate on code and see the output of your code as you write.

Basic Types:
* `nil` is nothing (emptiness)
* 0, -47, 1.2e4, 1/3 - numerics
* "hello there" - string

core functions:
The symbol `inc`  points to the function `#<core$inc clojure.core$inc@6f7ef41c>`. This is something that can be evaluated. Whereas primitive types are values, a function name is a reference.

Escape a sentence that can be evaluated with `'`. This doesn't evaluate the expression but returns the text itself, unchanged.

LISP => LISt Processing. Lists are the most basic compositional form. It is a single expression with multiple parts (including nested expressions). Heterogenous collection.

Ex: `(nil "hey delilah")`, `(1 (2 (3 ())))`

List can be thought of like a Tree of expressions (AST) where the most nested expressions (deepest node) are recursively evaluated to yield a value at the end.

Every list starts with a "verb". And lists are evaluated from left to right. Innermost lists are evaluated before outermost ones.

List just makes the tree of expressions structure explicit compared to other languages. 