# Raspberry Pi Health Card for Home Assistant

A sleek, modern Lovelace custom card for Home Assistant, designed specifically for Raspberry Pi users. It monitors your Pi's vital stats and alerts you instantly if a dangerous "Under-Voltage" condition occurs.

![Apple-Aesthetic Design](https://img.shields.io/badge/Design-Clean%20%26%20Minimal-blue)
![HACS Compatible](https://img.shields.io/badge/HACS-Custom%20Repository-orange)

## 🌟 Features
* **Apple-Aesthetic Design:** Clean, rounded corners, soft shadows, matching the default Home Assistant theme.
* **Vital Monitoring:** Displays CPU Temperature, RAM Usage, and Disk Space.
* **Smart Under-Voltage Warning:** Automatically detects power supply issues and displays a prominent warning box.
* **Integrated Calculator:** Provides a direct link to the [Raspberry Pi Power Calculator](https://raspberry.tips/?page_id=7948) to help users find the correct power supply.

## 🛠️ Prerequisites
Before adding the card, ensure you have the following official integrations enabled in Home Assistant:

1. **System Monitor:** Provides sensors for CPU Temperature, RAM usage, and Disk usage.
   - [Home Assistant System Monitor Docs](https://www.home-assistant.io/integrations/systemmonitor/)
2. **Raspberry Pi Power Supply Checker:** Provides the under-voltage status sensor (`binary_sensor.rpi_power_status`).
   - [Home Assistant RPi Power Docs](https://www.home-assistant.io/integrations/rpi_power/)

## 📦 Installation via HACS
Since this is a custom card, you need to add it as a **Custom Repository**:

1. Open **HACS** in your Home Assistant.
2. Go to the **Frontend** section.
3. Click the **three dots** in the top right corner and select **Custom repositories**.
4. Paste the repository URL: `https://github.com/raspberry-tips/rpi-health-card`
5. Select **Lovelace** as the category.
6. Click **Add**, then find "Raspberry Pi Health Card" and click **Download**.
7. **Refresh your browser** to ensure the card is loaded.

## ⚙️ Configuration
Add the card to your dashboard using the manual YAML editor or the UI:

```yaml
type: custom:rpi-health-card
title: My Raspberry Pi 5
temp_entity: sensor.cpu_temperature
ram_entity: sensor.memory_use_percent
disk_entity: sensor.disk_use_percent
power_entity: binary_sensor.rpi_power_status
```

### Options
| Name | Type | Requirement | Description |
| :--- | :--- | :--- | :--- |
| `type` | string | **Required** | `custom:rpi-health-card` |
| `title` | string | Optional | Header title (Default: Raspberry Pi Health) |
| `temp_entity` | string | **Required** | Entity ID for CPU temperature sensor |
| `ram_entity` | string | **Required** | Entity ID for RAM usage (%) |
| `disk_entity` | string | **Required** | Entity ID for Disk usage (%) |
| `power_entity` | string | **Required** | Entity ID for RPi power status (binary_sensor) |

---
**Powered by [raspberry.tips](https://raspberry.tips/home-assistant-auf-dem-raspberry-pi-der-grosse-smart-home-hub-2026)** - Your ultimate guide for Smart Home, Home Assistant, and Raspberry Pi tutorials (2026).
