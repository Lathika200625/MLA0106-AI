Breath First Search:-
BFS(Graph, S):
    create empty queue Q
    mark S as visited
    enqueue S into Q

    while Q is not empty:
        V = dequeue Q
        print V

        for each neighbor U of V:
            if U not visited:
                mark U as visited
                enqueue U into Q

DEPTH FIRST SEARCH:-
DFS(Graph):

    for each vertex V in Graph:
        mark V as not visited

    for each vertex V in Graph:
        if V is not visited:
            DFS_Visit(V)


DFS_Visit(V):

    mark V as visited
    print V

    for each neighbor U of V:
        if U is not visited:
            DFS_Visit(U)
