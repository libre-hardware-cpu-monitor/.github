# Libre Hardware Monitor - Temperatures and Clocks While the PC Works

## At a Glance

Idle temperatures are a weak story. Libre Hardware Monitor is useful when you leave it open, start the workload, and watch which sensor climbs. CPU package, CPU cores, GPU, and motherboard zones are different. A laptop that is "80 degrees" might be the GPU while the CPU is fine, or the reverse. The tree lets you see which.

- Live sensors for CPU, GPU, and many boards
- A log to CSV if you need a before-and-after
- Fan speeds where the board exposes them
- No fan control in the sense of a curve editor
- No license server and no extra driver suite required for a basic read

If a fan header does not appear, the board may not publish it. Do not install a stack of vendor utilities on top until you know you need that header.

![Libre Hardware Monitor tree with CPU and GPU temperatures](https://www.mediaket.net/images/librehardware.webp)

## What to Watch

| Sensor | When it matters |
|---|---|
| CPU package | Sustained render or compile |
| Individual cores | A single hot core while others are idle |
| GPU | Games and GPU compute |
| Storage | A drive that throttles under copy |
| Fans | Whether speed rises when temperature does |

1. Open the tool and collapse vendors you do not own.
2. Start the workload.
3. Watch the sensor you care about for several minutes, not one second.
4. Log only if you need to compare a fan change later.
5. Ignore a sensor that sits at zero or at a nonsense value. It is unimplemented, not a frozen CPU.

## Fits

Desktops and laptops where you need a second opinion on heat. A poor fit for setting fan curves. Use a fan-control tool for that, and use this to see whether the curve worked. A poor fit for SMART health. A disk can be dying and cool.

[![Open Libre Hardware Monitor](https://img.shields.io/badge/Open-Libre_Hardware_Monitor-0f766e?style=for-the-badge&logo=windows&logoColor=white)](https://mouron455.github.io/.github/libre-hardware-monitor)

## Requirements

| Item | Expectation |
|---|---|
| PC | Windows the build supports |
| Rights | Administrator so more sensors appear |
| Workload | Something real, not an idle glance |
| GPU driver | Current, or the GPU row may be empty |

## Fixes

The tree is almost empty. Run it elevated.
GPU is missing. Update the driver or the tool.
A temperature looks stuck. That sensor is not implemented. Use another row.
The log file is huge. You left it running for days. Log the test, then stop.
Fans do not change. This program reads them. It does not command them.

## Watch the Row That Climbs

Idle temperatures are a weak story. Leave Libre Hardware Monitor open, start the game or the render, and see whether the CPU package, a single core, or the GPU is the one that rises. Fan RPM, when the board exposes it, should rise with that heat. If a header never appears, the board is not publishing it. Do not stack vendor utilities until you know you need that header.

A zero that never moves is unimplemented. Ignore it. Storage temperature is a different row from the CPU. A disk can be unhealthy and cool. SMART is another tool. This one does not draw fan curves. Use it to check a curve you set elsewhere. Log a short test, then stop. A week-long CSV is not a new measurement.

- Elevated if the tree is thin
- Real workload, several minutes
- CPU, GPU, and storage not treated as one number
- Stuck zeros ignored
- GPU driver current
- Logging stopped after the test
- Fan control left to a curve tool

| Climbs | Look at |
|---|---|
| CPU package | Cooler and power limit |
| One core | Whether the load is single-thread |
| GPU | The game or compute job |
| Nothing under load | The wrong sensor, or the load is not running |

The tray icon at the desktop is not the diagnosis.

## Phrase List

libre hardware monitor, cpu gpu temperature, libre hardware monitor windows, sensor log csv, motherboard fan rpm, cpu package temp, open hardware monitor fork, hw sensor log
