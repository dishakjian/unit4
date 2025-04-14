# Trace Table

| Step | INT | R (INT % 10) | DATA              | INDEX | INT = INT // B |
|------|---------|------------------|-------------------|--------|-------------------------|
| Init | 4520    | -                | [0, 0, 0, 0]       | 0      | -                       |
| 1    | 4520    | 0                | [0, 0, 0, 0]       | 1      | 452                     |
| 2    | 452     | 2                | [0, 2, 0, 0]       | 2      | 45                      |
| 3    | 45      | 5                | [0, 2, 5, 0]       | 3      | 4                       |
| 4    | 4       | 4                | [0, 2, 5, 4]       | 4      | 0                       |

# Paper Solution
![image](https://github.com/user-attachments/assets/b5353cfc-a0aa-4f5a-b61a-c181e5dbafc0)
