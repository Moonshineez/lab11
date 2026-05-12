1.реализация

```python
def insertion_sort(arr):
    for i in range(1, len(arr)):
        element = arr[i]
        j = i - 1
        while j >= 0 and arr[j] > element:
            arr[j + 1] = arr[j]
            j -= 1
        arr[j + 1] = element
    return arr
```

2.измерение времени

```python

import time
def measure_time(func, data):
    start = time.perf_counter()
    func(data.copy())
    end = time.perf_counter()
    return end - start
```

3.измерение памяти

```python

import tracemalloc
def measure_memory(func, data):
    tracemalloc.start()
    func(data.copy())
    current, peak = tracemalloc.get_traced_memory()
    tracemalloc.stop()
    return peak
```

4.генерация массива

```python

import random
def generate_array(n):
    arr = []
    for i in range(n):
        arr.append(random.randint(0, 10000))
    return arr
```

5.эксперименты

```python

if __name__ == '__main__':
    sizes = [100, 500, 1000, 5000]
    
    for n in sizes:
        arr = generate_array(n)
        t = measure_time(insertion_sort, arr)
        m = measure_memory(insertion_sort, arr)
        print(n, f"{t:.7f}", m)
```

|         n          |            t           |        m          |
|--------------------|------------------------|-------------------|
| 100                | 0.0003064              | 880 bytes         |
| 500                | 0.0083708              | 4140 bytes        |
| 1000               | 0.0340658              | 8396 bytes        |
| 5000               | 0.9046487              | 40396 bytes       |

