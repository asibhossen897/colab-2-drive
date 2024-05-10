# colab-2-drive


```python
# Downloading an image from Unsplash

import requests

url = 'https://unsplash.com/photos/QcJ1XCc3gJo/download?ixid=M3wxMjA3fDB8MXxhbGx8MTB8fHx8fHwyfHwxNzE1MzMwMzM1fA&force=true'

r = requests.get(url)

with open('cars.jpg', 'wb') as f:
  f.write(r.content)
```

```python
# Mounting Google Drive to Colab Runtime

from google.colab import drive
drive.mount('/content/drive')
```

```python
# Copying the Image to Drive

!cp cars.jpg drive/MyDrive/
```
