# Database Templates

RS-Warehouse includes a `db-files-templates` folder inside the plugin folder.

This folder contains two database templates:

- `empty_database.db`
- `populated_database.db`

These files can be used to quickly replace the active Warehouse database.

---

## Populated Database

The `populated_database.db` file is the default database included with RS-Warehouse.
It contains the preconfigured categories and items included with the plugin.
This database is automatically used as the starting database when RS-Warehouse is installed for the first time.

---

## Empty Database

The `empty_database.db` file is a completely empty Warehouse database.

It contains:

- Zero categories
- Zero items

This can be used if you want to start with a completely blank Warehouse and create your own category and item organization from scratch.

---

## Using a Database Template

To replace the active Warehouse database with one of the templates:

1. Stop the server or disable/reload the plugin.
2. Open:

   `plugins/RS-Warehouse/db-files-templates/`

3. Choose the database template you want to use:

    - `populated_database.db`
    - `empty_database.db`

4. Make a copy of the selected file.
5. Rename the copied file to:

   `database.db`

6. Copy it into:

   `plugins/RS-Warehouse/`

7. Overwrite the existing `database.db` file.
8. Reload the RS-Warehouse plugin.

The selected database template will now become the active Warehouse database.

> **WARNING:** Replacing `database.db` will replace your current Warehouse categories, items, and stored database information. Make a backup of your existing `database.db` before replacing it if you may want to restore it later.