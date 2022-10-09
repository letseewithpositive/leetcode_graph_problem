# leetcode_graph_problem
Solution of Problem 732
class MyCalendarThree {
public:
    map<int,int> mp;
    
    MyCalendarThree() {
        
    }
    
    int book(int start, int end) {
        mp[start]++;
        mp[end]--;
        int ans=0,cur=0;
        auto it=mp.begin();
        while(it!=mp.end()){
            cur+=it->second;
            ans=max(ans,cur);
            it++;
        }
        return ans;
    }
};

/**
 * Your MyCalendarThree object will be instantiated and called as such:
 * MyCalendarThree* obj = new MyCalendarThree();
 * int param_1 = obj->book(start,end);
 */
