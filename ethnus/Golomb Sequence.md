public class Main {
    public static int gol(int n) {
        if (n == 0) {
            return 0; 
        }
        if (n == 1) {
            return 1;
        }
        return 1 + gol(n - gol(gol(n - 1)));
    }
    public static void printGol(int n) {
        for (int i = 1; i <= n; i++) { 
            System.out.print(gol(i)+" ");
        }
    }
    public static void main(String[] args) {
        printGol(100);
    }
}