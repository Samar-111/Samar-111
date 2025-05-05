- 👋 Hi, I’m @Samar-111
- this one is the solution of the happy numbers leetcode problems
- 
    #include <unordered_set>

class Solution {
public:
  
  int sumOfSquares(int n) {
        int sum = 0;
        while (n > 0) {
            int digit = n % 10;
            sum += digit * digit;
            n /= 10;
        }
        return sum;
    }

  bool isHappy(int n) {
        std::unordered_set<int> seen;

   while (n != 1 && seen.find(n) == seen.end()) {
            seen.insert(n);
            n = sumOfSquares(n);
        }

   return n == 1;
    }
};
Samar-111/Samar-111 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
