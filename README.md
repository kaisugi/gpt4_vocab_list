# GPT-4 Vocab List

## o200k_base

```py
import base64
import requests


res = requests.get("https://openaipublic.blob.core.windows.net/encodings/o200k_base.tiktoken")
contents = res.content

for token, rank in (line.split() for line in contents.splitlines() if line):
    decoded_token = base64.b64decode(token)

    try:
        print(repr(decoded_token.decode('utf-8')))
    except:
        print(decoded_token)
```

## cl100k_base

```py
import base64
import requests


res = requests.get("https://openaipublic.blob.core.windows.net/encodings/cl100k_base.tiktoken")
contents = res.content

for token, rank in (line.split() for line in contents.splitlines() if line):
    decoded_token = base64.b64decode(token)

    try:
        print(repr(decoded_token.decode('utf-8')))
    except:
        print(decoded_token)
```