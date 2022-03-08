# Challenges

0. Write a program/pseudocode called isBalanced that takes in a String containing parentheses, square brackets, and curly braces.  The function should return True if the String is **balanced**. For the purposes of this program the definition of balanced if all of the brackets are well-formed.
E.g., ` [()]{}{[()()]()}` is balanced but `[(])` is not

1. What does this fragment do to a queue q?
```
s = new Stack();
while(!q.isEmpty())
   s.push(q.dequeue());
while(!s.isEmpty())
   q.enqueue(s.pop());
```

2. Consider a standard arithmetic expression with `+, -, *,  /, (, )`. The standard way of writing arithmetic expressions is called **infix** notation because the **operator** (e.g., `+`) is in-between its **operands** (e.g., in `2 + 3`, `2` and `3` are **operands**).

An alternative to **infix** notation is **postfix** notation where the **operator** comes *after* the **operands**. 

Examples:
* `2 + 3 * 4` converted to **postfix** notation is `2 3 4 * +`
* `(2 + 3) * 4` converted to **postfix** notation is `2 3 + 4 *`

Write a program to evaluate a **postfix** expression.


3. See 2. Write a program to convert an infix expression to postfix notation.

