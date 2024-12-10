
# **First Fit Memory Allocation**

This repository contains the implementation of the **First Fit Memory Allocation Algorithm**, designed to simulate dynamic memory allocation in a simplified and efficient way. The project includes Python code, detailed documentation, flowcharts, and testing results.

---

## **Features**
- Simulates memory allocation using the **First Fit Algorithm**.
- Handles dynamic memory requests and releases efficiently.
- Provides visual flowcharts for better understanding.
- Detailed documentation explaining the algorithm, design, and implementation.

---

## **How It Works**
The **First Fit Algorithm** allocates the first available memory block that fits the requested process size.  
1. Memory blocks and process sizes are predefined or user-specified.  
2. The algorithm scans through the memory blocks sequentially to find a suitable block for each process.  
3. If a block is found:
   - It is allocated to the process.
   - The remaining space (if any) is updated in the block.  
4. If no block fits, the process is marked as unallocated.  

---

## **How to Run**
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/username/First-Fit-Memory-Allocation.git
   cd First-Fit-Memory-Allocation
   ```
2. **Run the Python Script**:
   ```bash
   python first_fit.py
   ```
3. **Input Data**:
   - You can modify the memory blocks and process sizes in the code or use the default values.

---

## **Project Structure**
```
# Memory blocks (sizes in KB)
memory_blocks = [100, 500, 200, 300, 600]

# Process sizes (in KB)
processes = [212, 417, 112, 426]

# Store allocation results
allocations = [-1] * len(processes)  # -1 means not allocated

# First Fit Algorithm Simulation
for i, process in enumerate(processes):
    for j, block in enumerate(memory_blocks):
        if process <= block:  # Check if the block can fit the process
            allocations[i] = j  # Assign the block index to the process
            memory_blocks[j] -= process  # Reduce the size of the block
            break  # Move to the next process

# Output Results
print("Process Allocation Results:")
for i, process in enumerate(processes):
    if allocations[i] != -1:
        print(f"Process {i + 1} ({process} KB) allocated to Block {allocations[i] + 1}")
    else:
        print(f"Process {i + 1} ({process} KB) could not be allocated")

print("\nFinal Memory Block Status:")
for i, block in enumerate(memory_blocks):
    print(f"Block {i + 1}: {block} KB remaining")

```
![First Fit Algorithm Flow Chart](https://github.com/Charakaja/First-Fit-Memory-Allocation/blob/main/First%20Fit%20Flow1.png?raw=true)
---

## **Output**
### **Input**:
- Memory Blocks: `[100, 500, 200, 300, 600]`
- Processes: `[212, 417, 112, 426]`

### **Output**:
```
Process Allocation Results:
Process 1 (212 KB) allocated to Block 2
Process 2 (417 KB) allocated to Block 5
Process 3 (112 KB) allocated to Block 2
Process 4 (426 KB) could not be allocated

Final Memory Block Status:
Block 1: 100 KB remaining
Block 2: 176 KB remaining
Block 3: 200 KB remaining
Block 4: 300 KB remaining
Block 5: 183 KB remaining.
```
---



## **License**
This project is open-source and licensed under the MIT License.

---

## **References**
1. [GeeksforGeeks - Memory Allocation Algorithms](https://www.geeksforgeeks.org/dynamic-memory-allocation-in-c-using-malloc-free/)
2. [Python Documentation](https://docs.python.org/)

