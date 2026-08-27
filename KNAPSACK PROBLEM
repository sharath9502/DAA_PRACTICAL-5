#include <iostream>
#include <vector>
#include <algorithm>
using namespace std;

// Function to solve the 0-1 Knapsack problem
int knapsack(int W, const vector<int>& weights,
             const vector<int>& values, int n) {

    // dp[w] stores the maximum value for capacity w
    vector<int> dp(W + 1, 0);

    // Process each item
    for (int i = 0; i < n; i++) {

        // Traverse capacity from right to left
        // to ensure each item is used only once
        for (int w = W; w >= weights[i]; w--) {
            dp[w] = max(dp[w],
                        dp[w - weights[i]] + values[i]);
        }
    }

    return dp[W];
}

int main() {

    // Values of the items
    vector<int> values = {10, 20, 25, 40, 60, 70};

    // Weights of the items
    vector<int> weights = {1, 2, 3, 6, 7, 4};

    // Maximum capacity of the knapsack
    int W = 7;

    // Number of items
    int n = values.size();

    // Find maximum value
    int max_value = knapsack(W, weights, values, n);

    // Display result
    cout << "Maximum value in Knapsack = "
         << max_value << endl;

    return 0;
}
