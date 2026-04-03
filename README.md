# Raspberry Pi Health Card for Home Assistant

A sleek, modern Lovelace custom card for Home Assistant, designed specifically for Raspberry Pi users. It monitors your Pi's vital stats and alerts you instantly if a dangerous "Under-Voltage" condition occurs.

![Apple-Aesthetic Design](https://img.shields.io/badge/Design-Clean%20%26%20Minimal-blue)
![HACS Compatible](https://img.shields.io/badge/HACS-Custom%20Repository-orange)

## 🌟 Features
* **Apple-Aesthetic Design:** Clean, rounded corners, soft shadows, matching the default Home Assistant theme.
* **Vital Monitoring:** Displays CPU Temperature, RAM Usage, and Disk Space.
* **Smart Under-Voltage Warning:** Automatically detects power supply issues (Yellow Lightning Bolt) and displays a prominent warning box.
* **Integrated Calculator:** Provides a direct link to the [Raspberry Pi Power Calculator](https://raspberry.tips/?page_id=7948) to help users find the correct power supply.

## 📦 Installation via HACS
1. Go to **HACS** -> **Frontend**.
2. Click the 3 dots in the top right corner and select **Custom repositories**.
3. Add the URL of your GitHub repository.
4. Select **Lovelace** as the category.
5. Click **Add** and then install the "Raspberry Pi Health Card".
6. Add the resource reference if HACS doesn't do it automatically.

## 🛠️ Configuration
Add the card to your dashboard using the manual YAML editor:

```yaml
type: custom:rpi-health-card
title: My Raspberry Pi 5
temp_entity: sensor.cpu_temperature
ram_entity: sensor.memory_use_percent
disk_entity: sensor.disk_use_percent
power_entity: binary_sensor.rpi_power_status
```

*Note: You need the official System Monitor and Raspberry Pi Power Supply Checker integrations enabled in Home Assistant.*

---
**Powered by [raspberry.tips](https://raspberry.tips/home-assistant-auf-dem-raspberry-pi-der-grosse-smart-home-hub-2026)** - Your ultimate guide for Smart Home, Home Assistant, and Raspberry Pi tutorials (2026).
