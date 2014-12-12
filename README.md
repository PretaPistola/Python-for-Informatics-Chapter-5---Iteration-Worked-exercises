Python-for-Informatics-Chapter-5---Iteration-Worked-exercises
=============================================================

A place to store problem sets, worked exercises and lessons learned for this chapter

Exercise 5.2 

Solution 1:

largest_so_far = None
smallest_so_far = None

while True:
    num_input = raw_input("Enter a number: ")
    if num_input == "done" : break
    
    else:
        try:
            num = int(num_input)
            if largest_so_far is None or num > largest_so_far:
                largest_so_far = num
                
            if smallest_so_far is None or num < smallest_so_far:
                smallest_so_far = num
                       
        except:
            print "Invalid input"
            
print "Maximum is", largest_so_far
print "Minimum is", smallest_so_far

Solution 2

def max(values):
    largest = None
    for value in values:
        if largest is None or value > largest:
           largest = value
    return largest

def min(values):
    smallest = None
    for value in values:
        if smallest is None or value < smallest:
           smallest = value
    return smallest


numlist= []

           
while True:
    num_input = raw_input("Enter a number: ")
    if num_input == "done" : break
    else:
        try:
            num = int(num_input)
            numlist.append(num)
            continue
            #list = (add the current num as the next value in the list)
           
            #each list item = current value for num, position == new_list_item
        except:
            print "Invalid input"
            continue

largest = max(numlist)
smallest = min(numlist)

print "Maximum is", largest
print "Minimum is", smallest
