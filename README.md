The UK101 was itself a clone of the Ohio Scientific Challenger 1E/ SUperboard 2.

I owned a C1E from around Christmas 1979. Thanks to my dad (RIP) for purchasing this machine for me (which wasn't cheap compared to his salary) and which ended up launching my carrier in electronics and computing.

Starting point is Grant Searle's implementation of a clone of the UK101 on an inexpensive FPGA. Full credit to the original authors.

```
The original copyright owners of ROM contents are respectfully acknowledged.
Use of the contents of any file within your own projects is permitted freely,
but any publishing of material containing whole or part of any file distributed here,
or derived from the work that I have done here will contain an acknowledgement back to myself,
Grant Searle, and a link back to this page.
```

Link to the relevant source page: http://searle.x10host.com/uk101FPGA/index.html#MyOtherPages

My aim is to extend to include with various features I'd like to recreate my own original Ohio Scientific Challenger 1E (Superboard II) that I owned circa 1980.

+ Switchable CPU Overclocking (1MHz or 2MHz clock) - my C1E was overclocked to 2MHz
+ Switchable video RAM (1624 - 3248 approx) - my C1E had additional video RAM and a modified clock circuit
+ Switchable Character ROM - The UK101 and C1E had slightly different character sets.

But first: recreate the original basic machine with FPGA only and then incremental releases. One branch per change so we can move forward and back.

My own work is released under the free-est licence possible, the MIT licence.
