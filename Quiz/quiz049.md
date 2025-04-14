# Trace Table

| Step           | D     | Z   | B      | (Z < L) | Action                                |
| 1           | 46    | 1   | false  | true              | Initialize variables                   |
| 2 | 15    | 2   | true   | true              | D = 46 div 3, Z = 2, B = NOT false     |
| 3 | 5     | 3   | false  | false             | D = 15 div 3, Z = 3, B = NOT true      |
| 4     | 5     | 3   | false  | -                 | Exit loop (Z = 3 is not < L)           |
| 5   | 5 ≠ 0 and B = false | - | - | false             | Condition is false → go to else       |
| 6         | -     | 3   | true   | -                 | Output(Z, NOT B) → `output(3, true)`   |

# Paper Solution
![image](https://github.com/user-attachments/assets/b0c37557-d51a-49d1-9cc2-142092341305)
