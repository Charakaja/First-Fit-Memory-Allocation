# First-Fit-Memory-Allocation
Implementation of the First Fit Memory Allocation algorithm in Python.
Here's a sample **README.md** file for your **First Fit Memory Allocation** project:

---

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
├── first_fit.py          # Python script for the First Fit Algorithm
├── README.md             # Project information and instructions
├── flowchart.png         # Flowchart illustrating the algorithm
├── documentation/
│   ├── report.pdf        # Detailed report of the project
│   ├── testing_results/  # Folder containing testing screenshots
```

---

## **Example Output**
### **Input**:
- Memory Blocks: `[50, 200, 150, 300, 100]`
- Processes: `[100, 10, 300, 200]`

### **Output**:
```
Process 1 allocated in Block 2
Process 2 allocated in Block 1
Process 3 allocated in Block 4
Process 4 not allocated
Remaining Memory: [50, 100, 150, 0, 100]
```

---

## **Technologies Used**
- **Programming Language**: Python
- **Tools**: Visual Studio Code, PyCharm
- **Testing Framework**: Manual and automated test cases

---

## **Contributions**
Contributions are welcome! Feel free to fork the repository, make changes, and submit a pull request.

---

## **License**
This project is open-source and licensed under the MIT License.

---

## **References**
1. [GeeksforGeeks - Memory Allocation Algorithms](https://www.geeksforgeeks.org/dynamic-memory-allocation-in-c-using-malloc-free/)
2. [Python Documentation](https://docs.python.org/)

