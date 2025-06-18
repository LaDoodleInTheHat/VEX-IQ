# VEX IQ Python Syntax

## Basic Structure

```python
from vex import *

brain = Brain()
motor_left = Motor(Ports.PORT1)
motor_right = Motor(Ports.PORT6)

# Main loop
while True:
    motor_left.spin(FORWARD)
    motor_right.spin(FORWARD)
    wait(1, SECONDS)
    motor_left.stop()
    motor_right.stop()
    wait(1, SECONDS)
```

## Common Commands

| Action                | Syntax Example                                 |
|-----------------------|------------------------------------------------|
| Print to screen       | `brain.screen.print("Hello")`                  |
| Wait                  | `wait(2, SECONDS)`                             |
| Set motor speed       | `motor_left.set_velocity(50, PERCENT)`         |
| Spin motor            | `motor_left.spin(FORWARD)`                     |
| Stop motor            | `motor_left.stop()`                            |
| Drive robot           | `drivetrain.drive_for(FORWARD, 100, MM)`       |
| Turn robot            | `drivetrain.turn_for(RIGHT, 90, DEGREES)`      |
| Get sensor value      | `distance_sensor.distance(MM)`                 |

## Example: Drive Forward

```python
from vex import *

brain = Brain()
drivetrain = Drivetrain(Motor(Ports.PORT1), Motor(Ports.PORT6))

drivetrain.drive_for(FORWARD, 200, MM)
```