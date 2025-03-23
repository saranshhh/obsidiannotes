class Main {
    public static int MaxHourGlass(int arr[][], int R, int C) {
        if (R < 3 || C < 3) {
            System.out.println("Not possible");
            return 0;
        }
        int max_sum = Integer.MIN_VALUE;
        for (int i = 0; i < R - 2; i++) {
            for (int j = 0; j < C - 2; j++) {
                int sum = (arr[i][j] + arr[i][j + 1] + arr[i][j + 2] +arr[i + 1][j + 1] + arr[i + 2][j] + arr[i +2][j + 1] + arr[i + 2][j + 2]);
                max_sum = Math.max(max_sum, sum);
            }
        }
        return max_sum;
    }
    public static void main(String[] args) {
        int a1[][] = {{1, 2, 3, 0, 0}, {0, 0, 0, 0, 0}, {2, 1, 4, 0, 0}, {0, 0, 0, 0, 0}, {1, 1, 0, 1, 0}};
        int res = MaxHourGlass(a1, 5, 5);
        System.out.println(res);
    }
}