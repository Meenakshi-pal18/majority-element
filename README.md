# majority-element
class Solution {
public:
    int majorityElement(vector<int>& nums) {
        map<int,int>v;
        int freq=0;
        int ans;
        int n=nums.size();
        for (auto x:nums){
            v[x]++;
        }
        for(auto it:v){
        if(it.second>freq){
            freq=it.second;
            ans=it.first;
        }
        }
        return ans;
    }
};
