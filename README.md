# Quadcopter & Main-Aircraft Simulink Models

Professional Simulink models for UAV dynamics and control studies:

- `quadcopter.slx` is dedicated to the **quadrotor** model.
- The other Simulink models in this repository are for the **main-aircraft** model.

> **Current scope:** This project does **not yet include sensor and state-estimation blocks**. Those will be added later to support a more comprehensive SIL simulation workflow.

## Repository Structure

- `load_uav_params.m` — parameter initialization script (run first).
- `quadcopter.slx` — quadrotor model.
- Other `.slx` files — main-aircraft models.

## Requirements

- MATLAB
- Simulink
- Any MathWorks toolboxes required by your local model configuration

## Quick Start

1. Open MATLAB and set the current folder to this repository.
2. Run the parameter-loading script first:

```matlab
load_uav_params
```

3. Open and run the model you want:

- For quadrotor simulation:

```matlab
open_system('quadcopter.slx')
```

- For main-aircraft simulation:
  - Open one of the other `.slx` model files in the repository.

4. In Simulink, click **Run** to start simulation.

## Recommended Workflow

1. Edit parameters in `load_uav_params.m`.
2. Re-run `load_uav_params` after each parameter change.
3. Simulate the selected model (`quadcopter.slx` for quadrotor, others for main-aircraft).
4. Inspect responses in scopes/logged signals and iterate on controller or plant parameters.

## Notes

- Always execute `load_uav_params.m` before running any model to ensure the workspace is initialized correctly.
- If a model reports missing variables, rerun `load_uav_params` and verify the current MATLAB folder is the repository root.
