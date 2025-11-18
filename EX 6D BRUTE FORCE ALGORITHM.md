# EX 6D BRUTE FORCE ALGORITHM
## DATE:
## AIM:
To write a python program using brute force method of searching for the given substring in the main string.




## Algorithm
1. Take two input strings: the main string and the substring to search.
2. Determine the lengths of both strings.
3. Loop from index 0 to len(main) - len(substring):
      At each index, extract a substring of the same length as sub.
      Compare it with the target sub.
      If they match, print the starting index.
   

## Program:
```
/*
To implement the program using brute force method of searching for the given substring in the main string.


Developed by: Vignesh M
Register Number: 212223240176
*/
```
```
def match(string,sub):
    l = len(string)
    ls = len(sub)
    start = sub[0]
    for i in range(l-ls+1):
        if string[i:i+ls]==sub:
            print(f"Found at index {i}")

str1=input()
str2=input()
```
## Output:

![image](https://github.com/user-attachments/assets/cff954c4-4f32-4345-8d84-45ea00afe04e)


## Result:
Thus the above program was executed successfully for searching the substring at respective index.
