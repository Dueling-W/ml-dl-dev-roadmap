# Lists vs. Tuples

**To view markdown in VSCode use: Ctrl + Shift + V**

## Notes Summary
- Investigate differences between lists and tuples
- Gain a deeper understanding of how Python handles lists and tuples in memory
- Resources Used:
    - [ChatGPT conversation](https://chatgpt.com/share/68e015ed-e078-800c-915a-4244769b2dcd)
    - [Stack Overflow discussion](https://stackoverflow.com/questions/46664007/why-do-tuples-take-less-space-in-memory-than-lists)

## How Do Lists and Tuples Work?
- A list is declared as follows:
``` python
a = [1, 2, 3]
```
- So there are two parts, the name and the list contents
- The name, a in this case, holds a pointer to a PyObject, it doesn't contain the list itself
- The PyObject, what the pointer points to, is the actual **list object**
- The interal structure might look something like this: 
``` vbnet
a ──▶ [ PyListObject ]
           ├── ob_refcnt
           ├── ob_type
           ├── ob_size = 3
           └── ob_item ──▶ [ ptr to 10, ptr to 20, ptr to 30 ]
```
- So there is actually a pointer for each element in the list
- This means that when you do:
``` python
a = [1, 2, 3]
b = a
b[0] = 5
print(a)
```
- It will output: [5, 2, 3], since when you say b = a, that just means there are two pointers to the same PyListObject
- The **ob_refcnt** field would also be updated to 2
---
**Tuples**
- Tuples have a similar structure, declared below:
``` python
c = (1, 2, 3)
```
- Just like with lists, the variable c is just a pointer to the object itself
- Except, the items are in the header directly, as in, the items are there along with PyTupleObject, instead of separate like with lists
- This is known as including the array of pointers "inline"
- This makes them slightly faster at getting your items and easier to delete, since everything is grouped together

## Immutable vs. Mutable
- In Python, lists over-allocate, meaning extra unused slots
    - This is necessary to make appending elements O(1) time, because if there weren't extra slots, ```realloc``` would have to copy all pointers to a new array, taking O(n) time
- So when you run out of space in the list, Python adds more than you actually need, and updates the pointer
- Tuples on the other hand are created with exactly enough size for the object header plus an array of pointers
- This doesn't mean the memory is read-only, it is that the **Python API** never provides anyway to resize or reassign elements
- The overallocation of lists can be shown below, thanks to a Stack Overflow answer:
``` python
l = [1,2,3]
l.__sizeof__()   # 64 bytes

l.append(4)
l.__sizeof__()   # 96 bytes
```
- In that case, overallocation kicked in, adding 32 bytes, likely space enough for 8 more elements, but it depends partially on the platform
- A overview table is shown below
---


# Python Lists vs Tuples (CPython implementation details)

| Aspect                  | List (`list`)                                                                 | Tuple (`tuple`)                                                                 |
|--------------------------|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| **Mutability**           | Mutable (can add, remove, reassign elements)                                  | Immutable (no API to modify after creation)                                     |
| **Memory layout**        | `PyListObject` + pointer (`ob_item`) to a separately allocated array of refs | `PyTupleObject` with element pointers stored **inline** after the header        |
| **Allocation strategy**  | Over-allocates (amortized O(1) append); grows by ~12.5% + constant            | Fixed size; allocates exactly enough space for N elements                       |
| **Resizing**             | Supports `append`, `extend`, `insert`, `pop`, etc.                           | Cannot resize; must create a new tuple                                          |
| **Access speed**         | Slight indirection (via `ob_item` pointer)                                    | Slightly faster (direct offset from header)                                     |
| **Cache locality**       | Elements may move in memory after reallocations                               | Contiguous header + element pointers = better locality                          |
| **Deallocation**         | Must free both the `PyListObject` and the `ob_item` array                     | Single free call (header + elements freed together)                             |
| **Use cases**            | Dynamic sequences, frequent mutation                                          | Fixed collections, dict keys, function arguments, lightweight read-only storage |
| **Overhead (`__sizeof__`)** | Includes room for extra slots when over-allocated                          | Exactly proportional to number of elements                                      |
| **Reference counting**   | Increases/decreases with new names/refs; freed when `ob_refcnt == 0`          | Same behavior (both are standard PyObjects)                                     |




