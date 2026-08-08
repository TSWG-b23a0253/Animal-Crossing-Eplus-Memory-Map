# Camera Position

The following memory addresses appear to represent the camera's position in 3D space.

These values are continuously updated by the game and return to their original values when manually modified.

## Memory Addresses

| Address | Column | Description | Behavior |
|---|---:|---|---|
| `81476D70` | 4th | Camera X position | Returns to original value |
| `81476D80` | 2nd | Camera Y position | Returns to original value |
| `81476D80` | 1st | Camera Z position | Returns to original value |

## Axes

- **X**: Camera position along the horizontal axis.
- **Y**: Camera position along the vertical axis.
- **Z**: Camera position along the depth axis.

## Notes

These values cannot normally be changed permanently by simply editing the memory values, as the game continuously recalculates and overwrites the camera position.

Further investigation is required to identify the values or instructions responsible for calculating the camera position.

</br></br>

## change X position

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/9a6cd98b-2adf-4354-8dae-343fcad43fb9" />

## change Y position

<img width="1440" height="860" alt="image" src="https://github.com/user-attachments/assets/f32cc878-4441-4695-9887-b68eb00832e4" />

## change Z position

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/cb392a37-60ba-4193-80b4-439654692bc7" />

