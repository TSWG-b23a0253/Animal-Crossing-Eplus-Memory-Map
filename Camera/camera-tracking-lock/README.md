# Camera Tracking Lock

The memory address `81476DD0` appears to control the camera's tracking behavior.

The default value is `0`.

Changing this value from `0` causes the camera to stop following the villager.

## Memory Address

| Address | Column | Description | Default Value |
|---|---:|---|---:|
| `81476DD0` | 1st | Camera tracking lock | `0` |

## Default: `0`

When the value is `0`, the camera normally follows the villager.

## Changed Value

Changing the value from `0` causes the camera to stop following the villager.

Once tracking has been disabled, the camera no longer follows the villager while remaining in the current area.

## Reset Behavior

Entering a house resets the camera state.

After entering a house, the camera tracking behavior returns to normal.

## Notes

This address appears to affect the camera's tracking state rather than directly controlling its X, Y, or Z position.

The effect persists while remaining in the current area, but is reset when entering a house.

The exact meaning of values other than `0` requires further investigation.

</br>

## Screen

*The camera remains fixed while the player enters a building.*

<img width="1440" height="867" alt="image" src="https://github.com/user-attachments/assets/da77424d-60bc-4d20-a3f9-ef7c97220b5e" />
