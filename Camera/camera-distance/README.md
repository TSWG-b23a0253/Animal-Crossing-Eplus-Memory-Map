# Camera Distance

The memory address `81476D90` appears to control the camera distance (depth).

Increasing the value moves the camera farther away from the player, allowing a larger area of the map to be visible.

## Memory Address

| Address | Column | Description | Default Value |
|---|---:|---|---:|
| `81476D90` | 2nd | Camera distance (depth) | `20` |

- Address

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/b8922bb6-92b0-4df0-b2ce-bcec5a988926" />

</br></br>

## Default: `20`

The default camera distance is `20`.

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/2fe98b9c-1253-48ee-b842-e67354a9fd85" />

## Camera Distance = `30`

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/658cb582-1edb-40b3-abd1-29c07959feb6" />

## Camera Distance = `100`

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/98fe2c32-3c95-4e29-817b-9722e5902ad6" />

## Camera Distance = `150`

<img width="1440" height="854" alt="image" src="https://github.com/user-attachments/assets/a4bbebb8-2f80-4005-8d61-861f2deff2b4" />

As the value increases, the camera moves progressively farther away.

At very high values, parts of the map that are normally outside the visible area can be seen.
