# 자랑스러운 한국 국기 설명

> 하얀 바탕: 밝음과 순수 전통적으로 평화를 사랑하는 우리의 민족성을 나타냄
```py
w, h = 600, 400

img = Image.new('RGB', (w, h), (241, 241, 241))
```
> 양(陽): 赤色을 띠며, 上에 있으며, 左을 뜻함
> 
> 음(陰): 靑色을 띠며, 下에 있으며, 右를 뜻함
```py
taegeuk = Image.new('RGB', (h // 2, h//2), color=(241, 241, 241))
draw = ImageDraw.Draw(taegeuk)

draw.pieslice((0, 0, h // 2, h // 2), start=180, end=360, fill=(205, 49, 58))
draw.pieslice((0, 0, h // 2, h // 2), start=0, end=180, fill=(0, 71, 160))

draw.ellipse((0, h // 8, h // 4, h * 3 // 8), fill=(205, 49, 58))
draw.ellipse((h // 4, h // 8, h // 2, h * 3 // 8), fill=(0, 71, 160))

taegeuk = taegeuk.rotate(-33.69, fillcolor=(241, 241, 241))

img.paste(taegeuk, (h // 2, h // 4))
```
> 건(乾): 東, 天, 春分을 상징
```py
sky = Image.new('RGB', (h // 4, h // 6), color=(14, 14, 14))
draw = ImageDraw.Draw(sky)

draw.rectangle((0, h * 2 // 48, h // 4, h * 3 // 48), fill=(241, 241, 241))
draw.rectangle((0, h * 5 // 48, h // 4, h * 6 // 48), fill=(241, 241, 241))

sky = sky.rotate(90 - 33.69, expand=True, fillcolor=(241, 241, 241))

img.paste(sky, (h * 22 // 96, h * 9 // 96))
```
> 곤(坤): 西, 地, 夏至를 상징
```py
earth = Image.new('RGB', (h // 4, h // 6), color=(14, 14, 14))
draw = ImageDraw.Draw(earth)

draw.rectangle((0, h * 2 // 48, h // 4, h * 3 // 48), fill=(241, 241, 241))
draw.rectangle((0, h * 5 // 48, h // 4, h * 6 // 48), fill=(241, 241, 241))
draw.rectangle((h * 11 // 96, 0, h * 13 // 96, h * 2 // 48), fill=(241, 241, 241))
draw.rectangle((h * 11 // 96, h * 3 // 48, h * 13 // 96, h * 5 // 48), fill=(241, 241, 241))
draw.rectangle((h * 11 // 96, h * 6 // 48, h * 13 // 96, h * 8 // 48), fill=(241, 241, 241))

earth = earth.rotate(90 - 33.69, expand=True, fillcolor=(241, 241, 241))

img.paste(earth, (h * 96 // 96, h * 59 // 96))
```
> 감(坎): 北, 月, 冬至, 水를 상징
```py
water = Image.new('RGB', (h // 4, h // 6), color=(14, 14, 14))
draw = ImageDraw.Draw(water)

draw.rectangle((0, h * 2 // 48, h // 4, h * 3 // 48), fill=(241, 241, 241))
draw.rectangle((0, h * 5 // 48, h // 4, h * 6 // 48), fill=(241, 241, 241))
draw.rectangle((h * 11 // 96, 0, h * 13 // 96, h * 2 // 48), fill=(241, 241, 241))
draw.rectangle((h * 11 // 96, h * 6 // 48, h * 13 // 96, h * 8 // 48), fill=(241, 241, 241))

water = water.rotate(90 + 33.69, expand=True, fillcolor=(241, 241, 241))

img.paste(water, (h * 96 // 96, h * 9 // 96))
```
> 리(離): 南, 日, 火, 秋分을 상징
```py
fire = Image.new('RGB', (h // 4, h // 6), color=(14, 14, 14))
draw = ImageDraw.Draw(fire)

draw.rectangle((0, h * 2 // 48, h // 4, h * 3 // 48), fill=(241, 241, 241))
draw.rectangle((0, h * 5 // 48, h // 4, h * 6 // 48), fill=(241, 241, 241))
draw.rectangle((h * 11 // 96, h * 3 // 48, h * 13 // 96, h * 5 // 48), fill=(241, 241, 241))
fire = fire.rotate(90 + 33.69, expand=True, fillcolor=(241, 241, 241))

img.paste(fire, (h * 22 // 96, h * 59 // 96))
```
> 태극기 출력하기
```py
img.show()
```
