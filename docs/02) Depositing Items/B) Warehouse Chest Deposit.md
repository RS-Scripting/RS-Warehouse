# Warehouse Chest Deposits
A Warehouse Chest can automatically process items placed inside it and deposit them into the shared Warehouse.
RS-Warehouse supports two methods of processing items from a Warehouse Chest:

- **Auto-Scan**
- **Process on Close**

Both methods ultimately deposit eligible items into the Warehouse.

---

## Auto-Scan
Auto-Scan periodically checks the contents of the Warehouse Chest while the chest is open or in use.
When Auto-Scan is enabled, RS-Warehouse checks the chest at the configured interval and processes any eligible items it finds.
By default, Auto-Scan runs every **30 seconds**.

### Configuration
Auto-Scan is controlled by the following configuration settings:

```yaml
chest-auto-processing:
  enabled: true
  interval-seconds: 30
  ```

## Chest Close Processing

### How It Works

1. Place items into the Warehouse Chest.
2. RS-Warehouse automatically scans the chest when it is closed.
3. Eligible items are removed from the chest.
4. The items are deposited into the Warehouse.
5. The chest is left with any items that could not be processed.

### Configuration
Auto-Scan is controlled by the following configuration settings:

```yaml
chest-close-processing:
  # Process warehouse chests immediately
  # when a player closes them.
  enabled: true
  ```
