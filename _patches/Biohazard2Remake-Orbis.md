# Resident Evil 2

[Game Index](README.md#games)

## Resolution Patch

[Demo](https://youtu.be/Qf3BCH8-ZPM)

Author: [illusion](https://twitter.com/illusion0002)

In file `eboot.bin`

<details>
<summary>Code for 1.05 (Click to Expand)</summary>

```
0x3FCA2D7 1F 85 2B 3F
# 67% of 1920x1080 or 2880x1620
# 1920x1080 => 1280x720
# 2880x1620 => 1920x1080
# 00 00 80 3F = 1.00f (default)
# 1F 85 2B 3F = 0.67f
```

</details>

## 30 FPS Limit (Proper Frame-Pacing)

[Demo](https://youtu.be/Qf3BCH8-ZPM)

Author: [illusion](https://twitter.com/illusion0002)

In file `eboot.bin`

<details>
<summary>Code for 1.05 (Click to Expand)</summary>

```
# Call

0x3F72473 48 E8 DB 07 00 00

# 0x1 to sceVideoOutSetFlipRate

0x3F72C54 41 8B 7F 10 BE 01 00 00 00 C3

## notes:
# 0x0 16.67ms -- 60hz
# 0x1 33.33ms -- 30hz
# 0x2 50.00ms -- 20hz
##
```

</details>
