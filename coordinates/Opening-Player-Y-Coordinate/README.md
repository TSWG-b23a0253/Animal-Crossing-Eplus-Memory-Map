## 1. Player Y Coordinate During the Opening Sequence

During the opening sequence, the player's Y coordinate appears to be stored at the following memory address:

- `0x8149c910`

Further investigation may be required to determine how this address is used during different parts of the opening sequence.

### Current State

#### Current Map

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/2f6f4ebb-8c26-4e19-a02c-9322fca3a8cb" />

#### Current Player Y Coordinate

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/cdd968ad-6ff2-4ed0-94ef-ae1a2861634c" />


## 1-1. Changing the Y Coordinate

The player's position can be changed by directly modifying the Y coordinate value in memory.

### Y Coordinate:  2497 → 4400

#### Player Y Coordinate

<img width="400" alt="image" src="https://github.com/user-attachments/assets/490c3c2c-5d02-46fd-b454-e324dae3597a" />


#### Player Location

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/91749c0f-7b8c-4509-a3b7-5abb46c761cb" />



## 1-2. Limitations During the Opening Sequence

Unlike during normal outdoor gameplay, modifying the Y coordinate during the opening sequence does not appear to allow the player to enter the ocean or reach the deserted island.

- The player does not appear to be able to enter the ocean.
- The deserted island does not appear to be reachable.
