# Coordinate Memory

This directory contains memory address information related to player coordinates in **Animal Crossing e+**.

The addresses documented here were discovered and tested using **Dolphin Emulator**.

## 1. Outdoor Player Y Coordinate

During normal outdoor gameplay, the player's Y coordinate appears to be stored at one of the following memory addresses:

- `0x814993B0`
- `0x81499580`

Further investigation is required to determine the exact purpose and usage of each address.

### Current State

#### Current Map

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/8f2c5959-df1e-464c-8bf2-1c29d58c4b95" />

#### Current Player Y Coordinate

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/867ea42b-93ed-494b-8596-a0b1ea21b5e5" />


## 1-1. Changing the Y Coordinate

The player's position can be changed by directly modifying the Y coordinate value in memory.

### Y Coordinate: 858 → 3000

#### Player Y Coordinate

<img width="400" alt="image" src="https://github.com/user-attachments/assets/a633e26b-692a-4eea-bd90-0d13b9cc734d" />

#### Player Location

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/c280658c-8942-48fe-92b0-72beb2554350" />


### Y Coordinate: 3000 → 5000

#### Player Y Coordinate

<img width="400" alt="image" src="https://github.com/user-attachments/assets/5946cbe4-3b6d-40b6-ab31-c30151119e8e" />

#### Player Location

<img width="1440" alt="スクリーンショット 2026-08-08 14 02 56" src="https://github.com/user-attachments/assets/3a22e0cb-e4a8-4ae3-a40b-366ddba053a6" />


## 1-2. Reaching Normally Inaccessible Areas

By modifying the Y coordinate, the player can reach normally inaccessible areas, including the deserted island.

### Deserted Island

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/58863bbc-a6f1-430f-a438-60fa49b7c7ce" />
