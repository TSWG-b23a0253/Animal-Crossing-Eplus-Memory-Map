## 1. Outdoor Player X Coordinate

During normal outdoor gameplay, the player's X coordinate appears to be stored at one of the following memory addresses:

- `0x814993a0`　col.3
- `0x81499570`　col.3

Further investigation is required to determine the exact purpose and usage of each address.

### Current State

#### Current Map

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/49f671b6-d140-4279-8129-29ed1682a7fe" />

#### Current Player X Coordinate

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/f1987298-c1b1-425f-aba0-8a4563339c32" />

</br>

## 1-1. Changing the X Coordinate

The player's position can be changed by directly modifying the X coordinate value in memory.

### X Coordinate: 658 → 3300

#### Player X Coordinate

<img width="400" alt="image" src="https://github.com/user-attachments/assets/710293fc-0ae8-479c-b6fe-5be3018c2427" />

#### Player Location

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/c110b8d0-92dd-45c8-a306-c48cfa0b6233" />
