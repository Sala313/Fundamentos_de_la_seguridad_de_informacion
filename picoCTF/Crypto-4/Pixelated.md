## Descripcion
I have these 2 images, can you make a flag out of them?[scrambled1.png](https://challenge-files.picoctf.net/c_wily_courier/d1577440e9a1f6f9ff3eacd6ec6a4b40722de3970b527f0e07e5a4a6f1c3c3e8/scrambled1.png) [scrambled2.png](https://challenge-files.picoctf.net/c_wily_courier/d1577440e9a1f6f9ff3eacd6ec6a4b40722de3970b527f0e07e5a4a6f1c3c3e8/scrambled2.png)
## Solucion
picoCTF{8cdf93c3}
## Notas
```
from PIL import Image
import numpy as np
import os

file_names = ["scrambled1.png", "scrambled2.png"]
img_data = [np.asarray(Image.open(f'{name}')) for name in file_names]

data = img_data[0].copy() + img_data[1].copy()

new_image = Image.fromarray(data)
new_image.save("out.png", "PNG")


open out.png
```
## Referencias

[CTFs/2021_picoCTF/Pixelated.md at master · Dvd848/CTFs · GitHub](https://github.com/Dvd848/CTFs/blob/master/2021_picoCTF/Pixelated.md)