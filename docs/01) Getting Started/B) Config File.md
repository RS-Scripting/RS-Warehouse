# Configuration

RS-Warehouse includes a `config.yml` file that allows you to control how certain features of the plugin behave.

The configuration file is located at:

`plugins/RS-Warehouse/config.yml`

After changing a setting, reload the plugin for the changes to take effect.

---

# Display Settings

The `display` section controls optional information and categories that are shown to players.

```yaml
display:
```

## Show Discovery Information

```yaml
show-discovery-information: true
```

Controls whether RS-Warehouse displays information about when an item was first deposited into the Warehouse database.
When enabled, discovery information can include information about when the item was first discovered.

### Options

```text
true
```

Discovery information will be displayed.

```text
false
```

Discovery information will not be displayed.

---

## Show Server Commands

```yaml
show-server-commands: true
```

Controls whether the **Server Commands** category is displayed.
The Server Commands category contains a list of commands available on your server.

> **NOTE:** This category does not execute commands. It is only used to provide players with a list of available commands.

### Options

```text
true
```

The Server Commands category will be displayed.

```text
false
```

The Server Commands category will be hidden.

---

## Show Server Rules

```yaml
show-server-rules: true
```

Controls whether the **Server Rules** category is displayed.
This category can be used to provide players with a list of rules for your server.

### Options

```text
true
```

The Server Rules category will be displayed.

```text
false
```

The Server Rules category will be hidden.

---

# Automatic Chest Processing

The `chest-auto-processing` section controls automatic scanning and processing of Warehouse Chests.

```yaml
chest-auto-processing:
```

## Enable Automatic Processing

```yaml
enabled: true
```

Controls whether Warehouse Chests are automatically scanned and processed.

### Options

```text
true
```

Warehouse Chests will automatically be scanned and processed.

```text
false
```

Automatic processing will be disabled.

---

## Processing Interval

```yaml
interval-seconds: 30
```

Controls how often RS-Warehouse automatically scans and processes Warehouse Chests.
The value is measured in seconds.

For example:

```yaml
interval-seconds: 30
```

The plugin will process Warehouse Chests every 30 seconds.
Increasing this value means chests will be processed less frequently.
Decreasing this value means chests will be processed more frequently.

---

# Item Creation Settings

These settings control how RS-Warehouse handles items that do not currently exist in the Warehouse database.

## Allow Uncategorized Item Creation

```yaml
allow-uncategorized-item-creation: true
```

Controls whether new items can automatically be added to the **Uncategorized** category when they are deposited into a Warehouse Chest.

### Options

```text
true
```

Items that do not already exist in the Warehouse can be automatically added to the Uncategorized category.

```text
false
```

Items that do not already exist in the Warehouse will not automatically be created.

---

## Always Show Uncategorized

```yaml
always-show-uncategorized: false
```

Controls whether the **Uncategorized** category is always displayed in the main Warehouse Category Menu.

### Options

```text
true
```

The Uncategorized category will always be displayed.

```text
false
```

The Uncategorized category will only be displayed when it contains items.

---

## Allow Damaged Item Creation

```yaml
allow-damaged-item-creation: true
```

Controls whether damaged versions of items can automatically be added as damaged variants of their base item.

### Options

```text
true
```

Damaged items can automatically be added to the damaged variants menu of their base item.

```text
false
```

Damaged items will not automatically be added as damaged variants.

---

# Chest Close Processing

The `chest-close-processing` section controls whether Warehouse Chests are processed when a player closes them.

```yaml
chest-close-processing:
```

## Enable Chest Close Processing

```yaml
enabled: true
```

Controls whether a Warehouse Chest is immediately processed when a player closes it.

### Options

```text
true
```

The Warehouse Chest will be processed immediately when a player closes it.

```text
false
```

The Warehouse Chest will not be processed when it is closed.
Items will instead be processed according to the Automatic Chest Processing settings if automatic processing is enabled.

--- 

# Default Configuration

The default `config.yml` is:

```yaml
#
# RS-Warehouse
#

display:

  # Display when item was first deposited
  # to database and what date it happened.
  show-discovery-information: true

  # Display the Server Commands category.
  # This category is a list of commands
  # available on your server. It DOES NOT
  # execute any commands.
  show-server-commands: true

  # Display the Server Rules category.
  # This category is a list of rules for
  # your server.
  show-server-rules: true


############################################
# Automatic-Chest scan and process settings.
############################################

chest-auto-processing:

  enabled: true
  interval-seconds: 30


############################################
# Item Creation. Whether to allow automatic
# creation when items aren't in the database.
############################################

# Allow item to be added to Uncategorized
# if item is not currently in warehouse.
allow-uncategorized-item-creation: true

# Whether or not to always show the Uncategorized category.
# True = Uncategorized will always show.
# False = Uncategorized will only show if it has items inside.
always-show-uncategorized: false

# Allow damaged items to be added to
# damaged variant menu of base items.
allow-damaged-item-creation: true


#######################################
# Chest Close Processing Settings
#######################################

chest-close-processing:

  # Process warehouse chests immediately
  # when a player closes them.
  enabled: true
```