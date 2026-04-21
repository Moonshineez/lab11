import time
import random



def alg(m,a):
    for i in m:
        if a==i:
            return 1
    return 0

def generate_array(n):
    arr = []
    for i in range(n):
        arr.append(random.randint(0, 10000))
    return arr

def measure_time(func, data,a):
    start = time.perf_counter()
    func(data,a)
    end = time.perf_counter()
    return end - start

if __name__ == '__main__':
    sizes = [100, 500, 1000, 5000, 10000]
    
    for n in sizes:
        arr = generate_array(n)
        a = arr[0]
        t = measure_time(alg, arr, a)
        print(n, f"{t:.7f}")

