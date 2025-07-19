# **Complete CUET M.Sc. (CSE) Question Bank with Answers**

## **1. Data Structures & Algorithms**
### **Q1. Define O(n log n) with example**
**Answer:**  
O(n log n) describes algorithms where runtime grows proportionally to the input size (n) multiplied by its logarithm.  
**Example:** Merge Sort, Heap Sort.

### **Q2. Bubble Sort Program**
```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
```
**Time Complexity:** O(n²) in worst case.

### **Q3. Hash Table & Collision**
**Answer:**  
A hash table stores key-value pairs using a hash function.  
**Collision Resolution Methods:**  
- Chaining (linked lists at each bucket)  
- Open Addressing (probing to find empty slots)

### **Q4. BFS vs DFS**
| **BFS** | **DFS** |
|---------|---------|
| Uses queue | Uses stack |
| Level-order traversal | Depth-wise traversal |
| Finds shortest path | Uses less memory |

### **Q5. Priority Queue vs Normal Queue**
**Priority Queue:** Elements dequeued based on priority (implemented with heaps).  
**Normal Queue:** FIFO (First-In-First-Out) order.

---

## **2. Operating Systems**
### **Q6. Deadlock & Conditions**
**Deadlock:** When processes block each other permanently.  
**Conditions:**  
1. Mutual Exclusion  
2. Hold and Wait  
3. No Preemption  
4. Circular Wait

### **Q7. Mutex vs Semaphore**
**Mutex:** Binary lock (0/1) for critical sections.  
**Semaphore:** Counter for multiple threads (can be counting semaphore).

### **Q8. Virtual Memory & Paging**
**Virtual Memory:** Uses disk as extended RAM.  
**Paging:** Divides memory into fixed-size pages (avoids external fragmentation).

### **Q9. Thrashing**
**Answer:** Excessive page faults occur when processes spend more time paging than executing due to insufficient memory.

### **Q10. Race Condition Prevention**
**Methods:**  
- Mutex locks  
- Semaphores  
- Atomic operations

---

## **3. Database Management Systems**
### **Q11. Normalization (1NF-3NF)**
**1NF:** All attributes atomic (no repeating groups).  
**2NF:** No partial dependencies (all non-keys depend on full primary key).  
**3NF:** No transitive dependencies (non-key attributes depend only on keys).

### **Q12. Indexing & B-Trees**
**Indexing:** Speeds up queries by creating lookup structures.  
**B-Tree:** Balanced tree where each node contains multiple keys (used in databases).

### **Q13. SQL vs NoSQL**
| **SQL** | **NoSQL** |
|---------|----------|
| Relational tables | Document/Key-Value stores |
| ACID compliant | BASE model (flexible) |
| Example: MySQL | Example: MongoDB |

### **Q14. Transaction Log**
**Purpose:** Records all transactions for recovery (used in rollback/rollforward).

### **Q15. SQL Query for 2nd Highest Salary**
```sql
SELECT MAX(salary) FROM Employee 
WHERE salary < (SELECT MAX(salary) FROM Employee);
```

---

## **4. Computer Networks**
### **Q16. TCP vs UDP**
| **TCP** | **UDP** |
|---------|---------|
| Reliable, connection-oriented | Unreliable, connectionless |
| Flow control, congestion control | No guarantees |
| HTTP, FTP | DNS, Video Streaming |

### **Q17. OSI Model Layers**
1. Physical (bits)  
2. Data Link (frames)  
3. Network (packets)  
4. Transport (segments)  
5. Session  
6. Presentation  
7. Application

### **Q18. DNS Spoofing**
**How it works:** Attacker corrupts DNS cache to redirect domains to malicious IPs.

### **Q19. Firewall Protection**
**Methods:**  
- Packet filtering  
- Stateful inspection  
- Proxy service

### **Q20. Phishing Detection**
1. Check sender email authenticity  
2. Hover over links to verify URLs  
3. Look for grammatical errors  

---

## **5. Software Engineering**
### **Q21. Scrum vs Kanban**
| **Scrum** | **Kanban** |
|-----------|------------|
| Fixed-length sprints | Continuous flow |
| Roles: Scrum Master | No fixed roles |
| Burn-down charts | WIP limits |

### **Q22. V-Model**
**Concept:** Verification and validation phases mirror each other (extension of Waterfall).

### **Q23. User Stories**
**Format:** "As a [user], I want [feature] so that [benefit]."

### **Q24. Git Branching**
**Common Strategies:**  
- Feature branches  
- Git Flow  
- Trunk-Based Development

### **Q25. CI/CD**
**CI:** Automates code integration/testing.  
**CD:** Automates deployment to production.

---

## **6. Machine Learning**
### **Q26. Bias-Variance Tradeoff**
**High Bias:** Underfitting (oversimplified model).  
**High Variance:** Overfitting (model memorizes training data).

### **Q27. k-NN Algorithm**
**Concept:** Classifies points based on majority vote of nearest neighbors.

### **Q28. Gradient Descent**
**Purpose:** Optimizes model parameters by minimizing loss function.

### **Q29. Confusion Matrix Metrics**
- Precision = TP / (TP + FP)  
- Recall = TP / (TP + FN)  
- F1-score = 2 * (Precision * Recall) / (Precision + Recall)

### **Q30. Decision Trees**
**Advantages:**  
- Handles non-linear data  
- Interpretable  
- No feature scaling needed

---

## **7. Programming**
### **Q31. Palindrome Check**
```python
def is_palindrome(s):
    return s == s[::-1]
```

### **Q32. Recursion (Fibonacci)**
```python
def fib(n):
    return n if n <= 1 else fib(n-1) + fib(n-2)
```

### **Q33. DP: Coin Change**
```python
def coin_change(coins, amount):
    dp = [float('inf')] * (amount + 1)
    dp[0] = 0
    for coin in coins:
        for x in range(coin, amount + 1):
            dp[x] = min(dp[x], dp[x - coin] + 1)
    return dp[amount] if dp[amount] != float('inf') else -1
```

### **Q34. GCD (Euclidean)**
```python
def gcd(a, b):
    return a if b == 0 else gcd(b, a % b)
```

### **Q35. Lambda Function**
```python
square = lambda x: x ** 2  # Example usage: square(5) → 25
```

---

## **8. System Design**
### **Q36. URL Shortener Design**
1. **Hashing:** Convert long URL to 6-char code (Base62 encoding).  
2. **DB:** Store mappings (code → original URL).  
3. **Cache:** Use Redis for hot URLs.

### **Q37. Load Balancing**
**Round Robin:** Distributes requests sequentially.  
**Least Connections:** Sends to server with fewest active connections.

### **Q38. Caching (Redis)**
**Benefits:** Reduces database load, speeds up read operations.

### **Q39. Microservices vs Monolith**
**Microservices:** Independent, scalable components.  
**Monolith:** Single codebase (harder to scale).

### **Q40. Fault Tolerance**
**Methods:**  
- Redundancy  
- Circuit breakers  
- Retry mechanisms

---

## **9. Computer Architecture**
### **Q41. RISC vs CISC**
| **RISC** | **CISC** |
|----------|----------|
| Simple instructions | Complex instructions |
| Fixed-length ops | Variable-length ops |
| ARM, MIPS | x86 |

### **Q42. Pipelining**
**Concept:** Overlaps instruction execution stages to improve throughput.

### **Q43. 4-Bit Adder**
**Logic:** Uses Full Adders chained together (carry propagates).

### **Q44. Cache Hierarchy**
**L1:** Fastest, smallest (CPU core).  
**L2/L3:** Larger, slower (shared between cores).

### **Q45. Virtual Memory**
**Purpose:** Allows running large programs by swapping pages to disk.

---

## **10. Shell Scripting**
### **Q46. Find Files >1MB**
```bash
find /path -type f -size +1M
```

### **Q47. grep Example**
```bash
grep "error" logfile.txt  # Searches for "error" in file
```

### **Q48. File Permissions**
```bash
chmod 755 script.sh  # Sets rwxr-xr-x
chown user:group file  # Changes ownership
```

### **Q49. Cron Job**
```bash
0 17 * * * /path/to/script.sh  # Runs daily at 5 PM
```

### **Q50. kill vs kill -9**
**kill:** Graceful termination (allows cleanup).  
**kill -9:** Forceful termination (SIGKILL).
