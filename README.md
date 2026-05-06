TASK-1:
public class HarshadChecker {
    public static boolean isHarshad(int n) {
        if (n <= 0) return false;
        int original = n;
        int sum = 0;
        while (n > 0) {
            sum += n % 10;
            n /= 10;
        }
        return (original % sum == 0);
    }

    public static void main(String[] args) {
        int num = 18;
        System.out.println(isHarshad(num));
    }
}


TASK-2:
class Solution {
    public int sumOfTheDigitsOfHarshadNumber(int n) {
        int sum = 0;
        int temp = n;
        
        while (n > 0) {
            int r = n % 10;
            sum = sum + r;
            n = n / 10;
        }

        if(sum == 0){
            return -1;
        }

        if(temp % sum == 0){
        return sum;
        }

        return -1;
    }
}
