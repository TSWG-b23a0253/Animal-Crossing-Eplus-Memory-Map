# Changing Inventory Items

In *Doubutsu no Mori e+*, the items in the player's inventory can be modified by directly changing their values in memory.

## Inventory Address

The following memory location corresponds to the **second item in the inventory**:

* `0x81266D00` — **Column 2**

The value stored in Column 2 at this address determines the second item in the player's inventory.

If the player does not have an item in this position, the value is:

```text
0
```

## Changing the Second Item

By changing the value in **Column 2 at `0x81266D00`**, the second item in the inventory can be modified.

### Current State

#### Second Item in the Inventory

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/50791d46-3979-43c3-a6f2-57a7bcda288e" />

#### Memory Value

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/3ac8db81-9338-4c72-979e-a06c7caebf55" />

</br>

### After Modification

#### Modified Memory Value　「121212」

<img width="400" alt="image" src="https://github.com/user-attachments/assets/d71bafe4-bacd-417d-a690-cd9cbf90911e" />

#### Second Item After Modification

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/393e55a8-9f3e-4adc-bad1-f82720149b52" />
