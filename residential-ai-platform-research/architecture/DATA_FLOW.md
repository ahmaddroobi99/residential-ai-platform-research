# Data flow

See [INTEGRATION_MAP.md](INTEGRATION_MAP.md) and [SYSTEM_ARCHITECTURE.md](SYSTEM_ARCHITECTURE.md).

Canonical flow: address → parcel/terrain/climate/zoning → constraint JSON → plan graph → IFC → gbXML/EnergyPlus + clash/IDS → QTO → glTF viewer → (later) USD twin + HA + ROS2.
