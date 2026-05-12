1.реализация

```python
def multiplication_table(n):
    a = [[0] * n for i in range(n)]
    for i in range(1, n + 1):
        b = a[i - 1]
        for j in range(1, n + 1):
            b[j - 1] = i * j
    return a
```

2.измерение времени

```python
import time
def measure_time(func, n):
    start = time.perf_counter()
    func(n)
    end = time.perf_counter()
    return end - start
```

3.эксперименты

```python
if __name__ == '__main__':
    sizes = [100, 500, 1000, 5000]
    
    for n in sizes:
        t = measure_time(multiplication_table, n)
        print(n, f"{t:.7f}")
```

|         n          |            t           |
|--------------------|------------------------|
| 100                | 0.0012710              |
| 500                | 0.0338093              |
| 1000               | 0.1156807              |
| 5000               | 2.9987023              |
