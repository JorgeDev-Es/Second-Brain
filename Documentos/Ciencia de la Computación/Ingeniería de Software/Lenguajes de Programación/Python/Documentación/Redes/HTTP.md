# HTTP
```Python
import http.client

host = 'docs.python.org'
conn = http.client.HTTPSConnection(host)

conn.request(method='GET', url="/3/")

res = conn.getresponse()

data = res.read()

print(data)
```