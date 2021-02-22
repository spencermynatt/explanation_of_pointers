# explanation_of_pointers
39
"
Pointers are best understood by C & C++'s differences in variable passing to functions.

Yes, you can pass either an entire variable or just a pointer to it (jargon is by value or reference, respectively).

But what if the variable is 20 meg array of bytes, like you decided to read an entire file in to one array? Passing it by value would be foolish: why would you copy 20 megs for this operation, and if you end up modifying it (i.e. it's an out-parameter) you have to copy that 20 megs BACK?

Better is to just "point" to it. You say, "here's a pointer to a big blob of memory". And that little indirection saves a ton of time.

Once you understand that, everything else is basically the same. Rearranging items in a list becomes just swapping pointers rather than copying every item around, you don't need to know how big things are when you start out, etc
"
