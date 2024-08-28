class Solution {
public:
    void sortColors(vector<int>& nums) {
        int n=nums.size();
        // int r=0;
        // int w=0;
        // int b=0;
        // for(int i=0;i<n;i++){
        //     if(nums[i]==0)
        //     r++;
        //     else if(nums[i]==1)
        //     w++;
        //     else
        //     b++;
        // }
        // int i=0;
        // while(r>0){
        //   nums[i++]= 0;
        //     r--;
        // }
        //    while(w>0){
        //    nums[i++]= 1;
        //     w--;
        // }
        //    while(b>0){
        //  nums[i++]= 2;
        //     b--;
        // }
        // return;
        int l=0;
        int m=0;
        int h=n-1;
        while(m<=h){
            if(nums[m]==0){
                swap(nums[m],nums[l]);
                l++;
                m++;
            }
            else if(nums[m]==1){
                m++;
            }
            else{
                swap(nums[m],nums[h]);
                h--;
            }
        }
        return;
    }
};
