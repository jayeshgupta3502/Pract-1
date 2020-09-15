# Pract-1
My Ds Code

'''
Write a program to store the elements in 1-D array and provide an option to perform 
the operatons like searching, sorting, merge_eling, reversing the elements.
'''
class pract1D:
    def __init__(self, a):
        self.array = a

    def search(self, e):
        if e in self.array:
            return True
        return False

    def sort(self):
        for i in range(len(self.array)):
            lowest_index = i
            for j in range(i+1, len(self.array)):
                if self.array[j] < self.array[lowest_index]:
                    lowest_index = j
            self.array[i], self.array[lowest_index] = self.array[lowest_index], self.array[i]
        return self.array

    def merge_el(self,l):
        self.array = self.array + l
        return self.array

    def reverse(self):
        return self.array[::-1]

a = [5,6,7,89,2,5,6,1]
o = pract1D(a)
print(o.sort())
print(o.search(89))
print(o.merge_el([8,5,7,9,3]))
print(o.reverse())
