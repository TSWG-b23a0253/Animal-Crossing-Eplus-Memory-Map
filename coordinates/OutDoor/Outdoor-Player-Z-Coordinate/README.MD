## 1. Outdoor Player Z Coordinate

During normal outdoor gameplay, the player's Z coordinate appears to be stored at one of the following memory addresses:

- `0x814993a0`　col.4
- `0x81499570`　col.4

Further investigation is required to determine the exact purpose and usage of each address.

### Current State

#### Current Map


![Current Map](./images/current-map.png)

#### Current Player Z Coordinate

<!-- Insert Current Player Z Coordinate Image Here -->

![Current Player Z Coordinate](./images/current-z-coordinate.png)


## 1-1. Changing the Z Coordinate

The player's height can be changed by directly modifying the Z coordinate value in memory.

### Z Coordinate: [Original Value] → [Modified Value]

#### Player Z Coordinate

<!-- Insert Modified Z Coordinate Image Here -->

![Modified Player Z Coordinate](./images/modified-z-coordinate.png)

#### Player Location

<!-- Insert Player Location Image Here -->

![Player Location](./images/modified-player-location.png)


### Z Coordinate: [Modified Value] → [Modified Value]

#### Player Z Coordinate

<!-- Insert Modified Z Coordinate Image Here -->

![Modified Player Z Coordinate](./images/modified-z-coordinate-2.png)

#### Player Location

<!-- Insert Player Location Image Here -->

![Player Location](./images/modified-player-location-2.png)


## 1-2. Changing the Player's Height

By modifying the Z coordinate, the player's vertical position can be changed, allowing the player to move above or below the normal ground level.

### Above Ground Level

<!-- Insert Above Ground Image Here -->

![Player Above Ground](./images/above-ground.png)

### Below Ground Level

<!-- Insert Below Ground Image Here -->

![Player Below Ground](./images/below-ground.png)
