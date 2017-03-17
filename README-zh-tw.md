> * 原文地址：[github.com/kdn251/interviews](https://github.com/kdn251/interviews)
> * 譯文出自：[掘金翻譯計劃](https://github.com/xitu/gold-miner)
> * 譯者：[王下邀月熊](https://github.com/wxyyxc1992)
> * 校對者：[PhxNirvana](https://github.com/phxnirvana)、[根號三](https://github.com/sqrthree)
> * 繁中化：[阿翔](https://github.com/leo424y)
> * 這個 [連結](https://github.com/xitu/interviews/compare/master...kdn251:master) 用來檢視本翻譯與英文版是否有差別（如果你沒有看到 README.md 發生變化，那就意味著這份翻譯文件是最新的）。

# Interviews
> 軟體工程技術面試個人指南。
>
> Maintainer - [Kevin Naughton Jr.](https://github.com/kdn251)

## 其他語言版本

- [English](./README.md)

## 目錄
- [線上練習](#線上練習)
- [線上面試程式設計](#線上面試程式設計)
- [資料結構](#資料結構)
- [演算法](#演算法)
- [位運算](#位運算)
- [演算法複雜度分析](#演算法複雜度分析)
- [視訊教程](#視訊教程)
- [面試書籍](#面試書籍)
- [電腦科學與技術資訊](#電腦科學與技術資訊)
- [檔案結構](#檔案結構)

## 線上練習
* [LeetCode](https://leetcode.com/)
* [Virtual Judge](https://vjudge.net/)
* [CareerCup](https://www.careercup.com/)
* [HackerRank](https://www.hackerrank.com/)
* [CodeFights](https://codefights.com/)
* [Kattis](https://open.kattis.com/)
* [HackerEarth](https://www.hackerearth.com)

## 線上面試程式設計
* [Gainlo](http://www.gainlo.co/#!/)
* [Refdash](https://refdash.com/)

## 資料結構
### Linked List
 * 連結串列即是由節點（Node）組成的線性集合，每個節點可以利用指針指向其他節點。它是一種包含了多個節點的、能夠用於表示序列的資料結構。
 * **單向連結串列**: 連結串列中的節點僅指向下一個節點，並且最後一個節點指向空。
 * **雙向連結串列**: 其中每個節點具有兩個指針 p、n，使得 p 指向先前節點並且 n 指向下一個節點；最後一個節點的 n 指針指向 null。
 * **迴圈連結串列**：每個節點指向下一個節點並且最後一個節點指向第一個節點的連結串列。
 * 時間複雜度:
   * 索引: `O(n)`
   * 搜尋: `O(n)`
   * 插入: `O(1)`
   * 移除: `O(1)`

### Stack
 * 棧是元素的集合，其包含了兩個基本操作：push 操作可以用於將元素壓入棧，pop 操作可以將棧頂元素移除。
 * 遵循後入先出（LIFO）原則。
 * 時間複雜度:
  * 索引: `O(n)`
  * 搜尋: `O(n)`
  * 插入: `O(1)`
  * 移除: `O(1)`

### Queue
 * 佇列是元素的集合，其包含了兩個基本操作：enqueue 操作可以用於將元素插入到佇列中，而 dequeeu 操作則是將元素從佇列中移除。
 * 遵循先入先出原則 (FIFO)。
 * 時間複雜度:
  * 索引: `O(n)`
  * 搜尋: `O(n)`
  * 插入: `O(1)`
  * 移除: `O(1)`

### Tree
* 樹是無向、連通的無環圖。

### Binary Tree
 * 二叉樹即是每個節點最多包含左子節點與右子節點這兩個節點的樹形資料結構。
 * **滿二叉樹**: 樹中的每個節點僅包含 0 或 2 個節點。
 * **完美二叉樹（Perfect Binary Tree）**: 二叉樹中的每個葉節點都擁有兩個子節點，並且具有相同的高度。
 * **完全二叉樹**: 除最後一層外，每一層上的結點數均達到最大值；在最後一層上只缺少右邊的若干結點。

### Binary Search Tree

* 二叉搜尋樹（BST）是一種特殊的二叉樹，其任何節點中的值都會大於或者等於其左子樹中儲存的值並且小於或者等於其右子樹中儲存的值。
* 時間複雜度:
  * 索引: `O(log(n))`
  * 搜尋: `O(log(n))`
  * 插入: `O(log(n))`
  * 刪除: `O(log(n))`

<img src="/Images/BST.png?raw=true" alt="Binary Search Tree" width="400" height="500">

### Trie
* 字典樹，又稱基數樹或者字首樹，能夠用於儲存鍵為字元串的動態集合或者關聯陣列的搜尋樹。樹中的節點並沒有直接儲存關聯鍵值，而是該節點在樹中的掛載位置決定了其關聯鍵值。某個節點的所有子節點都擁有相同的字首，整棵樹的根節點則是空字元串。

![Alt text](/Images/trie.png?raw=true "Trie")

### Fenwick Tree
* 樹狀陣列又稱 Binary Indexed Tree，其表現形式為樹，不過本質上是以陣列實現。陣列中的下標代表著樹中的頂點，每個頂點的父節點或者子節點的下標能夠通過位運算獲得。陣列中的每個元素包含了預計算的區間值之和，在整棵樹更新的過程中同樣會更新這些預計算的值。
* 時間複雜度:
  * 區間求值: `O(log(n))`
  * 更新: `O(log(n))`

![Alt text](/Images/fenwickTree.png?raw=true "Fenwick Tree")

### Segment Tree
* 線段樹是用於存放間隔或者線段的樹形資料結構，它允許快速的查詢某一個節點在若干條線段中出現的次數.
* 時間複雜度:
  * 區間查詢: `O(log(n))`
  * 更新: `O(log(n))`

![Alt text](/Images/segmentTree.png?raw=true "Segment Tree")

### Heap
* 堆是一種特殊的基於樹的滿足某些特性的資料結構，整個堆中的所有父子節點的鍵值都會滿足相同的排序條件。堆更準確地可以分為最大堆與最小堆，在最大堆中，父節點的鍵值永遠大於或者等於子節點的值，並且整個堆中的最大值儲存於根節點；而最小堆中，父節點的鍵值永遠小於或者等於其子節點的鍵值，並且整個堆中的最小值儲存於根節點。
* 時間複雜度:
  * 訪問: `O(log(n))`
  * 搜尋: `O(log(n))`
  * 插入: `O(log(n))`
  * 移除: `O(log(n))`
  * 移除最大值 / 最小值: `O(1)`

<img src="/Images/heap.png?raw=true" alt="Max Heap" width="400" height="500">


### Hashing
* 雜湊能夠將任意長度的資料對映到固定長度的資料。雜湊函數返回的即是雜湊值，如果兩個不同的鍵得到相同的雜湊值，即將這種現象稱為碰撞。
* **Hash Map**: Hash Map 是一種能夠建立起鍵與值之間關係的資料結構，Hash Map 能夠使用雜湊函數將鍵轉化為桶或者槽中的下標，從而優化對於目標值的搜尋速度。
* 碰撞解決
  * **鏈地址法（Separate Chaining）**: 鏈地址法中，每個桶是相互獨立的，包含了一系列索引的列表。搜尋操作的時間複雜度即是搜尋桶的時間（固定時間）與遍歷列表的時間之和。
  * **開地址法（Open Addressing）**: 在開地址法中，當插入新值時，會判斷該值對應的雜湊桶是否存在，如果存在則根據某種演算法依次選擇下一個可能的位置，直到找到一個尚未被佔用的地址。所謂開地址法也是指某個元素的位置並不永遠由其雜湊值決定。

![Alt text](/Images/hash.png?raw=true "Hashing")

### Graph
* 圖是一種資料元素間為多對多關係的資料結構，加上一組基本操作構成的抽象資料類型。
    * **無向圖（Undirected Graph）**: 無向圖具有對稱的鄰接矩陣，因此如果存在某條從節點 u 到節點 v 的邊，反之從 v 到 u 的邊也存在。
    * **有向圖（Directed Graph）**: 有向圖的鄰接矩陣是非對稱的，即如果存在從 u 到 v 的邊並不意味著一定存在從 v 到 u 的邊。

<img src="/Images/graph.png?raw=true" alt="Graph" width="400" height="500">

## 演算法

### 排序

#### 快速排序
* 穩定: 否
* 時間複雜度:
  * 最優時間: `O(nlog(n))`
  * 最壞時間: `O(n^2)`
  * 平均時間: `O(nlog(n))`

![Alt text](/Images/quicksort.gif?raw=true "Quicksort")

#### 歸併排序
* 歸併排序是典型的分治演算法，它不斷地將某個陣列分為兩個部分，分別對左子陣列與右子陣列進行排序，然後將兩個陣列合併為新的有序陣列。
* 穩定: 是
* 時間複雜度:
  * 最優時間: `O(nlog(n))`
  * 最壞時間: `O(nlog(n))`
  * 平均時間: `O(nlog(n))`

![Alt text](/Images/mergesort.gif?raw=true "Mergesort")

#### 桶排序
* 桶排序將陣列分到有限數量的桶子裡。每個桶子再個別排序（有可能再使用別的排序演算法或是以遞迴方式繼續使用桶排序進行排序）。
* 時間複雜度:
  * 最優時間: `Ω(n + k)`
  * 最壞時間: `O(n^2)`
  * 平均時間:`Θ(n + k)`


![Alt text](/Images/bucketsort.png?raw=true "Bucket Sort")

#### 基數排序
* 基數排序類似於桶排序，將陣列分割到有限數目的桶中；不過其在分割之後並沒有讓每個桶單獨地進行排序，而是直接進行了合併操作。
* 時間複雜度:
  * 最優時間: `Ω(nk)`
  * 最壞時間: `O(nk)`
  * 平均時間: `Θ(nk)`

### 圖演算法

#### 深度優先搜尋
* 深度優先演算法是一種優先遍歷子節點而不是回溯的演算法。
* 時間複雜度: `O(|V| + |E|)`

![Alt text](/Images/dfsbfs.gif?raw=true "DFS / BFS Traversal")

#### 廣度優先搜尋
* 廣度優先搜尋是優先遍歷鄰居節點而不是子節點的圖遍歷演算法。
* 時間複雜度: `O(|V| + |E|)`

![Alt text](/Images/dfsbfs.gif?raw=true "DFS / BFS Traversal")

#### 拓撲排序
* 拓撲排序是對於有向圖節點的線性排序，如果存在某條從 u 到 v 的邊，則認為 u 的下標先於 v。
* 時間複雜度: `O(|V| + |E|)`

#### Dijkstra 演算法
* **Dijkstra 演算法** 用於計算有向圖中單源最短路徑問題。
* 時間複雜度: `O(|V|^2)`

![Alt text](/Images/dijkstra.gif?raw=true "Dijkstra's")

#### Bellman-Ford 演算法
* **Bellman-Ford 演算法**是在帶權圖中計算從單一源點出發到其他節點的最短路徑的演算法。
* 儘管演算法複雜度大於 Dijkstra 演算法，但是它適用於包含了負值邊的圖。
* 時間複雜度:
  * 最優時間: `O(|E|)`
  - 最壞時間: `O(|V||E|)`

![Alt text](/Images/bellman-ford.gif?raw=true "Bellman-Ford")

#### Floyd-Warshall 演算法
* **Floyd-Warshall 演算法** 能夠用於在無環帶權圖中尋找任意節點的最短路徑。
* 時間複雜度:
  * 最優時間: `O(|V|^3)`
  * 最壞時間: `O(|V|^3)`
  * 平均時間: `O(|V|^3)`

#### Prim 演算法
* **Prim 演算法**是用於在帶權無向圖中計算最小生成樹的貪婪演算法。換言之，Prim 演算法能夠在圖中抽取出連線所有節點的邊的最小代價子集。
* 時間複雜度: `O(|V|^2)`

![Alt text](/Images/prim.gif?raw=true "Prim's Algorithm")

#### Kruskal 演算法
* **Kruskal 演算法**同樣是計算圖的最小生成樹的演算法，與 Prim 的區別在於並不需要圖是連通的。
* 時間複雜度: `O(|E|log|V|)`

![Alt text](/Images/kruskal.gif?raw=true "Kruskal's Algorithm")

## 位運算
* 位運算即是在位級別進行操作的技術，合適的位運算能夠幫助我們得到更快地運算速度與更小的記憶體使用。
* 測試第 k 位: `s & (1 << k)`
* 設定第 k 位: `s |= (1 << k)`
* 第 k 位置零: `s &= ~(1 << k)`
* 切換第 k 位值: `s ^= ~(1 << k)`
* 乘以 2: `s << n`
* 除以 2: `s >> n`
* 交集: `s & t`
* 並集: `s | t`
* 減法: `s & ~t`
* 交換 `x = x ^ y ^ (y = x)`
* 取出最小非 0 位（Extract lowest set bit）: `s & (-s)`
* 取出最小 0 位（Extract lowest unset bit）: `~s & (s + 1)`
* 交換值:
             ```
                x ^= y;
                y ^= x;
                x ^= y;
             ```

## 演算法複雜度分析

#### 大 O 表示
* **大 O 表示** 用於表示某個演算法的上限，往往用於描述最壞的情況。

![Alt text](/Images/bigO.png?raw=true "Theta Notation")

#### 小 O 表示
* **小 O 表示**用於描述某個演算法的漸進上界，不過二者要更為緊密。

#### 大 Ω 表示
* **大 Ω 表示**用於描述某個演算法的漸進下界。

![Alt text](/Images/bigOmega.png?raw=true "Theta Notation")

#### 小 ω 表示
* **Little Omega Notation**用於描述某個特定演算法的下界，不過不一定很靠近。

#### Theta Θ 表示
* **Theta Notation**用於描述某個確定演算法的確界。

![Alt text](/Images/theta.png?raw=true "Theta Notation")

## 視訊教程
* Data Structures
 * [UC Berkeley Data Structures](https://www.youtube.com/watch?v=mFPmKGIrQs4&index=1&list=PL-XXv-cvA_iAlnI-BQr9hjqADPBtujFJd)
 * [MIT Advanced Data Structures](https://www.youtube.com/watch?v=T0yzrZL1py0&list=PLUl4u3cNGP61hsJNdULdudlRL493b-XZf&index=1)
* Algorithms
 * [MIT Introduction to Algorithms](https://www.youtube.com/watch?v=HtSuA80QTyo&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=1)
 * [MIT Advanced Algorithms](https://www.youtube.com/playlist?list=PL6ogFv-ieghdoGKGg2Bik3Gl1glBTEu8c)

## 面試書籍
* Competitive Programming 3 - Steven Halim & Felix Halim
* Cracking The Coding Interview - Gayle Laakmann McDowell
* Cracking The PM Interview - Gayle Laakmann McDowell & Jackie Bavaro

## 電腦科學與技術資訊
* [Hacker News](https://news.ycombinator.com/)

## 檔案結構

```
.
├── Array
│   ├── bestTimeToBuyAndSellStock.java
│   ├── findTheCelebrity.java
│   ├── gameOfLife.java
│   ├── increasingTripletSubsequence.java
│   ├── insertInterval.java
│   ├── longestConsecutiveSequence.java
│   ├── maximumProductSubarray.java
│   ├── maximumSubarray.java
│   ├── mergeIntervals.java
│   ├── missingRanges.java
│   ├── productOfArrayExceptSelf.java
│   ├── rotateImage.java
│   ├── searchInRotatedSortedArray.java
│   ├── spiralMatrixII.java
│   ├── subsetsII.java
│   ├── subsets.java
│   ├── summaryRanges.java
│   ├── wiggleSort.java
│   └── wordSearch.java
├── Backtracking
│   ├── androidUnlockPatterns.java
│   ├── generalizedAbbreviation.java
│   └── letterCombinationsOfAPhoneNumber.java
├── BinarySearch
│   ├── closestBinarySearchTreeValue.java
│   ├── firstBadVersion.java
│   ├── guessNumberHigherOrLower.java
│   ├── pow(x,n).java
│   └── sqrt(x).java
├── BitManipulation
│   ├── binaryWatch.java
│   ├── countingBits.java
│   ├── hammingDistance.java
│   ├── maximumProductOfWordLengths.java
│   ├── numberOf1Bits.java
│   ├── sumOfTwoIntegers.java
│   └── utf-8Validation.java
├── BreadthFirstSearch
│   ├── binaryTreeLevelOrderTraversal.java
│   ├── cloneGraph.java
│   ├── pacificAtlanticWaterFlow.java
│   ├── removeInvalidParentheses.java
│   ├── shortestDistanceFromAllBuildings.java
│   ├── symmetricTree.java
│   └── wallsAndGates.java
├── DepthFirstSearch
│   ├── balancedBinaryTree.java
│   ├── battleshipsInABoard.java
│   ├── convertSortedArrayToBinarySearchTree.java
│   ├── maximumDepthOfABinaryTree.java
│   ├── numberOfIslands.java
│   ├── populatingNextRightPointersInEachNode.java
│   └── sameTree.java
├── Design
│   └── zigzagIterator.java
├── DivideAndConquer
│   ├── expressionAddOperators.java
│   └── kthLargestElementInAnArray.java
├── DynamicProgramming
│   ├── bombEnemy.java
│   ├── climbingStairs.java
│   ├── combinationSumIV.java
│   ├── countingBits.java
│   ├── editDistance.java
│   ├── houseRobber.java
│   ├── paintFence.java
│   ├── paintHouseII.java
│   ├── regularExpressionMatching.java
│   ├── sentenceScreenFitting.java
│   ├── uniqueBinarySearchTrees.java
│   └── wordBreak.java
├── HashTable
│   ├── binaryTreeVerticalOrderTraversal.java
│   ├── findTheDifference.java
│   ├── groupAnagrams.java
│   ├── groupShiftedStrings.java
│   ├── islandPerimeter.java
│   ├── loggerRateLimiter.java
│   ├── maximumSizeSubarraySumEqualsK.java
│   ├── minimumWindowSubstring.java
│   ├── sparseMatrixMultiplication.java
│   ├── strobogrammaticNumber.java
│   ├── twoSum.java
│   └── uniqueWordAbbreviation.java
├── LinkedList
│   ├── addTwoNumbers.java
│   ├── deleteNodeInALinkedList.java
│   ├── mergeKSortedLists.java
│   ├── palindromeLinkedList.java
│   ├── plusOneLinkedList.java
│   ├── README.md
│   └── reverseLinkedList.java
├── Queue
│   └── movingAverageFromDataStream.java
├── README.md
├── Sort
│   ├── meetingRoomsII.java
│   └── meetingRooms.java
├── Stack
│   ├── binarySearchTreeIterator.java
│   ├── decodeString.java
│   ├── flattenNestedListIterator.java
│   └── trappingRainWater.java
├── String
│   ├── addBinary.java
│   ├── countAndSay.java
│   ├── decodeWays.java
│   ├── editDistance.java
│   ├── integerToEnglishWords.java
│   ├── longestPalindrome.java
│   ├── longestSubstringWithAtMostKDistinctCharacters.java
│   ├── minimumWindowSubstring.java
│   ├── multiplyString.java
│   ├── oneEditDistance.java
│   ├── palindromePermutation.java
│   ├── README.md
│   ├── reverseVowelsOfAString.java
│   ├── romanToInteger.java
│   ├── validPalindrome.java
│   └── validParentheses.java
├── Tree
│   ├── binaryTreeMaximumPathSum.java
│   ├── binaryTreePaths.java
│   ├── inorderSuccessorInBST.java
│   ├── invertBinaryTree.java
│   ├── lowestCommonAncestorOfABinaryTree.java
│   ├── sumOfLeftLeaves.java
│   └── validateBinarySearchTree.java
├── Trie
│   ├── addAndSearchWordDataStructureDesign.java
│   ├── implementTrie.java
│   └── wordSquares.java
└── TwoPointers
    ├── 3Sum.java
    ├── 3SumSmaller.java
    ├── mergeSortedArray.java
    ├── minimumSizeSubarraySum.java
    ├── moveZeros.java
    ├── removeDuplicatesFromSortedArray.java
    ├── reverseString.java
    └── sortColors.java

18 directories, 124 files
```
