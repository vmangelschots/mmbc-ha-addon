# MMBC Home Assistant Add-on

This is the official Home Assistant add-on for **MMBC (Multiple Marstek Battery Controller)** — a flexible controller for managing multiple Marstek Venus batteries based on smart meter data, MQTT integration, and Modbus TCP communication.

## 📦 Features

- Control multiple Marstek Venus batteries
- Uses a HomeWizard P1 meter for grid monitoring
- MQTT support for Home Assistant Energy Dashboard integration
- Supports cumulative charge/discharge stats and HA discovery
- Fully configurable via Home Assistant add-on UI

---

## 🔧 Configuration

The add-on is configured through the Home Assistant UI under **Settings > Add-ons > MMBC**.

### Required Options

| Option                | Description                                      |
|-----------------------|--------------------------------------------------|
| `P1_HOST`             | URL of the HomeWizard P1 Meter (e.g. `http://192.168.1.50`) |
| `BATTERY_1_IP`        | IP of the first battery                         |
| `BATTERY_1_ADDRESS`   | Modbus address (usually `1`)                    |
| `BATTERY_1_PORT`      | Modbus TCP port (default: `502`)                |
| `BATTERY_2_IP`        | IP of the second battery                         |
| `BATTERY_2_ADDRESS`   | Modbus address (usually `1`)                    |
| `BATTERY_2_PORT`      | Modbus TCP port (default: `502`)                |
| `MQTT_HOST`           | IP of your MQTT broker (e.g. Home Assistant)    |
| `MQTT_PORT`           | MQTT port (default: `1883`)                     |
| `MQTT_USERNAME`       | MQTT username                                   |
| `MQTT_PASSWORD`       | MQTT password                                   |
| `MQTT_TOPIC_PREFIX`   | Prefix for MQTT topics (e.g. `mmbc/virtual`)    |
| `MQTT_HA_DISCOVERY`   | Enable Home Assistant MQTT discovery (`true` or `false`) |
| `INTERVAL_SECONDS`    | Polling interval in seconds                     |