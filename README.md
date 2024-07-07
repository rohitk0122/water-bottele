# water-bottele
class Solution {
    public int numWaterBottles(int numBottles, int numExchange) {
        int totalDrinks = numBottles;
        int emptyBottles = numBottles;

        while (emptyBottles >= numExchange) {
            int newBottles = emptyBottles / numExchange;
            totalDrinks += newBottles;
            emptyBottles = emptyBottles % numExchange + newBottles;
        }

        return totalDrinks;
    }

    public static void main(String[] args) {
        Solution solution = new Solution();
        System.out.println(solution.numWaterBottles(9, 3)); // Output: 13
        System.out.println(solution.numWaterBottles(15, 4)); // Output: 19
        System.out.println(solution.numWaterBottles(5, 5)); // Output: 6
        System.out.println(solution.numWaterBottles(2, 3)); // Output: 2
    }
}
