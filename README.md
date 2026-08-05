# UAV (Quadcopter & Fixed-wing) Simulink Models

Simulink models for UAV dynamics and control studies:

- `quadcopter.slx` is dedicated to the **quadrotor** model.
- The other Simulink models in this repository are for the **Fixed-wing** model.

> **Current scope:** This project does **not yet include sensor and state-estimation blocks**. Those will be added later to support a more comprehensive SIL simulation workflow. But for now, I'm going to simulate the HIL first:)

## Repository Structure

- `load_uav_params.m` — parameter initialization script (run first, this params is used for the fixed-wing only, if you want to use the quadrotor model, you only have to click on `quadcopter.slx`).
- `quadcopter.slx` — quadrotor model.
- Other files — fixed-wing models.

## Requirements

- MATLAB/Simulink (R2024a or after)
- Any MathWorks toolboxes required by your local model configuration

## How to use

1. Open MATLAB and set the current folder to this repository.
2. Run `load_uav_params.m`.
3. Open and run the model you want:

- For quadrotor simulation:

```matlab
open_system('quadcopter.slx')
```

- For fixed-wing simulation:

```matlab
open_system('aircraft.slx')
```

4. In Simulink, click **Run** to start simulation.

5. Jump into the `visualization` subsystem, then click on the `scope` block to see the responses.
