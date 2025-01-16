#txt="rai"
#print(txt)

fruits = ["apple","banana"]
fruits.append("orange")
fruits.remove("apple")
fruits.insert(1, "melon")
for fruit in fruits:
    print(f"This is a {fruits}.")











#########Dictionar  in Mobile robon
   #      A
   #     / \
   #     B  C
   #    / \  \
   #   D   E  F
    graph = {
    'A': ['B', 'C'],
    'B': ['D', 'E'],
    'C': ['F'],
    'D': [],
    'E': [],
    'F': []
}

start = 'A'
goal = 'C'
frontier = [start]
explored = set()#  Use set for unique (ignore duplicate appen)

print(frontier, explored)
while len(frontier) > 0:
    curret = frontier.pop() # Remove and put into varaible
    print(curret)

    if curret == goal:
        print("Goal reach")
        break
    print(f"neighbor of {curret} is {graph[curret]}")
    for neighbor in  graph[curret]: 
        frontier.append(neighbor)
