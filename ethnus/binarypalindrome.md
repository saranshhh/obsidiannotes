class Main {
    public static boolean isBinaryPalindrome(int n) {
        if (n < 0) {
            return false; 
        }

        
        String binaryString = Integer.toBinaryString(n);
        int left = 0;
        int right = binaryString.length() - 1;

        while (left < right) {
            if (binaryString.charAt(left) != binaryString.charAt(right)) {
                return false; 
            }
            left++;
            right--;
        }
        return true; 
    }
    
}