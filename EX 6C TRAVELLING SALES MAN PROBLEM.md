# EX 6C TRAVELLING SALES MAN PROBLEM
## DATE:
## AIM:
To Solve Travelling Sales man Problem for the following graph.

![image](https://github.com/user-attachments/assets/653921a4-3d7b-4691-9b41-735e80f7af0b)



## Algorithm
1. Initialize a list of all cities except the starting city s.
2. Generate all possible permutations of the remaining cities.
3. For each permutation:
        Set total path cost to 0.
        Starting from city s, add the cost to the next city in the permutation.
        After visiting all cities, return to the starting city and add that cost.
4.Track the minimum of all such path costs. 
5. Return the minimum cost found.  

## Program:
```
/*
To implement the program for TSP.


Developed by: Vignesh M
Register Number: 212223240176
*/
```
```
from sys import maxsize
from itertools import permutations
V = 4
 

def travellingSalesmanProblem(graph, s):
    ##Write your code
    vertex = [] 
    for i in range(V): 
        if i != s: 
            vertex.append(i) 
    min_path = maxsize 
    next_permutation=permutations(vertex)
    for i in next_permutation:

        current_pathweight = 0
        k = s 
        for j in i: 
            current_pathweight += graph[k][j] 
            k = j 
        current_pathweight += graph[k][s] 
        min_path = min(min_path, current_pathweight) 
         
    return min_path
   
 
 

if __name__ == "__main__":
    graph = [[0, 10, 15, 20], [10, 0, 35, 25],
            [15, 35, 0, 30], [20, 25, 30, 0]]
    s = 0
    print(travellingSalesmanProblem(graph, s))
```
## Output:

![image](https://github.com/user-attachments/assets/c525a13f-ed89-4e68-afbb-722cc7b70766)


## Result:
Thus the program was executed successfully for finding the minimum cost to vist all cities.
