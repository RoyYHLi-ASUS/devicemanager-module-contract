# Drone Data Field Specification

| Field | Type | Default | Can be empty? | Enum/Format | Description |
|-------|------|---------|---------------|-------------|-------------|
| id | string | N/A | N | uuid | Drone UUID |
| name | string | N/A | N | N/A | Drone name |
| status | string | unlink | N | `idle` `processing` `ready_to_go` `take_off` `flying` `hold` `rth` `landing` `error` | Drone status |
| battery_state | number | N/A | N | N/A | Drone battery percentage |
| ongoing_miss_id | string | N/A | Y | uuid | UUID of the ongoing mission assigned to this drone |
| ongoing_miss_name | string | N/A | Y | N/A | Name of the ongoing mission |
| swarm_id | string | N/A | N | uuid | Swarm UUID this drone is bound to |
| swarm_name | string | N/A | N | N/A | Swarm name this drone belongs to |
| rc_id | string | N/A | N | uuid | Remote control UUID bound to this drone |
| rc_name | string | N/A | N | N/A | Remote control name bound to this drone |
| drone_model_name | string | N/A | N | N/A | Drone model name |
| drone_weight | string | N/A | N | N/A | Drone's weight |
| drone_dimensions | string | N/A | N | N/A | Drone's dimensions |
| drone_endurance | number | N/A | N | N/A | Drone's endurance time in minutes |
| snr_compass | string | normal | N | `normal` `error` | Sensor compass status |
| snr_gyroscope | string | normal | N | `normal` `error` | Sensor gyroscope status |
| snr_accelerometer | string | normal | N | `normal` `error` | Sensor accelerometer status |
| payload_rtk | string | normal | N | `normal` `error` | Payload RTK module status |
| payload_lidar | string | normal | N | `normal` `error` | Payload LiDAR module status |

## Field Definitions

- **Can be empty?**: Y = Can be empty/null, N = Cannot be empty/null
- **Default**: Default value of the field
- **Enum**: Enumeration options
- **Format**: Data format (e.g., uuid)

## Status Descriptions

- `unlink`: Not connected
- `idle`: Idle
- `processing`: Processing
- `ready_to_go`: Ready to go
- `take_off`: Taking off
- `flying`: In flight
- `hold`: Hovering/Hold position
- `rth`: Returning to home
- `landing`: Landing
- `error`: Error state

## Sensor Status

Status values for all sensors and payload modules:
- `normal`: Operating normally
- `error`: Error or malfunction
