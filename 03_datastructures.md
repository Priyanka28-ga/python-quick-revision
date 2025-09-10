# TWO TYPES OF DATA SCTRCUTURES
- built in -> int float str bool
- sequential -> set list tuples dictionaries

# DEFINING THESE STRUCTURES
 - defining list - can hold multiple vlues in a single variable. can store values of different datatpes 
    L=[1,3,4.9,"name",3] 
- defining tuple - by default to store multiple values in single varibale it consider tuple
    T=(1,3,4.9,"name",3)
- definig set
    S={1,3,4.9,"name",3}
- definig dictionary
    D={23:"twothree",'B':43,'C':'CCD'}

- List: Ordered, mutable, allows duplicates.

- Tuple: Ordered, immutable, allows duplicates.

- Set: Unordered, mutable, no duplicates.

- Dict: Key-value pairs, keys unique.

# ACCESSING THE VALUES
print(L[1]) -> 3
print(T[1]) -> 3 
print(3 in S) -> True
print(D[23]) -> twothree


//If you do print(S) you will get this -> {'name', 1, 3, 4.9} -> set writes duplicate only once and does not follow the order in which they are written

//All indexing in list and tuples goes as string ones

// appending a list - L=L+["how","are",6,"you"] or L.append(6.5)
// appending a set - S.update({23,"game",1})
// appending a dictionary - D['newkey']="newvalue"
//remving from set - S.remove('game')
//remving from dictionary - del D['C']

//if you do L4=L ->this l4 will also be point there only where l is. No new memory will be created for it. It just create a reference. Same for set and dictionary
//so if you update the L4 then L will also get updated
// If you want a new location so if we change l4 then l will not change
L4=L.copy()

# If you write help(L.append) or any other function then run it it will tell you about tah function in jupyter notebook

# To know more functions write L. and press tab# for set use S. and similary for other in jupter notebook

#  Data structures are abstract dictionary can contain lost set tuple and lly list can contain all of them.
//suppose you create list L = [1, 3, 'four point nine', 3, 'how', 'are', 6, 'you', 6.8]
//suppose you craete tuple T = (1, 3, 4.9, 'name', 3)
//suppose you create set S= {1, 23, 3, 4.9, 'name'}
//suppose you create dictionary D = {23: 'twothree', 'B': 43, 'newkey': 'newvalue'}
// now you csn create another dictionary such as D2={'A':L,'B':T,'C':S,'D':D}

  
