class Main {
    int phi(int n) {
        int res = 1; 
        for (int i = 2; i <= n; i++) {
            if (gcd(i, n) == 1) {
                res++;
            }
        }
        return res; 
    }
    int gcd(int a, int b) {
        if (a == 0) {
            return b;
        }
        return gcd(b % a, a);
    }
    public static void main(String[] args) {
        Main m = new Main(); 
        int result = m.phi(6); 
        System.out.println(result);
    }
}