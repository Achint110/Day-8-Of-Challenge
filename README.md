https://leetcode.com/problems/intersection-of-two-arrays/description/?envType=daily-question&envId=2024-03-10

class Solution {
public:
    vector<int> intersection(vector<int>& nums1, vector<int>& nums2) {
        sort(nums1.begin(),nums1.end());
        sort(nums2.begin(),nums2.end());
int i=0,j=0;
vector<int>V;
set<int>a;
 while(i<nums1.size() && j<nums2.size()){
      
      if(nums1[i]<nums2[j])
      i++;

      else if (nums1[i]>nums2[j])
j++;
else{
a.insert(nums1[i]);
i++;
j++;
}

 }
 for(auto i :a){
    V.push_back(i);
}
return V;
    }
};
