## 1. Outdoor Player Z Coordinate

During normal outdoor gameplay, the player's Z coordinate appears to be stored at one of the following memory addresses:

- `0x814993a0`　col.4
- `0x81499570`　col.4

Further investigation is required to determine the exact purpose and usage of each address.

### Current State

#### Current Map

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/61a2f489-4e62-4138-b388-f28b7963f7e3" />

#### Current Player Z Coordinate

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/2871e1ec-38f4-47a5-b033-723b05decaf0" />

</br></br>

## 1-1. Changing the Z Coordinate

The player's height can be changed by directly modifying the Z coordinate value in memory.

### Z Coordinate: 160 → 3000

#### Player Z Coordinate

<img width="400" alt="image" src="https://github.com/user-attachments/assets/eeab95c0-52b6-4510-ae2c-616bc017f234" />

#### Player Location

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/34ab6e98-d01d-49d0-8ad8-52d9e870cd60" />

