## Knapsac
## Permutation
## Combination
## Subset Sum Problem
```java
// Returns true if there is a subset of set[] with sun equal to given sum
bool isSubsetSum(int set[], int n, int sum)
{
   // Base Cases
   if (sum == 0)
     return true;
   if (n == 0 && sum != 0)
     return false;
 
   // If last element is greater than sum, then ignore it
   if (set[n-1] > sum)
     return isSubsetSum(set, n-1, sum);
 
   /* else, check if sum can be obtained by any of the following
      (a) including the last element
      (b) excluding the last element   */
   return isSubsetSum(set, n-1, sum) || 
                        isSubsetSum(set, n-1, sum-set[n-1])
```
## Longest Paradromic Sequence
## Longest subsequent array with maximum sum
## Longest Common Subsequence
## Longest increasing Subsequence
## Job scheduling Problem
