tags: #clojure , #groundup , #fp 
links: [[CFGU - Intro]] [[Emacs Keybinds & Workflow]] [[Clojure Intro]]

Types:
What is a type -> Property that some values share (group of values which work in the same way, share the same properties)
Can overlap and intersect with each other (share properties). Types can be hierarchical (subsume one another) -> makes it easy to write programs which don't need to know the specifics of every value.

Type System -> way of organizing nouns into types.
Clojure has a *strong* type system [[CFGU - Intro]]. This means that operations on improper types are not allowed (unlike javascript where type coercion or implicit conversions can happen). Clojure is also dynamically typed (enforced at runtime vs compile time)