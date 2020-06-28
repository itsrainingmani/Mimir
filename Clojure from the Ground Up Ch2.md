tags: #clojure , #groundup , #fp 
links: [[202006231340 Clojure from the Ground Up Ch1]] [[Emacs Keybinds & Workflow]] [[202006221951 Clojure Intro]]

Types:
What is a type -> Property that some values share (group of values which work in the same way, share the same properties)
Can overlap and intersect with each other (share properties). Types can be hierarchical (subsume one another) -> makes it easy to write programs which don't need to know the specifics of every value.

Type System -> way of organizing nouns into types.
Clojure has a *strong* type system [[202006231340 Clojure from the Ground Up Ch1]]. This means that operations on improper types are not allowed (unlike javascript where type coercion or implicit conversions can happen). Clojure is also dynamically typed (enforced at runtime vs compile time)