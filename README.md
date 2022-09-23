# parallel-processing-hackerrank-certification-solution
#only logic
 x = []
    y = []
    for f in files:
        if f % numCores == 0:
            x.append(f)
        else:
            y.append(f)
    x.sort(reverse=True)
    return (sum(x[:limit]) // numCores) + sum(x[limit:]) + sum(y)
