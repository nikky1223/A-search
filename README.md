# A*  search
#using python

#heuristics for searching 
h={'Arad':366,'Bucharest':0,'Craiova':160,'Dobreta':242,'Eforie':161,'Fagaras':176,'Giurgiu':77,'Hirsowa':151,'Lasi':226,'Lugoj':244,'Mehadia':241,'Neamt':234,'Oradea':380,'Pitesti':100,'Rimnicu Vilcea':193,'Sibiu':253,'Timisoara':329,'Urziceni':80,'Vaslui':199,'Zerind':374}



pathcost from start to destination 
p1=['Arad','Arad','Arad','Zerind','Oradea','Timisoara','Sibiu','Sibiu','Lugoj','Fagaras','Rimnicu Vilcea','Rimnicu Vilcea','Mehadia','Bucharest','Bucharest','Bucharest','Pitesti','Craiova','Urziceni','Urziceni','Hirsova','Vaslui','Lasi']
p2=['Zerind','Sibiu','Timisoara','Oradea','Sibiu','Lugoj','Fagaras','Rimnicu Vilcea','Mehadia','Bucharest','Pitesti','Craiova','Dobreta','Pitesti','Urziceni','Giurgiu','Craiova','Dobreta','Hirsova','Vaslui','Eforie','Lasi','Neamt']
p3=[75,140,118,71,151,111,99,80,70,211,97,146,75,101,85,90,138,120,98,142,86,92,87]

#function for searching in a map
def A(start,stop):
    if start==stop:
        return
    else:
        s1=[]
        s2=[]
        for j in range(len(p1)):
            if start==p1[j]:
                s1.append(j)
        for i in s1:
            s2.append(p3[i]+h[p2[i]])
        print(start)
        print('->')
        A(p2[s1[s2.index(min(s2))]],stop)
A(starting point,ending point)
print('Rimnicu Vilcea')
