1. [the boolean order](https://www.codewars.com/kata/59eb1e4a0863c7ff7e000008/train/java)
```java
import java.math.BigInteger;

public class BooleanOrder {
    private final String values;
    private final String ops;

    public BooleanOrder(String values, String ops) {
        this.values = values;
        this.ops = ops;
    }

    public BigInteger solve() {
        int n = values.length();
        BigInteger[][][] dp = new BigInteger[n][n][2];

        for (int i = 0; i < n; i++) {
            dp[i][i][0] = values.charAt(i) == 'f' ? BigInteger.ONE : BigInteger.ZERO;
            dp[i][i][1] = values.charAt(i) == 't' ? BigInteger.ONE : BigInteger.ZERO;
        }

        for (int len = 2; len <= n; len++) {
            for (int i = 0; i <= n - len; i++) {
                int j = i + len - 1;
                dp[i][j][0] = BigInteger.ZERO;
                dp[i][j][1] = BigInteger.ZERO;

                for (int k = i; k < j; k++) {
                    char op = ops.charAt(k);

                    for (int left = 0; left <= 1; left++) {
                        for (int right = 0; right <= 1; right++) {
                            int result = evaluate(left, right, op);
                            dp[i][j][result] = dp[i][j][result].add(
                                dp[i][k][left].multiply(dp[k + 1][j][right])
                            );
                        }
                    }
                }
            }
        }

        return dp[0][n - 1][1];
    }

    private int evaluate(int a, int b, char op) {
        switch (op) {
            case '&': return a & b;
            case '|': return a | b;
            case '^': return a ^ b;
            default: throw new IllegalArgumentException("Invalid operator: " + op);
        }
    }
}
```

