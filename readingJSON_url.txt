import pandas as pd
import urllib, json

url = 'https://jsonplaceholder.typicode.com/todos'

operUrl = urllib.request.urlopen(url)
if(operUrl.getcode()==200):
  data = operUrl.read()
else:
  print("Error receiving data", operUrl.getcode())

ndata = json.loads(data)
ndata

ndf = pd.DataFrame(ndata)
ndf