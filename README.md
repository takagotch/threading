### threading
---
https://docs.python.org/3/library/threading.html

```py
mydata = threading.local()
mydata.x = 1

with cv:
  while not an_item_is_available():
    cv.wait()
  get_an_available_item()
  
with cv:
  make_an_item_available()
  cv.notify()
  
with cv:
  cv.wait_for(an_item_is_available)
  get_an_available_item()
  
b = Barrier(2, timeout=5)

def server():
  start_server()
  b.wait()
  while True:
    connection = accept_connection()
    process_server_connection(connection)
    
def client():
  b.wait()
  while True:
    connection = make_connection()
    process_client_connction(connection)
```

```
```

```
```


