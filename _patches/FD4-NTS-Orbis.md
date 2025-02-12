# Elden Ring: Network Test

[Game Index](README.md#games)

## Patch Preview

Patch applied: Resolution Patch (Neo) + 30 FPS Fix

![](https://storage.googleapis.com/assets-illusion0001/images/patches/preview/EldenRingPatches/EldenRingNeoPreview.png)

## Framerate Patch

### 60 FPS Unlock (For Base)

<details>
<summary>Code (Click to Expand)</summary>

```
# Flipmode
0x1BF6627 95

# VFR
0x1BF6795 48 E9 5B 00 00 00
```

</details>

### 30 FPS Fix (Proper Frame Pacing)

Locks FPS to 30 with Proper Frame Pacing.

Author: [illusion](https://twitter.com/illusion0002)

In file `eboot.bin`

<details>
<summary>Code (Click to Expand)</summary>

```
# Flipmode (Base Only)
0x1BF6627 95

# Call
0x2D42FF0 E8 0F D5 39 00
# Main code
0x30E0503 00 BF 00 01 11 4E BE 01 00 00 00 E8 ED F8 D8 FF C3
```

</details>

## Resolution Patch

Author: [illusion](https://twitter.com/illusion0002)

In file `eboot.bin`

<details>
<summary>Code (Click to Expand)</summary>

```
# Base
0x3C68B8C 00 05 00 00 D0 02 00 00

# Neo
0x1BE505F 80 07 00 00
0x1BE5069 38 04 00 00
```

</details>

## Bypass Network Check

Author: Unknown

In file `eboot.bin`

<details>
<summary>Code (Click to Expand)</summary>

```
0x015724A0 90 90 90 90 90 90
0x015725AC 90 90 90 90 90 90
0x015724B1 E9 EF 00 00 00 90
```

</details>

## Disable Fog Wall

Author: Pav

In file `eboot.bin`

<details>
<summary>Code (Click to Expand)</summary>

```
0x013BBC33 90 90 90 90 90
```

</details>

## Enable video recording

Re-enables built-in video recording (share button)

Author: Whitehawkx

In file `eboot.bin`

<details>
<summary>Code (Click to Expand)</summary>

```
0x01BFF78E 90 90 90 90 90
```

</details>

## Enable screenshots

Re-enables built-in screenshot capture (share button)

Author: Whitehawkx

In file `eboot.bin`

<details>
<summary>Code (Click to Expand)</summary>

```
0x01BFF7AC 90 90 90 90 90
```

</details>
