#include <vector>
class Solution {
public:
    int removeDuplicates(vector<int>& nums) 
        
{
        
    if (nums.empty()) return 0;

    int unique_pos = 0;

    for (int i = 1; i < nums.size(); i++)
    {
        
        if (nums[i] != nums[unique_pos])
        
        {
            unique_pos++;
            
            nums[unique_pos] = nums[i]; 
        }
    }

    return unique_pos + 1;
}

};
