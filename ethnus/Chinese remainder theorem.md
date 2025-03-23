```
ublic class ChineseRemainderTheorem {
    public static int findX(int[] y, int[] m, int k) {
        int M = 1, X = 0;
        int[] Mi = new int[k];
        int[] Z = new int[k];

        // Calculate M
        for (int i = 0; i < k; i++) {
            M *= m[i];
        }

        // Calculate Mi
        for (int i = 0; i < k; i++) {
            Mi[i] = M / m[i];
        }

        // Calculate Z[i]
        for (int i = 0; i < k; i++) {
            int z = 0;
            while ((z * Mi[i]) % m[i] != 1) {
                z++;
            }
            Z[i] = z;
        }

        // Calculate X
        for (int i = 0; i < k; i++) {
            X = (X + (y[i] * Z[i] * Mi[i])) % M;
        }

        return X;
    }

    public static void main(String[] args) {
        int[] y = {1, 1, 3};
        int[] m = {5, 7, 11};
        int k = y.length;
        int X = findX(y, m, k);
        System.out.println("The answer using CRT is: " + X);
    }
}
	``` 

public class Main {
    static int modInverse(int a, int m){
        a = a%m;
        for (int x =1; x<m;x++){
            if ((a*x)%m ==1)
                return x;
        }
        return 1;
    }
    
    static int findMinX(int num[], int rem[], int k){
        int prod = 1;
        for (int i=0; i<k; i++)
            prod = num[i]
    }
    public static void main(String[] args) {
        int[] y = {1, 1, 3};
        int[] m = {5, 7, 11};
        int k = y.length;
        int X = findX(y, m, k);
        System.out.println("The answer using CRT is: " + X);
    }
}