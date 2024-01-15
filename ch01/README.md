# Managing Data Integrity for Finance

<a href="https://www.packtpub.com/product/managing-data-integrity-for-finance/9781837630141"><img src="https://content.packt.com/B19758/cover_image_small.jpg" alt="Book Name" height="120px" align="left" style="margin: 0px 15px; border-color: white; border-style: solid; border-width: 1px;"></a>

**Chapter 1: Recognizing the Importance of Data Integrity in Finance** <br />
This chapter gives the reader a quick overview of the concepts relevant to the succeeding chapters in the book.

<br />
<br />
<br />
<br />
<br />

## Links and Files

- https://en.wikipedia.org/wiki/Levenshtein_distance
- https://www.investopedia.com/terms/r/restatement.asp
- https://www.online-python.com/
- https://en.wikipedia.org/wiki/Lock_(computer_science)
- https://en.wikipedia.org/wiki/Floating-point_arithmetic

<br />

## Code blocks specific to the chapter

#### Mutual exclusion (without mutex lock)
```
import threading
counter = 0
 
def increment_counter():
    global counter
    for _ in range(100000):
        counter += 1
 
threads = []
for i in range(10):
    thread = threading.Thread(target=increment_counter)
    threads.append(thread)
    thread.start()
 
for thread in threads:
    thread.join()
 
print(f"Final counter value without mutex: {counter}")
```

#### Mutual exclusion (with mutex lock)
```
import threading
counter = 0
counter_lock = threading.Lock()
 
def increment_counter():
    global counter
    for _ in range(100000):
        with counter_lock:
            counter += 1
 
threads = []
for i in range(10):
    thread = threading.Thread(target=increment_counter)
    threads.append(thread)
    thread.start()
 
for thread in threads:
    thread.join()
 
print(f"Final counter value with mutex: {counter}")
```

#### Floating-point number
```
principal = 1000
rate = 0.001 # 0.1%
time = 1/365
interest_float = principal * rate * time
interest_float
```

#### Decimal data type
```
from decimal import Decimal
principal = Decimal('1000')
rate = Decimal('0.001') # 0.1%
time = Decimal('1') / Decimal('365')
interest_decimal = principal * rate * time
interest_decimal
```
