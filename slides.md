%title: Carp: A Language for the 21st century
%author: Veit Heller
%date: 2018-03-31

---

-> # Always start with a bold claim, right? <-

---

-> # What?

* Compiled Lisp without garbage collector
* Strong and simple C interoperability
* Syntax inspired by Clojure

---

-> # Why?

* Lisps (traditionally) always have garbage collection
* no hard realtime :(
* games and other multimedia applications are hard
  to program like that

---

-> # Why?

* Lisps (traditionally) are dynamically typed
* makes it harder to compile them efficiently
* generates avoidable runtime errors

---

-> # Why?

Enter Haskell
* let’s have Hindley-Milner typing, it’s super powerful!
* let’s have types be inferred by the compiler!

---

-> # Why?

Enter Rust
* let’s have ownership and borrowing semantics!
* we can throw away the garbage collector by inferring
  when to allocate and free memory

---

-> # Why?

* Haskell has garbage collection
* Rust has explicit typing
* :(

---

-> # Why?

Enter Carp
* Hindley-Milner types
* Ownership/borrowing semantics
* Powerful Lisp macro system on top!

---

-> # Show me some code!

```
(def x 1)
  
(defn main []
  (IO.println (str (+ x 10))))
```

---

-> # What about some real code?

```
(deftype Vector [x Int y Int])
  
(defmodule Vector
  (defn + [a b]
    (Vector.init (+ (x a) (x b))
                 (+ (y a) (y b))))
)
  
(defn main []
  (IO.println (str (+ (Vector.init 1 2)
                      (Vector.init 3 4)))))
```

---

-> # What about some real real code?

---

-> # Let’s talk about anima

* I wrote a drawing microframework
* SDL-based
* Inspired by Processing
* setup/draw functions
* Super lightweight (111 lines)

---

-> # Demo time!
