tags: #emacs, #clojure 
links: [[Clojure Intro]]

Workflow for starting a CIDER session in a Clojure Project:

- Open the source code file within the src/<classname> folder
- `M-x cider-jack-in` to start a CIDER session and open a REPL
- `C-c C-z` to switch between REPL and Code
- `C-c C-k` to compile the current Clojure file
- `q` when there is an exception in the CIDER REPL to close the stack trace
	
Common Emacs Movement Keybinds
![[emacs-keybindings.png]]