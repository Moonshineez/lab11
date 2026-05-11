1.реализация
```python

def find_max(arr):
    max1 = arr[0]
    max2 = arr[0]
    for i in arr:
        if i > max1:
            max2 = max1
            max1 = i
        elif i > max2 and i != max1:
            max2 = i
    return max2
```

3.измерение времени
```python
import time
def measure_time(func, data):
    start = time.perf_counter()
    func(data)
    end = time.perf_counter()
    return end - start
```
2.генерация массива
```python
import random
def generate_array(n):
    arr = []
    for i in range(n):
        arr.append(random.randint(0, 10000))
    return arr
```
4.Эксперименты
```python
if __name__ == '__main__':
    sizes = [100, 1000, 5000, 10000]
    
    for n in sizes:
        arr = generate_array(n)
        t = measure_time(find_max, arr)
        print(n, f"{t:.7f}")
```


