# Personalized 10-Week Plan — Java · ~17 hrs/week · MAG-7 + Top SaaS

Profile: 9 YoE, strong in arrays/strings/linked lists. Flagged shaky: Graphs, DP, Heaps/Backtracking/Design.
Budget: 2.5 hrs weekdays + ~5 hrs weekends ≈ 17 hrs/week → 15–18 problems/week is sustainable.
Strategy: compress strengths to 1 week, give Graphs and DP a double-width 2 weeks each, and push heaps/design depth since they're flagged. Tree week stays because graphs and DP are built on tree-recursion intuition.

Pattern numbers (#) refer to dsa-interview-prep-roadmap.md.

---

## Week 1 — Speed runs on strengths (Phases 1, compressed)
Two Pointers (#1) · Sliding Window (#2) · Prefix/Hash (#3) · Fast & Slow (#4) · LL Manipulation (#5)
- ⭐ problems only, treat as timed drills: Easy ≤ 12 min, Medium ≤ 22 min
- Any problem that blows the time limit goes into the re-solve queue
- Weekend: 42. Trapping Rain Water + 25. Reverse Nodes in k-Group (the two hards) untimed

## Week 2 — Core mechanics (Phase 2)
Binary Search (#6) · Monotonic Stack (#7) · Intervals (#8) · Matrix (#9)
- Full problem lists, not just ⭐ — these patterns feed graphs and DP later
- Weekend: 4. Median of Two Sorted Arrays + 84. Largest Rectangle in Histogram

## Week 3 — Trees (Phase 3a)
Tree DFS (#10) · Tree BFS (#11) · BSTs (#12)
- Focus: the "return value vs. global state" DFS distinction (diameter, max path sum) — this is the #1 tree concept interviews probe
- Weekend: 124. Max Path Sum + 297. Serialize/Deserialize + first re-solve sweep of Weeks 1–2 misses

## Week 4 — Heaps, Tries, first Design ⚠ flagged area
Heaps (#13) · Tries (#14) · start Design (#24): 146. LRU Cache, 380. Insert Delete GetRandom
- Heaps: drill Java PriorityQueue comparators until automatic; learn quickselect for 215
- Two-heaps pattern (295. Median from Data Stream) is a MAG-7 favorite
- 🎤 First mock this weekend (Pramp / peer)

## Weeks 5–6 — Graphs, double width ⚠ flagged area
- Week 5: Grid + adjacency BFS/DFS (#15), Topological Sort (#16)
  - Drill until you can write BFS-with-visited-set and recursive DFS from memory in < 3 min
  - Multi-source BFS (994) and "reverse thinking" (417 Pacific Atlantic) are the conceptual leaps
- Week 6: Union-Find (#17), Shortest Paths (#18), Backtracking (#19) ⚠
  - Hand-roll a UnionFind class with path compression + rank; memorize it
  - Backtracking: master the choose → explore → unchoose template via 78/46/39, then 79 and 131
- 🎤 1 mock per week from here on
- Weekend W6: 127. Word Ladder + 51. N-Queens

## Weeks 7–8 — Dynamic Programming, double width ⚠ flagged area
- Week 7: 1-D DP (#20) + Greedy (#23)
  - Method every time: brute-force recursion → identify repeated states → memoize → (only if asked) tabulate → (bonus) space-optimize
  - Don't skip writing the recurrence in plain words before coding
- Week 8: 2-D/String DP (#21) + Knapsack (#22)
  - LCS (1143) and Edit Distance (72) share one grid mental model — learn it once, reuse everywhere
- Weekend W8: 10. Regular Expression Matching (attempt, then study) + re-solve sweep

## Week 9 — Design depth + gaps + company tuning
- Finish Design (#24): 460 LFU, 355 Design Twitter, 981 Time-Based KV Store
- Bit Manipulation (#25) + Math (#26): one light day each
- Start company-tagged problem lists (LeetCode tags) for your top 2-3 targets
- 🎤 1 full mock + start behavioral story prep (STAR format, 8–10 stories)

## Week 10 — Simulation week
- Daily: 2 random unseen mediums, 60-minute block, no pauses — Meta-style
- Re-solve everything still in the shaky queue
- 🎤 2 mocks (at least one with a stranger, not a friend)
- Light review only on the 2 days before any real interview

---

## Company-specific tuning (your target list)

**Meta** — speed game: 2 mediums in ~40 min, minimal hints, heavy on arrays/strings/trees/graphs, light on DP. Week 10's timed-pairs drill is built for this.

**Google** — ambiguity + follow-ups: expect underspecified problems, graph/DP-heavy, and "now what if the input doesn't fit in memory?" extensions. Practice stating assumptions out loud.

**Amazon** — DSA is slightly easier (LC easy-medium) but Leadership Principles dominate; your behavioral stories matter as much as code. Budget real time for LP prep in Weeks 9–10.

**Microsoft / Apple / Nvidia** — standard LC mediums, conversational style; Apple teams vary wildly by org, check the specific team's reputation.

**Stripe** — ⚠ different beast: practical coding (string parsing, building a small ledger/API, integrating components), not algorithmic LC. If Stripe is high-priority, reserve 2–3 weekend sessions for "build a working thing in 45 min" practice instead of LC grinding.

**Atlassian / Salesforce / Workday-tier / PayPal / Twilio / MongoDB / CrowdStrike** — standard LC mediums, rarely hards; your ⭐ list more than covers them. Atlassian adds a values interview; prep 2–3 collaboration stories.

---

## Weekly rhythm (17 hrs)
- Mon–Thu: 2 new problems + 15 min reviewing yesterday's (2.5 hrs)
- Fri: 1 new + 2 re-solves from the shaky queue (2.5 hrs)
- Sat: longer session — pattern's hard problem, mock interview, or Stripe-style build (3–4 hrs)
- Sun: lighter — notes review, 1 problem, plan the week (1.5–2 hrs)

## Slip rule
Behind schedule? Cut in this order: non-⭐ problems → Week 9 bit/math day → never cut Graphs or DP weeks.

## Shaky-area tracker (live — we update as we go)
| Area | Self-assessed | Coach-observed | Status |
|---|---|---|---|
| Graphs | Shaky | — | Scheduled W5–6 |
| Dynamic Programming | Shaky | — | Scheduled W7–8 |
| Heaps / Backtracking / Design | Shaky | — | Scheduled W4, W6, W9 |
| Trees | OK? | unverified — W3 will confirm | |
| Arrays / Strings / LL | Strong | — | Verify with W1 timed drills |
