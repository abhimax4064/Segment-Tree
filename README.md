# segmentTree

Some Points which can be useful while using this library

1. include segmentTree.cpp file

2. to construct a segment tree you need to specify the following:
   a. The datatype of array for which the tree is being constructed.
   b. an array or vector for which the tree is to be constructed.
   c. a value that can be used to fill the extra nodes of the tree.
   d. a function combine that specifies how the result of left and right child of a node
   should be used to generate the value of current node.

3. Example usage:
   int small(int x,int y){return min(x,y);}
   SegmentTree < int > rangeMinQueries(dataVector,INT_MAX,small);

   int sum(int x,int y){return x+y;}
   SegmentTree < int > rangeSumQueries(dataVector,0,sum);

   long long product(long long x,long long y){return x*y;}
   SegmentTree < long long > rangeProductQueries(dataVector,1,product);
