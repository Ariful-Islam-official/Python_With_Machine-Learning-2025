## **1. Define O(1). Mention one algorithm which follows O(1).**  
### **English:**  
- **O(1)** means **constant time complexity**. The algorithm takes the same time to execute, regardless of input size.  
- **Example**: Accessing an array element by index (`arr[5]`).  

### **Bangla:**  
- **O(1)** হলো **ধ্রুব সময় কমপ্লেক্সিটি**। ইনপুট সাইজ যাই হোক, এক্সিকিউশন সময় একই থাকে।  
- **উদাহরণ**: অ্যারের একটি এলিমেন্ট ইনডেক্স দিয়ে অ্যাক্সেস করা (`arr[5]`)।  

---

## **2. Compare Fishbone Model vs. Waterfall Model**  
### **English:**  
| **Fishbone Model (Ishikawa)** | **Waterfall Model** |  
|-------------------------------|---------------------|  
| Used for **root cause analysis** (e.g., defects in manufacturing). | A **linear SDLC model** with sequential phases. |  
| Visualizes causes of a problem (like a fish skeleton). | Phases: Requirements → Design → Implementation → Testing → Maintenance. |  
| Flexible, non-linear. | Rigid, no going back to previous phases. |  

### **Bangla:**  
- **ফিশবোন মডেল**: সমস্যার মূল কারণ বিশ্লেষণ করে (যেমন: উৎপাদনে ত্রুটি)।  
- **ওয়াটারফল মডেল**: সিকোয়েনশিয়াল সফটওয়্যার ডেভেলপমেন্ট মডেল (ফিজ একের পর এক)।  

---

## **3. Detecting Malware in a Suspicious Email (Without Clicking)**  
### **English:**  
1. **Check Sender’s Email**: Look for misspellings (e.g., `support@bankk.com`).  
2. **Hover Over Link**: Preview URL (e.g., shows `malware.com` instead of `bank.com`).  
3. **Attachments**: Avoid `.exe`, `.zip` files.  
4. **Grammar Errors**: Poor English = red flag.  

### **Bangla:**  
1. **প্রেরকের ইমেইল চেক করুন**: ভুল স্পেলিং দেখুন (যেমন: `support@bankk.com`)।  
2. **লিঙ্কে হোভার করুন**: আসল URL চেক করুন।  
3. **অ্যাটাচমেন্ট**: `.exe`, `.zip` ফাইল এড়িয়ে চলুন।  

---

## **4. Role of Semaphores in Synchronization**  
### **English:**  
- **Semaphore** is a **variable** used to control access to shared resources in multithreading.  
- **Types**:  
  - **Binary (0/1)**: Like a mutex lock.  
  - **Counting**: Allows multiple threads.  

### **Bangla:**  
- **সেমাফোর** হলো একটি ভেরিয়েবল যা মাল্টিথ্রেডিংয়ে শেয়ার্ড রিসোর্স এক্সেস কন্ট্রোল করে।  

---

## **5. ACID Properties in Database Transactions**  
### **English:**  
| **Property** | **Description** |  
|--------------|----------------|  
| **Atomicity** | All operations succeed or fail together. |  
| **Consistency** | Data remains valid before/after transaction. |  
| **Isolation** | Concurrent transactions don’t interfere. |  
| **Durability** | Committed data persists after crashes. |  

### **Bangla:**  
- **Atomicity**: সব অপারেশন একসাথে হয় বা বাতিল হয়।  
- **Consistency**: ডাটা ট্রানজেকশনের আগে ও পরে বৈধ থাকে।  

---

## **6. Agile vs. Waterfall**  
### **English:**  
| **Agile** | **Waterfall** |  
|-----------|---------------|  
| Iterative, flexible. | Linear, rigid. |  
| Client feedback at each sprint. | No feedback until end. |  

### **Bangla:**  
- **এজাইল**: ধাপে ধাপে কাজ, ক্লায়েন্ট ফিডব্যাক নেয়া হয়।  
- **ওয়াটারফল**: একবারে পুরো প্রজেক্ট শেষ করে দেখানো হয়।  

---

## **7. Neural Networks & Backpropagation**  
### **English:**  
- **Neural Network**: Mimics human brain (input → hidden layers → output).  
- **Backpropagation**: Adjusts weights using gradient descent to minimize error.  

### **Bangla:**  
- **নিউরাল নেটওয়ার্ক**: মানুষের মস্তিষ্কের মতো কাজ করে।  
- **ব্যাকপ্রোপাগেশন**: ভুল কমাতে নেটওয়ার্কের ওয়েট আপডেট করে।  

---

## **8. Program to Reverse a Linked List**  
```python  
class Node:  
    def __init__(self, data):  
        self.data = data  
        self.next = None  

def reverse_list(head):  
    prev = None  
    current = head  
    while current:  
        next_node = current.next  
        current.next = prev  
        prev = current  
        current = next_node  
    return prev  
```  

---

## **9. `sizeof()` vs. `len()`**  
- **`sizeof()`** (C): Returns memory size in bytes.  
- **`len()`** (Python): Returns number of items in a list.  

---

## **10. Merge Sort vs. Quick Sort**  
- **Merge Sort**:  
  - **Time**: O(n log n) (always).  
  - **Space**: O(n) (extra memory).  
- **Quick Sort**:  
  - **Time**: O(n log n) avg., O(n²) worst-case.  
  - **Space**: O(log n) (in-place).  

---

## **11. Greedy vs. Dynamic Programming**  
| **Greedy** | **DP** |  
|------------|--------|  
| Chooses locally optimal solution. | Solves subproblems, stores results. |  
| Example: Dijkstra’s Algorithm. | Example: Fibonacci Series. |  

---

## **12. Expression vs. Statement in C**  
- **Expression**: Evaluates to a value (e.g., `x + 5`).  
- **Statement**: Performs an action (e.g., `if (x > 5) { ... }`).  

---

## **13. Leap Year Check Program**  
```python  
def is_leap(year):  
    return (year % 400 == 0) or (year % 100 != 0 and year % 4 == 0)  
```  

---

## **14. IP Addressing & Subnetting**  
Given IP: `192.168.1.0/24`  
- **Subnets**: 256 (if /24).  
- **Broadcast**: `192.168.1.255`.  

---

## **15. Overfitting in ML: Solutions**  
- **Regularization (L1/L2)**: Penalizes complex models.  
- **Cross-Validation**: Splits data to test generalization.  

---

## **16. Real-Time Flight Control System**  
- **Priority Scheduling**: Critical signals get highest priority.  
- **Load Shedding**: Discard non-critical tasks during overload.  

---

## **17. Multiway Tree vs. B-Tree**  
- **Multiway Tree**: General tree with >2 children.  
- **B-Tree**: Balanced, used in databases for efficient disk access.  

---

## **18. Bucket Sort & Radix Sort**  
- **Bucket Sort**: Divides data into buckets, sorts individually.  
- **Radix Sort**: Sorts digit by digit (LSD/MSD).  

---

## **19. Job Scheduling Problem**  
- **Goal**: Maximize jobs completed before deadlines.  
- **Algorithm**: Greedy (earliest deadline first).  

---

### **Final Notes**  
- **For ETE Students**: Focus on **practical examples** (e.g., IP addressing for networking, sorting for data analysis).  
- **Bangla Translations**: Simplified for better understanding. 
