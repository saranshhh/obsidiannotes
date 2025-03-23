import java.util.HashMap;
import java.util.Map;

public class Main {

    public static boolean isStrobogrammatic(String num) {
        if (num == null || num.isEmpty()) {
            return true; 
        }

        Map<Character, Character> map = new HashMap<>();
        map.put('0', '0');
        map.put('1', '1');
        map.put('6', '9');
        map.put('8', '8');
        map.put('9', '6');

        int left = 0;
        int right = num.length() - 1;

        while (left <= right) {
            char leftChar = num.charAt(left);
            char rightChar = num.charAt(right);

            if (!map.containsKey(leftChar) || !map.containsKey(rightChar) || map.get(leftChar) != rightChar) {
                return false;
            }

            left++;
            right--;
        }

        return true;
    }


    public static void main(String[] args) {
        String[] testCases = {"69", "88", "96", "1", "0", "101","689", "", "11111","999666","4"};

        for (String num : testCases) {
            System.out.println(num + " is strobogrammatic: " + isStrobogrammatic(num));
        }
    }
}