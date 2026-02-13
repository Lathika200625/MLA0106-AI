Breath First Search(BFS):-
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

DEPTH FIRST SEARCH(DFS):-
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

UNIFORM COST SEARCH(UCS):-
UCS(Graph, Start, Goal):

    create priority queue PQ
    create cost table

    cost(Start) = 0
    insert Start into PQ

    while PQ not empty:

        Current = extract node with minimum cost

        if Current == Goal:
            stop

        for each neighbor N of Current:

            tempCost = cost(Current) + edgeCost(Current, N)

            if N not visited OR tempCost < cost(N):
                cost(N) = tempCost
                parent(N) = Current
                insert N into PQ


