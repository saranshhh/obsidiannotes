public  class Main {
    public static int findEquilibriumIndex(int[] arr) {
        if (arr == null || arr.length == 0) {
            return -1;
        }
        
        
        // int[] ls = [];
        // int[] rs = [];
        // ls[0] = arr[0];
        
        // for (int i=1; i<arr.length; i++){
        //     ls[i] = ls[i-1] +arr[i];
        // }
        // rs[-1] = arr[-1];
        // for (int i=arr.length-2; i>=0; i--){
        //     rs[i] = rs[i+1]+arr[i];
        // }
        int totalSum = 0;
        for (int num : arr) {
            totalSum += num;
        }
        int leftSum = 0;
        for (int i = 0; i < arr.length; i++) {
            int rightSum = totalSum - leftSum -arr[i]

            if (leftSum == rightSum) {
                return i;
            }

            leftSum += arr[i];
        }

        return -1;
    }
    public static void main(String[] args) {
        int[] arr1 = {1,2,3,9,5,1};
        int eq1 = findEquilibriumIndex(arr1);
        System.out.println(eq1);
    }
}
