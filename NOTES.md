# Notes and ideas pertaining to Bone Lisp

* [Reddit](https://www.reddit.com/r/lisp/comments/4mtktn/bone_01_lisp_without_garbage_collection/)
* [GitHub](https://github.com/wolfgangj/bone-lisp/)

I had started thinking that a GC-less Lisp could be a good thing to connect to the
Linux kernel as a sort of kernel scripting language. You don't want GC in that case.
I started to think about it, and then discovered that somebody got there first, so
here's my git clone of Bone Lisp. It does not use GC and the values are immutable.

> Bone is an interpreter for a lexically scoped Lisp-1.
> It is based on immutable values and does tail-call elimination.
> The special feature that distinguishes it from other Lisps is the *semi-automatic memory management*:
> It uses explicit regions instead of garbage collection.

I should probably study how these explicit regions work. My quick (and probably
wrong) initial impression is that it's similar to Rust.

If I made this a Linux kernel module, how would it do stdin/stdout/stderr?
