# 10-Week DSA Blueprint

**Profile:** 9 YoE | Java | ~17 hrs/week
**Strong:** Arrays, Strings, Linked Lists | **Shaky:** Graphs, DP, Heaps, Backtracking, Design
**Budget:** 2.5 hrs weekdays + 5 hrs weekends | 15-18 problems/week

---

## Rules

**Timing:** Easy < 15 min | Medium < 25 min | Hard < 40 min
**If stuck past the limit:** read the *approach* (not the code), then implement yourself.
**Re-solve rule:** any problem you couldn't do unaided — re-solve after 3 days, then after 1 week.
**Complexity:** always state time + space complexity out loud before and after coding.
**DP method every time:** brute-force recursion -> identify repeated states -> memoize -> tabulate -> space-optimize.

**Legend:** ⭐ = high-frequency must-do | (E) Easy | (M) Medium | (H) Hard

---

## Weekly Rhythm (17 hrs)

| Day       | Focus                                              | Time     |
|-----------|----------------------------------------------------|----------|
| Mon-Thu   | 2 new problems + 15 min reviewing yesterday's      | 2.5 hrs  |
| Fri       | 1 new problem + 2 re-solves from shaky queue        | 2.5 hrs  |
| Sat       | Hard problems, mock interview, or deep practice     | 3-4 hrs  |
| Sun       | Notes review, 1 problem, plan next week             | 1.5-2 hrs|

**Mock cadence:** first mock end of Week 4, then 1/week from Week 5 onward, 2/week in Week 10.

---

## Slip Rule

Behind schedule? Cut in this order:
1. Non-starred problems
2. Week 9 bit manipulation / math day
3. **Never** cut Graphs (W5-6) or DP (W7-8)

---

# WEEK 1 — Speed Runs on Strengths

*Treat starred problems as timed drills: Easy < 12 min, Medium < 22 min.*
*Any problem that blows the time limit goes into the re-solve queue.*

### Pattern 1: Two Pointers
- [ ] ⭐ **167. Two Sum II - Sorted Array** (E)
- [ ] 125. Valid Palindrome (E)
- [ ] ⭐ **15. 3Sum** (M)
- [ ] ⭐ **11. Container With Most Water** (M)
- [ ] 75. Sort Colors / Dutch National Flag (M)
- [ ] 42. Trapping Rain Water (H) — *weekend*

> Template: left = 0, right = end; move the pointer that improves the objective.

### Pattern 2: Sliding Window
- [ ] ⭐ **121. Best Time to Buy and Sell Stock** (E)
- [ ] ⭐ **3. Longest Substring Without Repeating Characters** (M)
- [ ] 424. Longest Repeating Character Replacement (M)
- [ ] 567. Permutation in String (M)
- [ ] ⭐ **76. Minimum Window Substring** (H)
- [ ] 239. Sliding Window Maximum (H) — monotonic deque crossover

> Template: expand right until valid, shrink left until invalid, track best.

### Pattern 3: Prefix Sum & Hashing
- [ ] ⭐ **1. Two Sum** (E)
- [ ] ⭐ **560. Subarray Sum Equals K** (M)
- [ ] 238. Product of Array Except Self (M)
- [ ] 128. Longest Consecutive Sequence (M)
- [ ] 49. Group Anagrams (M)
- [ ] 525. Contiguous Array (M)

> Key insight: prefix[j] - prefix[i] = subarray sum from i+1 to j.

### Pattern 4: Fast & Slow Pointers
- [ ] ⭐ **141. Linked List Cycle** (E)
- [ ] 142. Linked List Cycle II (M)
- [ ] 876. Middle of the Linked List (E)
- [ ] 287. Find the Duplicate Number (M) — Floyd's on an array
- [ ] 234. Palindrome Linked List (E)

> Template: slow moves 1 step, fast moves 2. They meet inside cycle. Reset one to head for entry point.

### Pattern 5: In-Place Linked List Manipulation
- [ ] ⭐ **206. Reverse Linked List** (E)
- [ ] ⭐ **21. Merge Two Sorted Lists** (E)
- [ ] 19. Remove Nth Node From End (M)
- [ ] 143. Reorder List (M)
- [ ] 92. Reverse Linked List II (M)
- [ ] 138. Copy List with Random Pointer (M)
- [ ] ⭐ **25. Reverse Nodes in k-Group** (H) — *weekend*

> Template: prev/curr/next trio for reversal. Draw the pointer changes before coding.

### Week 1 Checkpoint
- [ ] All ⭐ problems solved within time limits
- [ ] Weekend hards attempted: 42, 25
- [ ] Re-solve queue started for blown time limits

**Problems this week: 30 | Starred: 13**

---

# WEEK 2 — Core Mechanics

*Full problem lists, not just starred. These patterns feed graphs and DP later.*

### Pattern 6: Binary Search
- [ ] ⭐ **704. Binary Search** (E)
- [ ] ⭐ **33. Search in Rotated Sorted Array** (M)
- [ ] 153. Find Minimum in Rotated Sorted Array (M)
- [ ] 74. Search a 2D Matrix (M)
- [ ] ⭐ **875. Koko Eating Bananas** (M) — binary search on answer
- [ ] 1011. Capacity to Ship Packages in D Days (M)
- [ ] 4. Median of Two Sorted Arrays (H) — *weekend*

> Two templates: (1) find exact match, (2) search on answer space — "can I do X in Y?" -> binary search on Y.

### Pattern 7: Stack & Monotonic Stack
- [ ] ⭐ **20. Valid Parentheses** (E)
- [ ] 155. Min Stack (M)
- [ ] 150. Evaluate Reverse Polish Notation (M)
- [ ] ⭐ **739. Daily Temperatures** (M) — monotonic stack
- [ ] 853. Car Fleet (M)
- [ ] ⭐ **84. Largest Rectangle in Histogram** (H) — *weekend*

> Monotonic stack template: pop while stack top is worse than current; the answer for popped element involves current and new stack top.

### Pattern 8: Intervals
- [ ] ⭐ **56. Merge Intervals** (M)
- [ ] 57. Insert Interval (M)
- [ ] ⭐ **435. Non-overlapping Intervals** (M)
- [ ] 252 / 253. Meeting Rooms I & II (E/M)
- [ ] 1851. Min Interval to Include Each Query (H)

> Always sort by start time first. Overlap check: b.start < a.end.

### Pattern 9: Matrix / Simulation
- [ ] 36. Valid Sudoku (M)
- [ ] ⭐ **54. Spiral Matrix** (M)
- [ ] 48. Rotate Image (M)
- [ ] 73. Set Matrix Zeroes (M)

> Spiral: use 4 boundaries (top, bottom, left, right), shrink after each pass.

### Week 2 Checkpoint
- [ ] All ⭐ problems solved within time limits
- [ ] Weekend hards attempted: 4, 84
- [ ] Binary search on answer space pattern solid

**Problems this week: 22 | Starred: 8**

---

# WEEK 3 — Trees

*Focus: the "return value vs. global state" DFS distinction (diameter, max path sum) — this is the #1 tree concept interviews probe.*

### Pattern 10: Binary Trees - DFS
- [ ] ⭐ **104. Maximum Depth of Binary Tree** (E)
- [ ] 226. Invert Binary Tree (E)
- [ ] 543. Diameter of Binary Tree (E)
- [ ] 110. Balanced Binary Tree (E)
- [ ] ⭐ **236. Lowest Common Ancestor of a Binary Tree** (M)
- [ ] ⭐ **124. Binary Tree Maximum Path Sum** (H) — *weekend*
- [ ] 297. Serialize and Deserialize Binary Tree (H) — *weekend*

> Key concept: DFS returns value UP to parent; use a global variable when the answer spans two branches (diameter, max path sum).

### Pattern 11: Binary Trees - BFS
- [ ] ⭐ **102. Binary Tree Level Order Traversal** (M)
- [ ] 199. Binary Tree Right Side View (M)
- [ ] 103. Zigzag Level Order Traversal (M)
- [ ] 116. Populating Next Right Pointers (M)

> Template: queue with level-size loop. `int size = queue.size(); for (int i = 0; i < size; i++)`.

### Pattern 12: Binary Search Trees
- [ ] 98. Validate Binary Search Tree (M)
- [ ] ⭐ **230. Kth Smallest Element in a BST** (M)
- [ ] 235. LCA of a BST (M)
- [ ] 108. Convert Sorted Array to BST (E)

> BST property: inorder traversal gives sorted order. Use this for validation and kth element.

### Week 3 Checkpoint
- [ ] All ⭐ problems solved within time limits
- [ ] Can articulate return-value vs. global-state DFS distinction
- [ ] Weekend hards attempted: 124, 297
- [ ] First re-solve sweep of Week 1-2 misses

**Problems this week: 15 | Starred: 5**

---

# WEEK 4 — Heaps, Tries & Design Intro [SHAKY AREA]

### Pattern 13: Heaps / Priority Queue
- [ ] 703. Kth Largest Element in a Stream (E)
- [ ] ⭐ **215. Kth Largest Element in an Array** (M) — also learn quickselect
- [ ] ⭐ **347. Top K Frequent Elements** (M)
- [ ] 973. K Closest Points to Origin (M)
- [ ] ⭐ **295. Find Median from Data Stream** (H) — two-heap pattern
- [ ] 621. Task Scheduler (M)
- [ ] 23. Merge k Sorted Lists (H) — heap + linked list crossover

> Java: `PriorityQueue<int[]> pq = new PriorityQueue<>((a,b) -> a[0] - b[0]);` — drill comparators until automatic.
> Two-heap pattern: max-heap for lower half, min-heap for upper half, balance sizes.

### Pattern 14: Tries
- [ ] ⭐ **208. Implement Trie** (M)
- [ ] 211. Design Add and Search Words (M)
- [ ] 212. Word Search II (H)

> Trie node: `TrieNode[] children = new TrieNode[26]; boolean isEnd;`

### Pattern 24 (start): Design
- [ ] ⭐ **146. LRU Cache** (M) — HashMap + doubly linked list
- [ ] 380. Insert Delete GetRandom O(1) (M) — HashMap + ArrayList

> LRU: every get/put moves node to head. Evict from tail. O(1) everything via map + DLL.

### Week 4 Checkpoint
- [ ] PriorityQueue comparators are automatic
- [ ] Can implement Trie from scratch in < 10 min
- [ ] LRU Cache implementation is solid
- [ ] First mock interview completed this weekend

**Problems this week: 12 | Starred: 5**

---

# WEEK 5 — Graphs I [SHAKY AREA - DOUBLE WIDTH START]

*Drill until you can write BFS-with-visited-set and recursive DFS from memory in < 3 min.*

### Pattern 15: Graph BFS/DFS (grid + adjacency list)
- [ ] ⭐ **200. Number of Islands** (M)
- [ ] 695. Max Area of Island (M)
- [ ] ⭐ **994. Rotting Oranges** (M) — multi-source BFS
- [ ] 417. Pacific Atlantic Water Flow (M) — reverse thinking
- [ ] 130. Surrounded Regions (M)
- [ ] ⭐ **133. Clone Graph** (M)
- [ ] 127. Word Ladder (H)

> Grid BFS template: `int[][] dirs = {{0,1},{0,-1},{1,0},{-1,0}};` + visited set + queue.
> Multi-source BFS: add ALL sources to queue at start, then process level by level.
> Reverse thinking: instead of "where does water flow FROM here", ask "where does water flow TO here".

### Pattern 16: Topological Sort
- [ ] ⭐ **207. Course Schedule** (M)
- [ ] 210. Course Schedule II (M)
- [ ] 269. Alien Dictionary (H)

> Two approaches: (1) Kahn's BFS with in-degree array, (2) DFS with 3-color marking (white/gray/black). Learn Kahn's first.

### Week 5 Checkpoint
- [ ] Can write BFS and DFS graph templates from memory in < 3 min
- [ ] Multi-source BFS pattern is solid
- [ ] Topological sort via Kahn's is solid
- [ ] 1 mock interview this week

**Problems this week: 10 | Starred: 4**

---

# WEEK 6 — Graphs II + Backtracking [SHAKY AREA - DOUBLE WIDTH END]

### Pattern 17: Union-Find (Disjoint Set)
- [ ] 323. Number of Connected Components (M)
- [ ] ⭐ **684. Redundant Connection** (M)
- [ ] 721. Accounts Merge (M)
- [ ] 128. Longest Consecutive Sequence (M) — alt. UF solution

> Hand-roll and memorize: `find(x)` with path compression + `union(x,y)` with rank. ~15 lines of code.

### Pattern 18: Shortest Paths / Weighted Graphs
- [ ] ⭐ **743. Network Delay Time** (M) — Dijkstra
- [ ] 787. Cheapest Flights Within K Stops (M) — Bellman-Ford / BFS+pruning
- [ ] 1584. Min Cost to Connect All Points (M) — Prim's / Kruskal's MST
- [ ] 778. Swim in Rising Water (H)

> Dijkstra template: `PriorityQueue` + `dist[]` array + relax edges. Does NOT work with negative weights.

### Pattern 19: Backtracking [SHAKY]
- [ ] ⭐ **78. Subsets** (M)
- [ ] 90. Subsets II (M)
- [ ] ⭐ **46. Permutations** (M)
- [ ] ⭐ **39. Combination Sum** (M)
- [ ] 40. Combination Sum II (M)
- [ ] 79. Word Search (M)
- [ ] 131. Palindrome Partitioning (M)
- [ ] 51. N-Queens (H) — *weekend*

> Template: `choose -> explore -> unchoose`. For duplicates: sort first, skip `nums[i] == nums[i-1]` when `i > start`.

### Week 6 Checkpoint
- [ ] UnionFind class written from memory with path compression + rank
- [ ] Can identify when to use Dijkstra vs. Bellman-Ford vs. BFS
- [ ] Backtracking choose/explore/unchoose template is automatic
- [ ] Weekend hard attempted: 51 (N-Queens)
- [ ] 1 mock interview this week

**Problems this week: 16 | Starred: 4**

---

# WEEK 7 — Dynamic Programming I [SHAKY AREA - DOUBLE WIDTH START]

*Method every time: brute-force recursion -> identify repeated states -> memoize -> tabulate -> space-optimize.*
*Don't skip writing the recurrence in plain words before coding.*

### Pattern 20: 1-D DP
- [ ] ⭐ **70. Climbing Stairs** (E)
- [ ] 746. Min Cost Climbing Stairs (E)
- [ ] ⭐ **198. House Robber** (M)
- [ ] 213. House Robber II (M)
- [ ] ⭐ **322. Coin Change** (M)
- [ ] 139. Word Break (M)
- [ ] ⭐ **300. Longest Increasing Subsequence** (M) — know the O(n log n) version
- [ ] 152. Maximum Product Subarray (M)

> 1-D DP framework: define `dp[i]` = best answer considering elements 0..i. Recurrence relates dp[i] to dp[i-1], dp[i-2], etc.

### Pattern 23: Greedy
- [ ] ⭐ **53. Maximum Subarray** (M) — Kadane's algorithm
- [ ] ⭐ **55. Jump Game** (M)
- [ ] 45. Jump Game II (M)
- [ ] 134. Gas Station (M)
- [ ] 763. Partition Labels (M)
- [ ] 678. Valid Parenthesis String (M)

> Greedy vs DP: if a locally optimal choice is globally optimal (provably), use greedy. If unsure, start with DP.

### Week 7 Checkpoint
- [ ] Can write recurrence in plain words before coding for every problem
- [ ] Kadane's algorithm is automatic
- [ ] LIS O(n log n) with patience sorting understood
- [ ] 1 mock interview this week

**Problems this week: 14 | Starred: 6**

---

# WEEK 8 — Dynamic Programming II [SHAKY AREA - DOUBLE WIDTH END]

### Pattern 21: 2-D DP / Strings
- [ ] 62. Unique Paths (M)
- [ ] ⭐ **1143. Longest Common Subsequence** (M)
- [ ] 5. Longest Palindromic Substring (M)
- [ ] ⭐ **72. Edit Distance** (M)
- [ ] 97. Interleaving String (M)
- [ ] 10. Regular Expression Matching (H) — *weekend: attempt, then study*

> LCS and Edit Distance share one grid mental model: `dp[i][j]` = answer for first i chars of s1 and first j chars of s2. Learn this grid once, reuse everywhere.

### Pattern 22: Knapsack Variants
- [ ] ⭐ **416. Partition Equal Subset Sum** (M) — 0/1 knapsack
- [ ] 494. Target Sum (M)
- [ ] 518. Coin Change II (M) — unbounded knapsack

> 0/1 knapsack: each item used at most once, iterate items outer, capacity inner (reverse).
> Unbounded: each item reusable, iterate capacity forward.

### Week 8 Checkpoint
- [ ] 2-D DP grid mental model is solid
- [ ] Can distinguish 0/1 vs. unbounded knapsack and choose correct loop direction
- [ ] Weekend hard attempted: 10 (Regex Matching)
- [ ] Re-solve sweep of Week 5-7 misses
- [ ] 1 mock interview this week

**Problems this week: 9 | Starred: 3**

---

# WEEK 9 — Design Depth + Gaps + Tuning

### Pattern 24 (finish): Design
- [ ] 460. LFU Cache (H)
- [ ] 355. Design Twitter (M)
- [ ] 981. Time Based Key-Value Store (M)

### Pattern 25: Bit Manipulation (1 day)
- [ ] 136. Single Number (E)
- [ ] 191. Number of 1 Bits (E)
- [ ] 338. Counting Bits (E)
- [ ] 268. Missing Number (E)
- [ ] 371. Sum of Two Integers (M)

> Key operations: XOR for toggle/find-unique, AND for check-bit, shift for traversal. `n & (n-1)` clears lowest set bit.

### Pattern 26: Math / Misc (1 day)
- [ ] 202. Happy Number (E)
- [ ] 50. Pow(x, n) (M)
- [ ] 43. Multiply Strings (M)
- [ ] 7 / 8. Reverse Integer & atoi (M) — string-parsing edge cases

### Week 9 Checkpoint
- [ ] All 5 design problems implemented cleanly
- [ ] Bit tricks are quick-reference ready
- [ ] Started target company tagged problem lists
- [ ] 1 full mock interview
- [ ] Behavioral story prep started (STAR format, 8-10 stories)

**Problems this week: 12 | Starred: 0 (consolidation week)**

---

# WEEK 10 — Simulation Week

*No new patterns. This week is pure exam prep.*

### Daily Practice
- [ ] Mon: 2 random unseen mediums, 60-min block, no pauses
- [ ] Tue: 2 random unseen mediums, 60-min block, no pauses
- [ ] Wed: 2 random unseen mediums, 60-min block, no pauses
- [ ] Thu: 2 random unseen mediums, 60-min block, no pauses
- [ ] Fri: Re-solve everything still in shaky queue

### Weekend
- [ ] Sat: Full mock interview (with a stranger, not a friend)
- [ ] Sun: Full mock interview + light review only

### Week 10 Checkpoint
- [ ] 8 random mediums completed under timed conditions
- [ ] Shaky queue is empty or nearly empty
- [ ] 2 mock interviews completed (at least 1 with a stranger)
- [ ] Light review only on the 2 days before any real interview

---

## Quick Pattern Reference

### How to use: read the problem, scan the "Recognize When..." column, match the pattern, apply the template.

---

#### Arrays & Strings

| #  | Pattern              | Recognize When...                                              | Template / Key Idea                          | Go-To Problem |
|----|----------------------|----------------------------------------------------------------|----------------------------------------------|---------------|
| 1  | Two Pointers         | Sorted array; find pair with condition; compare from both ends | `L=0, R=end; move pointer that improves ans` | 15. 3Sum      |
| 2  | Sliding Window       | Contiguous subarray/substring; max/min with constraint         | Expand R until valid, shrink L until invalid | 76. Min Window Substring |
| 3  | Prefix Sum & Hashing | Subarray sum equals K; count subarrays; cumulative property    | `prefix[j] - prefix[i] = sum(i+1..j)`       | 560. Subarray Sum = K |
| 4  | Fast & Slow Pointers | Detect cycle; find middle; linked list has a loop              | `slow += 1, fast += 2; meet = cycle exists`  | 141. LL Cycle  |
| 5  | Linked List Ops      | Reverse, merge, reorder a linked list in-place                 | `prev / curr / next` pointer trio            | 206. Reverse LL |

#### Search & Structure

| #  | Pattern              | Recognize When...                                              | Template / Key Idea                          | Go-To Problem |
|----|----------------------|----------------------------------------------------------------|----------------------------------------------|---------------|
| 6  | Binary Search        | Sorted input; "min value that satisfies X"; search on answer   | `while (lo < hi)` + midpoint + condition     | 875. Koko Bananas |
| 7  | Monotonic Stack      | "Next greater/smaller element"; histogram; temperature         | Pop worse, answer uses current + new top     | 739. Daily Temps |
| 8  | Intervals            | Overlapping ranges; merge/insert/count intervals               | Sort by start; overlap = `b.start < a.end`   | 56. Merge Intervals |
| 9  | Matrix / Simulation  | 2D grid traversal; spiral order; rotate/transform in-place     | Boundary vars (top/bot/left/right), shrink   | 54. Spiral Matrix |

#### Trees

| #  | Pattern              | Recognize When...                                              | Template / Key Idea                          | Go-To Problem |
|----|----------------------|----------------------------------------------------------------|----------------------------------------------|---------------|
| 10 | Tree DFS             | Path sum; diameter; max depth; any root-to-leaf question       | Return value UP vs. global state across branches | 124. Max Path Sum |
| 11 | Tree BFS             | Level order; right side view; zigzag; "level by level"         | Queue + `size = queue.size()` level loop     | 102. Level Order |
| 12 | BSTs                 | Sorted tree operations; validate BST; kth smallest            | Inorder traversal = sorted order             | 230. Kth Smallest |

#### Heaps & Tries

| #  | Pattern              | Recognize When...                                              | Template / Key Idea                          | Go-To Problem |
|----|----------------------|----------------------------------------------------------------|----------------------------------------------|---------------|
| 13 | Heaps / PQ           | "Top K"; "kth largest/smallest"; streaming median              | PQ + comparator; two-heap for median         | 295. Median Stream |
| 14 | Tries                | Prefix search; autocomplete; word dictionary with wildcards    | `TrieNode[26] children + boolean isEnd`      | 208. Implement Trie |

#### Graphs

| #  | Pattern              | Recognize When...                                              | Template / Key Idea                          | Go-To Problem |
|----|----------------------|----------------------------------------------------------------|----------------------------------------------|---------------|
| 15 | Graph BFS/DFS        | Connected components; islands; flood fill; shortest unweighted | Visited set + queue (BFS) or stack (DFS)     | 200. Num Islands |
| 16 | Topological Sort     | Prerequisites; dependency order; "can I finish all courses?"   | Kahn's: in-degree array + BFS queue          | 207. Course Schedule |
| 17 | Union-Find           | "Are X and Y connected?"; group merging; redundant edges       | `find()` + path compression, `union()` + rank| 684. Redundant Connection |
| 18 | Shortest Paths       | Weighted graph; minimum cost; "delay time"; K stops            | Dijkstra = PQ + dist[]; no negative weights  | 743. Network Delay |
| 19 | Backtracking         | Generate all subsets/permutations/combinations; constraint satisfaction | `choose -> explore -> unchoose`        | 78. Subsets    |

#### Dynamic Programming

| #  | Pattern              | Recognize When...                                              | Template / Key Idea                          | Go-To Problem |
|----|----------------------|----------------------------------------------------------------|----------------------------------------------|---------------|
| 20 | 1-D DP               | Optimal value with decisions at each step; "number of ways"    | `dp[i]` relates to `dp[i-1], dp[i-2]...`    | 322. Coin Change |
| 21 | 2-D DP / Strings     | Two strings; edit distance; LCS; interleaving; regex           | `dp[i][j]` = answer for `s1[0..i] x s2[0..j]` | 72. Edit Distance |
| 22 | Knapsack             | Subset to reach target sum; pick items with capacity limit     | 0/1 = reverse loop; unbounded = forward      | 416. Partition Sum |
| 23 | Greedy               | Locally optimal = globally optimal; interval scheduling        | Prove greedy choice property first           | 55. Jump Game  |

#### Design & Misc

| #  | Pattern              | Recognize When...                                              | Template / Key Idea                          | Go-To Problem |
|----|----------------------|----------------------------------------------------------------|----------------------------------------------|---------------|
| 24 | Design               | "Design a data structure"; O(1) get/put/random                 | HashMap + DLL (LRU); HashMap + List (random) | 146. LRU Cache |
| 25 | Bit Manipulation     | Single number; missing number; no extra space; XOR tricks      | XOR = find unique; `n & (n-1)` = clear low bit | 136. Single Number |
| 26 | Math                 | Power function; string multiply; number theory                 | Fast exponentiation; digit-by-digit simulate | 50. Pow(x,n)   |

---

### Pattern Decision Flowchart

```
Problem involves an array/string?
├── Sorted? ─────────────────────> Two Pointers or Binary Search
├── Contiguous subarray? ────────> Sliding Window or Prefix Sum
├── Intervals/ranges? ──────────> Intervals (sort by start)
└── "Next greater/smaller"? ────> Monotonic Stack

Problem involves a linked list?
├── Cycle detection? ───────────> Fast & Slow Pointers
└── Reverse/reorder? ──────────> In-Place LL Manipulation

Problem involves a tree?
├── Level-by-level? ────────────> BFS (queue + level loop)
├── Path/depth/diameter? ──────> DFS (return value vs. global)
└── Sorted tree property? ─────> BST (inorder = sorted)

Problem involves a graph?
├── Unweighted shortest path? ─> BFS
├── Weighted shortest path? ───> Dijkstra (or Bellman-Ford if negative)
├── Dependencies/ordering? ────> Topological Sort
├── Connected components? ─────> Union-Find or DFS
└── Grid with regions? ────────> BFS/DFS with visited set

Problem asks "generate all..." or "find all combinations"?
└── Backtracking ──────────────> choose -> explore -> unchoose

Problem asks "min cost / max value / number of ways"?
├── Optimal substructure + overlapping subproblems? ──> DP
├── Two strings? ──────────────> 2-D DP
├── Subset with target? ──────> Knapsack
└── Greedy choice provable? ──> Greedy

Problem asks "top K" or "kth largest"?
└── Heap / PriorityQueue

Problem asks "design a data structure"?
└── Design (HashMap + supporting structure)

Problem says "O(1) space" or "without extra space"?
└── Bit Manipulation or Math trick
```

---

## Totals

| Week | Focus                          | Problems | Starred |
|------|--------------------------------|----------|---------|
| 1    | Arrays / Strings / LL          | 30       | 13      |
| 2    | Binary Search / Stack / Intervals | 22    | 8       |
| 3    | Trees                          | 15       | 5       |
| 4    | Heaps / Tries / Design I       | 12       | 5       |
| 5    | Graphs I                       | 10       | 4       |
| 6    | Graphs II / Backtracking       | 16       | 4       |
| 7    | 1-D DP / Greedy                | 14       | 6       |
| 8    | 2-D DP / Knapsack              | 9        | 3       |
| 9    | Design II / Bits / Math        | 12       | 0       |
| 10   | Simulation & review            | 8+       | -       |
|      | **TOTAL**                      | **~148** | **48**  |

---

## Shaky Area Tracker

| Area                        | Self-Assessed | Verified | Status          |
|-----------------------------|---------------|----------|-----------------|
| Graphs                      | Shaky         |          | Scheduled W5-6  |
| Dynamic Programming         | Shaky         |          | Scheduled W7-8  |
| Heaps / Backtracking / Design | Shaky       |          | Scheduled W4,6,9|
| Trees                       | OK?           |          | Verify in W3    |
| Arrays / Strings / LL       | Strong        |          | Verify with W1 timed drills |

---

## Re-Solve Queue

| # | Problem | Date Failed | Re-solve 1 (3 days) | Re-solve 2 (1 week) | Clear? |
|---|---------|-------------|---------------------|----------------------|--------|
|   |         |             |                     |                      |        |
|   |         |             |                     |                      |        |
|   |         |             |                     |                      |        |
|   |         |             |                     |                      |        |
|   |         |             |                     |                      |        |
|   |         |             |                     |                      |        |
|   |         |             |                     |                      |        |
|   |         |             |                     |                      |        |
|   |         |             |                     |                      |        |
|   |         |             |                     |                      |        |
|   |         |             |                     |                      |        |
|   |         |             |                     |                      |        |
|   |         |             |                     |                      |        |
|   |         |             |                     |                      |        |
|   |         |             |                     |                      |        |

---

## Weekly Progress

| Week | Planned | Completed | Starred Done | Mocks | Notes |
|------|---------|-----------|--------------|-------|-------|
| 1    |         |           |              |       |       |
| 2    |         |           |              |       |       |
| 3    |         |           |              |       |       |
| 4    |         |           |              |       |       |
| 5    |         |           |              |       |       |
| 6    |         |           |              |       |       |
| 7    |         |           |              |       |       |
| 8    |         |           |              |       |       |
| 9    |         |           |              |       |       |
| 10   |         |           |              |       |       |
