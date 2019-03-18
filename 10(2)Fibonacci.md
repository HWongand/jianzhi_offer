//我的
class Solution {
public:
    int jumpFloor(int number) {
        int frist=0,second=1,temp;
        if (number<=2)
            return number;
        else
        {
             for (int i=2; i<=number+1; i++)
            {
                temp=frist+second;
                frist=second;
                second=temp;
            }
        }
        return temp;
    }
};

//牛客网
class Solution {
public:
    int jumpFloor(int number) {
         int result[2] = {0, 1};
    if(number < 2)
        return result[number];
 
    long long  fibNMinusOne = 1;
    long long  fibNMinusTwo = 0;
    long long  fibN = 0;
    for(unsigned int i = 1; i <= number; ++ i)
    {
        fibN = fibNMinusOne + fibNMinusTwo;
 
        fibNMinusTwo = fibNMinusOne;
        fibNMinusOne = fibN;
    }
 
     return fibN;
         
    }
};
