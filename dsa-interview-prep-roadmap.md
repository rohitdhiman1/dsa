# DSA Interview Prep Roadmap — Patterns & LeetCode Problems

Target: Mid/Senior SWE loops (Workday-tier + MAG-7). Difficulty tags: (E) Easy, (M) Medium, (H) Hard.
⭐ = high-frequency, must-do. Problems within each pattern are ordered easiest → hardest.

Suggested order of study is the order below. Phases 1–2 leverage your existing strengths (arrays/strings/linked lists); Phases 3–5 are where most MAG-7 interviews are won or lost.

---

## Phase 1 — Sharpen Your Strengths (Arrays / Strings / Linked Lists)

### 1. Two Pointers
- ⭐ 167. Two Sum II – Sorted Array (E)
- 125. Valid Palindrome (E)
- ⭐ 15. 3Sum (M)
- ⭐ 11. Container With Most Water (M)
- 42. Trapping Rain Water (H)
- 75. Sort Colors / Dutch National Flag (M)

### 2. Sliding Window
- ⭐ 121. Best Time to Buy and Sell Stock (E)
- ⭐ 3. Longest Substring Without Repeating Characters (M)
- 424. Longest Repeating Character Replacement (M)
- 567. Permutation in String (M)
- ⭐ 76. Minimum Window Substring (H)
- 239. Sliding Window Maximum (H) — monotonic deque crossover

### 3. Prefix Sum & Hashing
- ⭐ 1. Two Sum (E)
- ⭐ 560. Subarray Sum Equals K (M)
- 238. Product of Array Except Self (M)
- 128. Longest Consecutive Sequence (M)
- 49. Group Anagrams (M)
- 525. Contiguous Array (M)

### 4. Fast & Slow Pointers (Linked List Cycles)
- ⭐ 141. Linked List Cycle (E)
- 142. Linked List Cycle II (M)
- 876. Middle of the Linked List (E)
- 287. Find the Duplicate Number (M) — Floyd's on an array
- 234. Palindrome Linked List (E)

### 5. In-Place Linked List Manipulation
- ⭐ 206. Reverse Linked List (E)
- ⭐ 21. Merge Two Sorted Lists (E)
- 19. Remove Nth Node From End (M)
- 143. Reorder List (M)
- 92. Reverse Linked List II (M)
- ⭐ 25. Reverse Nodes in k-Group (H)
- 138. Copy List with Random Pointer (M)

---

## Phase 2 — Core Mechanics

### 6. Binary Search (incl. "search on answer space")
- ⭐ 704. Binary Search (E)
- ⭐ 33. Search in Rotated Sorted Array (M)
- 153. Find Minimum in Rotated Sorted Array (M)
- 74. Search a 2D Matrix (M)
- ⭐ 875. Koko Eating Bananas (M) — binary search on answer
- 1011. Capacity to Ship Packages in D Days (M)
- 4. Median of Two Sorted Arrays (H)

### 7. Stack & Monotonic Stack
- ⭐ 20. Valid Parentheses (E)
- 155. Min Stack (M)
- 150. Evaluate Reverse Polish Notation (M)
- ⭐ 739. Daily Temperatures (M) — monotonic stack
- 853. Car Fleet (M)
- ⭐ 84. Largest Rectangle in Histogram (H)

### 8. Intervals
- ⭐ 56. Merge Intervals (M)
- 57. Insert Interval (M)
- ⭐ 435. Non-overlapping Intervals (M)
- 252 / 253. Meeting Rooms I & II (E/M)
- 1851. Min Interval to Include Each Query (H)

### 9. Matrix / Simulation
- 36. Valid Sudoku (M)
- ⭐ 54. Spiral Matrix (M)
- 48. Rotate Image (M)
- 73. Set Matrix Zeroes (M)

---

## Phase 3 — Trees & Heaps (highest-frequency interview territory)

### 10. Binary Trees — DFS
- ⭐ 104. Maximum Depth of Binary Tree (E)
- 226. Invert Binary Tree (E)
- 543. Diameter of Binary Tree (E)
- 110. Balanced Binary Tree (E)
- ⭐ 236. Lowest Common Ancestor of a Binary Tree (M)
- ⭐ 124. Binary Tree Maximum Path Sum (H)
- 297. Serialize and Deserialize Binary Tree (H)

### 11. Binary Trees — BFS
- ⭐ 102. Binary Tree Level Order Traversal (M)
- 199. Binary Tree Right Side View (M)
- 103. Zigzag Level Order Traversal (M)
- 116. Populating Next Right Pointers (M)

### 12. Binary Search Trees
- 98. Validate Binary Search Tree (M)
- ⭐ 230. Kth Smallest Element in a BST (M)
- 235. LCA of a BST (M)
- 108. Convert Sorted Array to BST (E)

### 13. Heaps / Priority Queue
- 703. Kth Largest Element in a Stream (E)
- ⭐ 215. Kth Largest Element in an Array (M) — also know quickselect
- ⭐ 347. Top K Frequent Elements (M)
- 973. K Closest Points to Origin (M)
- ⭐ 295. Find Median from Data Stream (H) — two heaps
- 621. Task Scheduler (M)
- 23. Merge k Sorted Lists (H) — heap + linked list crossover

### 14. Tries
- ⭐ 208. Implement Trie (M)
- 211. Design Add and Search Words (M)
- 212. Word Search II (H)

---

## Phase 4 — Graphs & Backtracking

### 15. Graph BFS/DFS (grid + adjacency list)
- ⭐ 200. Number of Islands (M)
- 695. Max Area of Island (M)
- ⭐ 994. Rotting Oranges (M) — multi-source BFS
- 417. Pacific Atlantic Water Flow (M)
- 130. Surrounded Regions (M)
- ⭐ 133. Clone Graph (M)
- 127. Word Ladder (H)

### 16. Topological Sort
- ⭐ 207. Course Schedule (M)
- 210. Course Schedule II (M)
- 269. Alien Dictionary (H)

### 17. Union-Find (Disjoint Set)
- 323. Number of Connected Components (M)
- ⭐ 684. Redundant Connection (M)
- 721. Accounts Merge (M)
- 128. Longest Consecutive Sequence (M) — alt. UF solution

### 18. Shortest Paths / Weighted Graphs
- ⭐ 743. Network Delay Time (M) — Dijkstra
- 787. Cheapest Flights Within K Stops (M) — Bellman-Ford / BFS+pruning
- 1584. Min Cost to Connect All Points (M) — Prim's/Kruskal's MST
- 778. Swim in Rising Water (H)

### 19. Backtracking
- ⭐ 78. Subsets (M)
- 90. Subsets II (M)
- ⭐ 46. Permutations (M)
- ⭐ 39. Combination Sum (M)
- 40. Combination Sum II (M)
- 79. Word Search (M)
- 131. Palindrome Partitioning (M)
- 51. N-Queens (H)

---

## Phase 5 — Dynamic Programming & Greedy

### 20. 1-D DP
- ⭐ 70. Climbing Stairs (E)
- 746. Min Cost Climbing Stairs (E)
- ⭐ 198. House Robber (M) + 213. House Robber II (M)
- ⭐ 322. Coin Change (M)
- 139. Word Break (M)
- ⭐ 300. Longest Increasing Subsequence (M) — know the O(n log n) version
- 152. Maximum Product Subarray (M)

### 21. 2-D DP / Strings
- 62. Unique Paths (M)
- ⭐ 1143. Longest Common Subsequence (M)
- 5. Longest Palindromic Substring (M)
- ⭐ 72. Edit Distance (M)
- 97. Interleaving String (M)
- 10. Regular Expression Matching (H)

### 22. Knapsack Variants
- ⭐ 416. Partition Equal Subset Sum (M) — 0/1 knapsack
- 494. Target Sum (M)
- 518. Coin Change II (M) — unbounded

### 23. Greedy
- ⭐ 53. Maximum Subarray (M) — Kadane's
- ⭐ 55. Jump Game (M) + 45. Jump Game II (M)
- 134. Gas Station (M)
- 763. Partition Labels (M)
- 678. Valid Parenthesis String (M)

---

## Phase 6 — Rounding Out

### 24. Design (very common at senior level)
- ⭐ 146. LRU Cache (M)
- 460. LFU Cache (H)
- 380. Insert Delete GetRandom O(1) (M)
- 355. Design Twitter (M)
- 981. Time Based Key-Value Store (M)

### 25. Bit Manipulation
- 136. Single Number (E)
- 191. Number of 1 Bits (E)
- 338. Counting Bits (E)
- 268. Missing Number (E)
- 371. Sum of Two Integers (M)

### 26. Math / Misc
- 202. Happy Number (E)
- 50. Pow(x, n) (M)
- 43. Multiply Strings (M)
- 7 / 8. Reverse Integer & atoi (M) — string-parsing edge cases

---

## How to Use This List

1. **Per pattern:** learn the template first, then solve in order. Aim for ⭐ problems minimum if short on time (~75 core problems).
2. **Timing discipline:** Easy ≤ 15 min, Medium ≤ 25–30 min, Hard ≤ 40 min. If stuck past the limit, read the approach (not the code), then implement yourself.
3. **Spaced repetition:** re-solve any problem you couldn't do unaided after 3 days, then 1 week.
4. **Always state complexity** out loud (time + space) before and after coding — interviewers expect this unprompted at your level.
5. **Mock cadence:** after Phase 3, start 1–2 timed mocks per week (Pramp, interviewing.io, or peer mocks).

## Progress Tracker (we'll maintain this together)

| Pattern | Status | Confidence | Notes |
|---|---|---|---|
| Two Pointers | Not started | — | |
| Sliding Window | Not started | — | |
| ... | | | |

Tell me whenever you finish a pattern or struggle with a problem, and I'll flag shaky areas here.
