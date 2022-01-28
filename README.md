# Problem Solution: 
  Rotate Image
  
# Difficulty: 
  Medium
  
# Description:
  You are given an n x n 2D matrix representing an image, rotate the image by 90 degrees (clockwise).

  You have to rotate the image in-place, which means you have to modify the input 2D matrix directly. DO NOT allocate another 2D matrix and do the rotation.
  
  Example:
  Input: matrix = [[1,2,3],[4,5,6],[7,8,9]]
  Output: [[7,4,1],[8,5,2],[9,6,3]]
  
  For more details: https://leetcode.com/problems/rotate-image/
  
# Idea:
  We need a temporary matrix as a copy of the given matrix.
  Next, we transpose 'matrix' by using 'for' that go from the last to the first row (reversed rows order). 
      
# Code:
  Here is my completed function: 

    void rotate(vector<vector<int>>& matrix) {
        vector<vector<int>> temp = matrix;
        int len = matrix.size();
        int i2(0),j2;
        for(int i1=len-1;i1>=0;--i1){
            for(int j1=0;j1<len;++j1){
                j2 = j1;
                matrix[j2][i2] = temp[i1][j1];
            }
            i2++;
        }
    }
  
  


