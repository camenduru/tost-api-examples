🐣 Please follow me for new updates https://twitter.com/camenduru <br />
🔥 Please join our discord server https://discord.gg/k5BwmmvJJU <br />
🥳 Please join my patreon community https://patreon.com/camenduru <br />

###  🥪 Tost API Examples
https://tost.ai

| Notebook | Info
| --- | --- |
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/camenduru/tost-api-examples/blob/main/flux.1-dev-tost-api.ipynb) | Flux.1 [dev] + Loras
```py
import requests

url = "https://dev.tost.ai/api/v1"
headers = {
    "Content-Type": "application/json",
    "Authorization": "API_KEY_HERE"
}
data = {
    "app": "flux.1-dev",
    "command": {
        "positive_prompt": "cute anime cat",
        "seed": 0,
        "steps": 20,
        "guidance": 3.5,
        "lora_file": "xlabs_realism.safetensors",
        "lora_strength_model": 1,
        "lora_strength_clip": 1,
        "sampler_name": "euler",
        "scheduler": "simple",
        "width": 1024,
        "height": 1024
    }
}

response = requests.post(url, headers=headers, json=data)
print(response.json())
```

