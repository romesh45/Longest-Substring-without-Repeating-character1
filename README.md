# Longest-Substring-without-Repeating-character1



class Solution {
    public int lengthOfLongestSubstring(String s) {
        int n=s.length();
        int res=0;
        for(int i=0;i<n;i++)
        {
            boolean[] visited=new boolean[256];
            for(int j=i;j<n;j++)
            {
                if(visited[s.charAt(j)])
                {
                    break;
                }
                else
                {
                    res=Math.max(res,j-i+1);
                    visited[s.charAt(j)]=true;
                }
            }
        }
        return res;   
    }
}
