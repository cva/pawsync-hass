# Pawsync Home Assistant Integration

This custom integration allows you to connect your Pawsync pet feeder devices to Home Assistant. You can monitor device status, view sensor data, and trigger feeding actions directly from your smart home dashboard.

## Features

- **Sensor Entities:** Exposes device properties (e.g., food level) as Home Assistant sensors.
- **Feed Service:** Trigger manual feeding via Home Assistant services.

## Installation

### HACS

1. In HACS, add this repository's GitHub URL as a custom repository with type **Integration**.
2. Download **Pawsync**.
3. Restart Home Assistant.

### Manual

1. Copy `custom_components/pawsync` from this repository into your Home Assistant configuration directory's `custom_components` folder. The resulting path should be `custom_components/pawsync/manifest.json`.
2. Restart Home Assistant.

## Configuration

### UI Setup

1. Go to **Settings > Devices & Services**.
2. Click **Add Integration** and search for "Pawsync".
3. Enter your Pawsync account credentials.

### YAML Setup (optional)

Add to your `configuration.yaml`:

```yaml
pawsync:
  username: your_email@example.com
  password: your_password
```

## Services

### Feed

Trigger a manual feeding for a device:

```yaml
service: pawsync.feed
data:
  entity_id: sensor.pawsync_device_id
```

## License

MIT

## Disclaimer

This integration is not affiliated with or endorsed by Pawsync.
