# checking types in interpreters is costly
Some lisp language added typing. However the issue was passing data to the old
core libraries. If you pass data untyped you have unchecked code. If you check
the types before passing your app turns slow
