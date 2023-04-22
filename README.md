# longest-dist-char
int longestSubstrDistinctChars (string S)
{
    // your code here
    unordered_set<char>st;
   
    int maxlen=0;
    int i=0;
     for(int j=0;j<S.size();j++){
        while(st.find(S[j])!=st.end())
        {
            st.erase(S[i]);
            i++;
        }
        st.insert(S[j]);
        maxlen=max(maxlen,(int)st.size());
     }
     return maxlen;
}
