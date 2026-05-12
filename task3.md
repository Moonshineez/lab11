1.реализация

```python
def binary_search(arr, element):
    l = 0
    r = len(arr) - 1
    
    while l <= r:
        mid = (l + r) // 2
        
        if arr[mid] == element:
            return True
        elif arr[mid] < element:
            l = mid + 1
        else:
            r = mid - 1
    return False
```

2.измерение времени

```python
import time
def measure_time(func, data, element):
    start = time.perf_counter()
    func(data, element)
    end = time.perf_counter()
    return end - start
```

3.генерация массива

```python
import random
def generate_array(n):
    arr = []
    for i in range(n):
        arr.append(random.randint(0, 10000))
    arr.sort()
    return arr
```

4.Эксперименты

```python
if __name__ == '__main__':
    sizes = [100, 1000, 5000, 10000]
    
    for n in sizes:
        arr = generate_array(n)
        element = arr[n // 2]
        t = measure_time(binary_search, arr, element)
        print(n, f"{t:.7f}")
```

|         n          |            t           |
|--------------------|------------------------|
| 100                | 0.0000026              |
| 1000               | 0.0000040              |
| 5000               | 0.0000061              |
| 10000              | 0.0000277               |


        

