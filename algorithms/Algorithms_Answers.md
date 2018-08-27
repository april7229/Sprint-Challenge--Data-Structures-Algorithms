Add your answers to the Algorithms exercises here.
 
 
 A.a = 0; while(a < n *n*n) a = a + n * n;
  O(n)

 b. inut arrays is of length n i = array.length -1; while (arry[i] > x && i >= 0) i = i/2;
 O(log n)

c. sum = 0; for (i = 0; i < Math.sqrt(n))/ 2; i++) for (j = i; j < 8 + i; j++) for (k = j; k < 8 + j; k++)sum++;
O(n^2)

D.sum = 0; for (i = 1; i < n; i *= 2) for (j = 0; j < n; j++) sum++;
O(n^2)

E.e) sum = 0; for (i = 0; i < n; i++) for (j = i + 1; j < n; j++) for (k = j + 1; k < n; k++) for (l = k + 1; l < 10 + k; l++) sum++;
O(N^2)

F.bunnyEars = function (bunnies) { // here bunnies === n if (bunnies === 0) return 0; return 2 + bunnyEars(bunnies-1); 
O(N)

g.search = function (array, arraySize, target) { // here arraySize === n if (arraySize > 0) { if (array[arraySize-1] === target) return true; else return search(array, arraySize-1, target); } return false; }
 O(N)


EXCERCISE II.
a) Given an array of n numbers, design a linear running time algorithm to find the maximum value of a[j] - a[i], where j ≥ i.

Sean Solve: function maxDiff(arr) { let min = arr[0]; let maxDiff = 0;

arr.forEach(val => { min = Math.min(min, val); maxDiff = Math.max(maxDiff, val - min); });

return maxDiff; }

B. 
b) Suppose that you have an n-story building and plenty of eggs. Suppose also that an egg is broken if itis thrown off floor f or higher, and unbroken otherwise. Devise a strategy to determine the value of f such that the number of dropped eggs is minimized.

Answer: Use binary sectioning. Start at f' = n/2. If egg breaks, set f' = f'/2. If egg does not break, set f' = 3f'/2
def egg_drop(n):
   ''' Find the highest floor in a building that an egg can drop from without breaking '''
   t = [1,11]
   while t[0] < 100:
       if t[1] >= n:
           print 'break_an_egg on floor %d' % t[1]
           for i in range(t[0],t[1]):
               if i >= n:
                   print  'break_an_egg on floor %d' % i
                   return i - 1
       else:
           t[0] += 10
           t[1] += 10
   return 100

EXERCISE III.
A.
Below is the the pseudo-code for the Quicksort algorithm:

function quicksort(array) if length(array) <= 1 return array select and remove a pivot element pivot from array create empty lists less and greater for each x in array if x <= pivot then append x to less else append x to greater return concatenate(quicksort(less), list(pivot), quicksort(greater))

a) Suppose we implement quicksort so that the pivot is always chosen to be the first element of the array. What is the running time of this algorithm on an input array that is already sorted? Why?

ANSWER: For sorting it would be O(n^2)
b) Suppose we implement quicksort so that the pivot is always magically chosen to be the median element of the array. What is the running time of this algorithm? Why?

ANSWER: O(n log n)
