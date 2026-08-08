# Player Body Scale

The following memory addresses control the player's body scale.

The default value for each axis is `0.01`.

## Memory Addresses

### Address Group 1

| Address    | Column | Description        | Default Value |
| ---------- | -----: | ------------------ | ------------: |
| `814995A0` |    4th | Player body width  |        `0.01` |
| `814995B0` |    1st | Player body height |        `0.01` |
| `814995B0` |    2nd | Player body depth  |        `0.01` |

### Address Group 2

| Address    | Column | Description        | Default Value |
| ---------- | -----: | ------------------ | ------------: |
| `814993D0` |    4th | Player body width  |        `0.01` |
| `814993E0` |    1st | Player body height |        `0.01` |
| `814993E0` |    2nd | Player body depth  |        `0.01` |

## Scale Values

* **Width**: Controls the horizontal size of the player's body.
* **Height**: Controls the vertical size of the player's body.
* **Depth**: Controls the depth of the player's body.

The standard value is `0.01`. Increasing or decreasing these values changes the player's body proportions along the corresponding axis.

</br></br>

## Change All Scale Values from `0.01` to `0.1`

All three scale values—width, height, and depth—were changed from the default value of `0.01` to `0.1`.

### Before: All Scale Values = `0.01`

- Memory values:

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/5b91cd4f-dbdd-4809-a9e5-f7e1fa4b201d" />

- Player appearance:

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/eb46b10b-f0db-497e-8eac-e19c496e22bc" />

</br>

### After: All Scale Values = `0.1`

- Memory values:

<img width="400" alt="image" src="https://github.com/user-attachments/assets/f5c7f8dc-ce12-4205-a078-e2471be49b15" />

- Player appearance:

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/ac72c3a3-06a8-4ef0-8e9b-c57ead921afe" />

</br>

### After: All Scale Values = `0.005`

- Memory values:

<img width="400" alt="image" src="https://github.com/user-attachments/assets/921600a0-ae95-4890-883a-cab8bf71a66b" />

- Player appearance:

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/681b60d7-4dc0-46e3-be8e-c562ec23ebcd" />
