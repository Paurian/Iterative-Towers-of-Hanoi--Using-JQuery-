Iterative Towers of Hanoi

This is a JQuery implementation of an iteratively coded Towers of Hanoi using my own algorithm.

Why:
We used a VAX mainframe system at our university that restricted students' memory allocation, making it impossible to code this recursively beyond five discs before we ran out of stack space. Although the professor excused this shortfall and just graded on our printed code, I wanted to take it further and make this program perform an arbitrary number of rings greater than five (typically seven) and do it faster and cleaner than my classmates.

What (Solution):
The answer came to me after examining patterns of motion between moves and rethinking the problem as movement rather than state. In other words, instead of looking at the problem as a series of rods (or stacks) that are in a static line, I thought of the problem as a lazy-susan of rods that can spin around (I actually thought of it as a cylinder with three chambers which is why the code uses the term "Cylinder"). The result is a simple algorithm that rotates the rods (or stacks of rings) clockwise and compares the state of the previous rod with that of the current to determine where to move the ring.

How it works:
Each move starts with rotating the cylinder (or lazy-susan if you prefer) clockwise. This positions the rod that was previously to the right as the current rod. On odd-number moves (and we consider the very first move to be an odd-number) we always move from the current rod to the last rod. On even-number moves we check for empty poles and where the largest ring sits such that if the current stack is empty or the top ring on our current stack is larger than that of the last stack, we change direction and move from the last rod to the current one.
