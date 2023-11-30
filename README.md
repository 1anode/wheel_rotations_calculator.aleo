# wheel_rotations_calculator.aleo

The "WheelInfo" struct representing information about the wheel.

## Build Guide

To compile this Aleo program, run:
```bash
// Wheel rotations calculation program.
program wheel_rotations_calculator.aleo {
    // The "WheelInfo" struct representing information about the wheel.
    struct WheelInfo {
        // A struct member named "circumference" with type "field".
        circumference: field,
        // A struct member named "distanceTraveled" with type "field".
        distanceTraveled: field,
    }

    // The "main" function of this Leo program takes a "WheelInfo" struct type as input.
    // To pass "wheelInfo" into the "main" function we
    // 1. Define the "WheelInfo" type.
    // 2. Use brackets { } to enclose the struct members.
    // 3. Define each struct member name : value.
    //
    // You can try this transition function by running: 
    // leo run main "{ circumference: 2field, distanceTraveled: 10field }"

    transition main(wheelInfo: WheelInfo) -> field {
        // Calculate wheel rotations based on the formula.
        let rotations: field = wheelInfo.distanceTraveled / wheelInfo.circumference;

        return rotations;
    }
}

```

To execute this Aleo program, run:
```bash
leo run main "{ circumference: 2field, distanceTraveled: 10field }"
```
