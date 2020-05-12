# MAR_coding

We define a magic square to be an n x n matrix of distinct positive integers from 1 to n^2 where the sum of any row, column, or diagonal of length n is always equal to the same number: the magic constant.

You will be given a 3 x 3 matrix s of integers in the inclusive range [1,9] . We can convert any digit a to any other digit b in the range [1,9] at cost of |a - b|. Given s, convert it into a magic square at minimal cost. Print this cost on a new line.

Note: The resulting magic square must contain distinct integers in the inclusive range [1,9].

For example, we start with the following matrix s:

5 3 4 <br>
1 5 8 <br>
6 4 2

We can convert it to the following magic square:

8 3 4 <br>
1 5 9 <br>
6 7 2 <br>
This took three replacements at a cost of |5 - 8| + |8 - 9| + |4 - 7| = 7.

Function Description

Complete the formingMagicSquare function in the editor below. It should return an integer that represents the minimal total cost of converting the input square to a magic square.

formingMagicSquare has the following parameter(s):

s: a 3 x 3 array of integers

Input Format

Each of the lines contains three space-separated integers of row s[i].

Constraints

s[i][j] belongs to [1,9]

Output Format

Print an integer denoting the minimum cost of turning matrix s into a magic square.

Sample Input 0

4 9 2 <br>
3 5 7 <br>
8 1 5 <br>

Sample Output 0

1

Explanation 0

If we change the bottom right value, s[2][2], from 5 to 6 at a cost of |6 - 5| = 1, s becomes a magic square at the minimum possible cost.

Sample Input 1

4 8 2 <br>
4 5 7 <br>
6 1 6 <br>

Sample Output 1

4

Explanation 1

Using 0-based indexing, if we make

s[0][1]->9 at a cost of |9 - 8| = 1 <br>
s[1][0]->3 at a cost of |3 - 4| = 1 <br>
s[2][0]->8 at a cost of |8 - 6| = 2 <br>
then the total cost will be 1 + 1 + 2 = 4.
