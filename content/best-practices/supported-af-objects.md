---
uid: supported-af-objects
---

# Supported AF objects

PI Cloud Connect currently supports the following PI AF objects:

- AF Elements

- AF Element Templates

  - Element Templates cannot exceed 3,000 attributes.

- AF Enumeration Sets

- AF Attributes configured with the following Data References:

  - None (static values)

  - PI Points

    - PI Cloud Connect uses replace (by default) or insert mode when writing to the PI Data Archive.

    - Historical PI Points

    - Future PI Points

      - The PI Server for both the Publisher and the Subscriber requires PI Server 2015.

      - If a Publication includes future PI Points but the Subscriber's PI Server does not support future data then the future PI Points will not be created on the Subscriber side.

      - When Publishing future PI Points following an upgrade to PI Server 2015 or higher it will be necessary to restart the PI Connect service in order to publish or subscribe to future data.

  - Formula data references which reference attributes that have also been published.

  - Attribute data references which reference attributes that have also been published.

  - Table data references

  - Units of Measure

    - Source UOM, Default UOM, and the Value UOM for attributes

    - UOM dependencies (reference UOM(s), class, base classes)

- AF Categories

The only fully supported AF objects are those listed above. Here is a short list of the commonly used unsupported objects:

- PI Analyses or PI Analyses Templates

- PI Event Frames

- Custom Data References (data reference will be set to none, and the configuration string will not be copied)

- Custom AF Reference types

- PI Point Arrays

- PI Notifications

- AF File data types

- AF Transfers and Cases
