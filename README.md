# LRU Cache in Go

This is a simple implementation of a **fixed-size LRU (Least Recently Used) Cache** in Go using a combination of:

- **Hash Map** → for O(1) lookups  
- **Doubly Linked List** → for O(1) add/remove operations  

---

## 📌 How It Works
- When you **access (Check)** an item:
  - If it exists → move it to the front (most recently used).  
  - If not → create a new node and insert it at the front.  
- If the cache exceeds the **fixed size (`SIZE = 5`)**, the **least recently used** item is evicted (removed from the end of the list).  
