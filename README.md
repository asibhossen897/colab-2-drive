# colab-2-drive

This repository provides Python code snippets to download images from Unsplash and copy them to Google Drive within a Google Colab environment.

## Usage

1. Open the notebook in Google Colab.
2. Copy the notebook to your drive.
3. Run each code cell sequentially. Change the codes as per your requirements.
4. Follow the instructions to mount Google Drive and copy images.

<hr>

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

"""
You can, of course copy an entire folder.
In that case, replace 'cars.jpg' with the folder name. And add ```-r``` in front of the folder name.
And to save to another folder, change 'drive/MyDrive/' accordingly.
"""

!cp -r images drive/MyDrive/
```
