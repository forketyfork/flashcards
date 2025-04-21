START
Basic
Front: How do "and" and "or" functions work?
Back: 
- These functions go through their arguments and evaluate them.
- Once "and" evaluates an argument to an empty or false value, it stops and returns this value, otherwise, it returns the last value.
- Once "or" evaluates an argument to a non-empty or true value, it stops and returns this value, otherwise, it returns the last value.
- Before Go 1.18, those functions were not short-circuit, and they evaluated all their arguments. Starting from 1.18, they are short-circuit.
END
