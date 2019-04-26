---
layout: default
title:  "Design of Logic Environments"
categories: main
---

<h1 id="firstHeading" class="firstHeading" lang="en">Design of Logic Environments</h1>

<p>The
"nand" logic operation is considered functionally complete, which means
that using only nands it is possible to build any othr logic operation.
For this reason, we have chosen to give Avida organisms "nand" as one
of their instructions, and we can thereafter approximate the difficulty
of all of the other tasks by the number of nands it takes to complete
them.
</p><p>The nand operation functions as follows:
</p>
<table>
<tbody><tr><th>Input A&nbsp; </th><th>Input B&nbsp; </th><th>A nand B&nbsp;</th></tr>
<tr><td>0 </td><td>0 </td><td>1</td></tr>
<tr><td>0 </td><td>1 </td><td>1</td></tr>
<tr><td>1 </td><td>0 </td><td>1</td></tr>
<tr><td>1 </td><td>1 </td><td>0</td></tr>
</tbody></table>
<p>All 2-input logic operations can be described in the same fashion.
There are always 4 pairs of possible inputs, and the function is
described by the four bits in the right-hand column.  This means that
there are, theoretically 16 possible 2-input logic functions, but some
of these are trivial.
</p><p>Four of the logic operations require no nands at all.  They are
ALL-ZEROs, ALL-ONEs, ECHO-A, and ECHO-B.  In Avida we combine ECHO-A and
ECHO-B into a single task (ECHO) and we ignore ALL-ZEROs and ALL-ONEs
since they are trivial (a bit string with all zeros is just "0" and a
bit string with all ones evaluates to "-1").
</p><p>Given one NAND, we can determine whats possible by NANDing all
pairs of our no-nands values together and see what we get.  We have our
two inputs (A and B) and out ALL-ZEROs and ALL-ONEs to work with.
</p>
<table border="1">
<tbody><tr><th>NAND COMBOS </th><th>Input A </th><th>Input B </th><th>Zeros </th><th>Ones
</th></tr><tr><th>Input A </th><td>NOT-A    </td><td>A-NAND-B </td><td>ALL-ONES </td><td>NOT-A
</td></tr><tr><th>Input B </th><td>B-NAND-A </td><td>NOT-B    </td><td>ALL-ONES </td><td>NOT-B
</td></tr><tr><th>Zeros   </th><td>ALL-ONES </td><td>ALL-ONES </td><td>ALL-ONES </td><td>ALL-ONES
</td></tr><tr><th>Ones    </th><td>NOT-A    </td><td>NOT-B    </td><td>ALL-ONES </td><td>ALL-ZEROS
</td></tr></tbody></table>
<p><br>
Glancing through this, it looks like we get four new functions: NOT-A,
NOT-B, A-NAND-B, and B-NAND-A.  We also see that ALL-ZEROS and ALL-ONES
get us nothing new that we can't get from the other options, so we're
going to ignore them from here on out.
</p><p>Looking closer at the new functions, we realize the A-NAND-B is
identical to B-NAND-A (they both produce 1,1,1,0 in the last column), so
we lump them together into a single NAND function.  With this, we
discover that with a single nand we have uncovered three more 2-input
logic functions, for a total of seven so far.
</p><p>They are:
</p>
<table>
<tbody><tr><th colspan="9">2-Input Logic using zero or one nands.</th></tr>
<tr><th>Input A&nbsp; </th><th>Input B&nbsp; </th><th>ALL-ZEROS&nbsp; </th><th>ALL-ONES&nbsp; </th><th>ECHO-A&nbsp; </th><th>ECHO-B&nbsp; </th><th>NOT-A&nbsp; </th><th>NOT-B&nbsp; </th><th>NAND&nbsp;</th></tr>
<tr><td>0 </td><td>0 </td><td>0 </td><td>1 </td><td>0 </td><td>0 </td><td>1 </td><td>1 </td><td>1 </td></tr>
<tr><td>0 </td><td>1 </td><td>0 </td><td>1 </td><td>0 </td><td>1 </td><td>1 </td><td>0 </td><td>1 </td></tr>
<tr><td>1 </td><td>0 </td><td>0 </td><td>1 </td><td>1 </td><td>0 </td><td>0 </td><td>1 </td><td>1 </td></tr>
<tr><td>1 </td><td>1 </td><td>0 </td><td>1 </td><td>1 </td><td>1 </td><td>0 </td><td>0 </td><td>0 </td></tr>
</tbody></table>
<p><br>
We will also lump the NOT-A and NOT-B together and create the single
task NOT, which will identify either of them in Avida.  Of course, for
the purpose of determining what other tasks can be built off of these,
we will consider both separately.
</p><p>To continue this process, we take our current state (and nand
everything together again.)  Anything new we get here will be function
that cannot be performed using fewer than two nands.
</p>
<table border="1">
<tbody><tr><th>NAND COMBOS </th><th>Input A    </th><th>Input B    </th><th>NOT-A      </th><th>NOT-B      </th><th>A-NAND-B
</th></tr><tr><th>Input A     </th><td>NOT-A      </td><td>A-NAND-B   </td><td>ALL-ONES   </td><td>B-OR-NOT-A </td><td>B-OR-NOT-A
</td></tr><tr><th>Input B     </th><td>B-NAND-A   </td><td>NOT-B      </td><td>A-OR-NOT-B </td><td>ALL-ONES   </td><td>A-OR-NOT-B
</td></tr><tr><th>NOT-A       </th><td>ALL-ONES   </td><td>A-OR-NOT-B </td><td>ECHO-A     </td><td>A-OR-B     </td><td>ECHO-A
</td></tr><tr><th>NOT-B       </th><td>B-OR-NOT-A </td><td>ALL-ONES   </td><td>A-OR-B     </td><td>ECHO-B     </td><td>ECHO-B
</td></tr><tr><th>A-NAND-B    </th><td>B-OR-NOT-A </td><td>A-OR-NOT-B </td><td>ECHO-A     </td><td>ECHO-B     </td><td>A-AND-B
</td></tr></tbody></table>
<p><br>
Here it looks like we've found four new functions: A-OR-NOT-B,
B-OR-NOT-A, A-OR-B and A-AND-B.  But how many nands do they each
require?  Clearly the first two are a 1-nand function nanded with a
0-nand function, thus they require 2 nands each.  The A-OR-B is
clear-cut in the other direction.  To get this function you must nand
NOT-A to NOT-B.  Each of these already cost 1 nand to build.  Add to
that the additional nand of combining them and you realize the A-OR-B
costs 3-nands.
</p><p>The same logic can almost be used for A-AND-B until we realize
that both inputs are the same function.  As such, we would only need one
nand to construct it, and one more to nand it to itself, for a total of
two nands.
</p><p>When converting these to tasks in Avida, we note the symmertry
between A-OR-NOT-B and B-OR-NOT-A and create a single "or not" task
called ORN.
</p><p>We have now found 11 of the 16 possible operations.  The last 5
will arise by repeating this process.  For each of them we keep track of
the fewest nands we can build it with.
</p><p>The final five are: A-AND-NOT-B and B-AND-NOT-A (combined into ANDN) costing 3 nands, A-NOR-B , A-XOR-B, and A-EQU-B.
</p>
<table border="1">
<tbody><tr><th colspan="16">2-Input Logic Operations</th></tr>
<tr><th colspan="4">No-NAND Operations </th><th colspan="3">One-NAND operations </th><th colspan="3">Two-NAND operations </th><th colspan="3">Three-NAND operations </th><th colspan="2">Four-NAND operations </th><th>Five NAND op.
</th></tr>
<tr><th>Input A&nbsp; </th><th>Input B&nbsp; </th><th>ALL-ZERO&nbsp; </th><th>ALL-ONE&nbsp; </th><th>NOT-A&nbsp; </th><th>NOT-B&nbsp; </th><th>NAND&nbsp; </th><th>A-OR-NOT-B&nbsp; </th><th>B-OR-NOT-A </th><th>AND </th><th>A-AND-NOT-B </th><th>B-AND-NOT-A </th><th>OR </th><th>NOR </th><th>XOR </th><th>EQU
</th></tr>
<tr><td>0 </td><td>0 </td><td>0 </td><td>1 </td><td>1 </td><td>1 </td><td>1 </td><td>1 </td><td>1 </td><td>0 </td><td>0 </td><td>0 </td><td>0 </td><td>1 </td><td>0 </td><td>1</td></tr>
<tr><td>0 </td><td>1 </td><td>0 </td><td>1 </td><td>1 </td><td>0 </td><td>1 </td><td>0 </td><td>1 </td><td>0 </td><td>0 </td><td>1 </td><td>1 </td><td>0 </td><td>1 </td><td>0</td></tr>
<tr><td>1 </td><td>0 </td><td>0 </td><td>1 </td><td>0 </td><td>1 </td><td>1 </td><td>1 </td><td>0 </td><td>0 </td><td>1 </td><td>0 </td><td>1 </td><td>0 </td><td>1 </td><td>0</td></tr>
<tr><td>1 </td><td>1 </td><td>0 </td><td>1 </td><td>0 </td><td>0 </td><td>0 </td><td>1 </td><td>1 </td><td>1 </td><td>0 </td><td>0 </td><td>1 </td><td>0 </td><td>0 </td><td>1</td></tr>
</tbody></table>
<p><br>
This entire process can easily scale up to three-input or higher logic
functions, but by that point you'd probably want to automate the
process.  When you move to three inputs, you have 8 combinations of
inputs (2^3).  Each of these combinations comes out to a zero or one for
any specific logic function.  This means that there are 2^8 = 256
unique logic functions.  When we remove symmetries (given that inputs
can come in in any order), we only get 68 new logic operations out of
this.
</p>
