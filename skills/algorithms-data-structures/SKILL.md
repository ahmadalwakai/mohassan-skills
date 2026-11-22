---
name: الخوارزميات وهياكل البيانات
description: الخوارزميات وهياكل البيانات: التعقيد الزمني Big O، البحث الثنائي، الفرز، المخططات graphs، البرمجة الديناميكية، الأشجار، أسئلة المقابلات البرمجية. algorithm algorithms structures complexity sorting binary tree trees graph graphs heap stack hash dynamic programming leetcode recursion خوارزمية خوارزميات الخوارزميات هياكل المصفوفات الفرز التعقيد
version: 1.0.0
category: coding
---
Use this for algorithm design, complexity analysis and data structure choices.
1. Clarify the problem: input size, constraints and edge cases (empty, one element, duplicates, negatives, very large values), and whether the input is sorted or streamed.
2. State a brute-force solution and its complexity, then improve it. Input size hints at the target: n ≤ 20 allows exponential search, n ≤ 10^4 allows O(n^2), n ≤ 10^6 needs O(n log n) or O(n).
3. Pick the structure for the dominant operation: hash map or set for O(1) lookup and counting; array for indexed access; heap for repeated min or max (priority queue, top-k); balanced tree or sorted array with binary search for ordered queries; deque for sliding windows and BFS; stack for matching and monotonic problems; union-find for connectivity.
4. Patterns: two pointers, sliding window, prefix sums, binary search on the answer, BFS for shortest paths without weights, Dijkstra for non-negative weights, topological sort for dependencies, dynamic programming when subproblems overlap (define the state, the transition and the base case, then iterate).
5. Binary search runs in O(log n) on sorted data; write the loop invariant and test the boundaries (first, last, missing element) to avoid off-by-one errors.
6. Give time and space complexity of the final solution and why it is correct (an invariant or a proof sketch).
7. Trace a small example by hand, then the edge cases.
Answer shape: the idea in two sentences, complexity, clean code, a traced example.
