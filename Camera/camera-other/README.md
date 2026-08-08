# Miscellaneous Camera Values

The following memory addresses appear to be related to camera behavior.

Their exact purposes have not yet been fully identified.

## Memory Addresses

| Address | Column | Possible Description | Default Value / Notes |
|---|---:|---|---|
| `81476D80` | 3rd | Camera rotation | Approximately `±90` |
| `81476D80` | 4th | Camera rotation | Approximately `±180` |
| `81476D90` | 4th | Possible redraw / refresh value | Exact behavior unknown |
| `81476DC0` | 1st | Possible camera depth / distance | Returns to its original value |
| `814995C0` | 4th | Player-camera Z position / movement | Default: `-8` |

## Notes

### Camera Rotation

The values at `81476D80` appear to affect the camera rotation.

- 3rd column: approximately `±90`
- 4th column: approximately `±180`

The exact rotation axes have not yet been identified.

### Possible Redraw Value

`81476D90` (4th column) may be related to screen or camera redrawing.

The exact purpose is currently unknown.

### Camera Depth / Distance

`81476DC0` (1st column) appears to affect the camera's depth or distance.

When manually modified, the value returns to its original value, suggesting that it is continuously recalculated by the game.

### Player-Camera Z Position / Movement

`814995C0` (4th column) appears to affect the Z-axis relationship between the player and the camera.

The default value is `-8`.

Increasing the value appears to increase the movement speed.

The exact purpose of this value has not yet been identified.
