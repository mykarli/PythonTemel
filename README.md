# PythonTemel
Ödev

# Online Python - IDE, Editor, Compiler, Interpreter
"""
1- Bir listeyi düzleştiren (flatten) fonksiyon yazın. Elemanları birden çok katmanlı listelerden ([[3],2] gibi) oluşabileceği gibi, non-scalar verilerden de oluşabilir. Örnek olarak:
"""
inp1 = [[1,'a',['cat'],2],[[[3]],'dog'],4,5]

def makeListsFlatten(paramList):
    if isinstance(paramList, list):
        return [a for i in paramList for a in makeListsFlatten(i)]
    else:
        return [paramList]

"""
2- Verilen listenin içindeki elemanları tersine döndüren bir fonksiyon yazın. Eğer listenin içindeki elemanlar da liste içeriyorsa onların elemanlarını da tersine döndürün. Örnek olarak:
"""
inp2 = [[1, 2], [3, 4], [5, 6, 7]]

def makeReverseListOfLists(paramList):
    inp2Reverse = [[x for x in y[::-1]] for y in paramList[::-1]]
    return inp2Reverse


print(makeListsFlatten(inp1))

print(makeReverseListOfLists(inp2))
