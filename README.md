# JTURPCM4248 ThingsBoard Dashboard

## Overview
This repository contains the ThingsBoard dashboard configuration for monitoring and controlling a concrete mixer truck dosing system. The dashboard provides real-time telemetry visualization, trip statistics, dosing control, power status monitoring, and analytics.

## Features

### Truck Monitoring
- Truck Number Display
- Device Number Display
- Mixer State Monitoring
- Dosing Mode Status

### Telemetry Monitoring
- Total Trips
- Dosing Count
- Dosing Amount per Trip
- Manual Dosing Amount
- External Power Supply Status

### Remote Control
- RPC-based Dosing Amount Control
- Configurable Dosing Setpoint
- Real-time Device Interaction

### Analytics
- Historical Data Visualization
- Performance Monitoring
- Trend Analysis

## Dashboard Components

| Component | Description |
|-----------|-------------|
| Truck Dashboard | Main monitoring screen |
| Graph & Analytics | Historical trends and reports |
| Truck Image Card | Visual representation of vehicle |
| Status Cards | Device and operational information |
| RPC Controls | Remote dosing configuration |

## Telemetry Keys

| Key | Description |
|------|-------------|
| Total_Trip | Total completed trips |
| Dosing_Count | Number of dosing operations |
| Dosing_amount_per_trip | Chemical dosage per trip |
| Manual_dosing_amount | Manual dosing quantity |
| Dosing_mode | Auto or Manual mode |
| Event | Current mixer state |
| External_Supply | Power source status |

## Power Status Logic

| Value | Display |
|---------|---------|
| false | On UPS |
| true | On Battery |

## Requirements

- ThingsBoard Platform
- MQTT-enabled Device
- Configured Device Telemetry
- RPC Support Enabled

## Installation

1. Login to ThingsBoard.
2. Navigate to Dashboards.
3. Select Import Dashboard.
4. Upload the dashboard JSON file.
5. Configure entity aliases and device mappings.
6. Save and publish the dashboard.

## Remote Procedure Calls (RPC)

Supported methods:

```json
{
  "method": "getState"
}
