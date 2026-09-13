# cuos.dev

🚀 CuOS components help you keep systems and services secure, up-to-date, and easy to manage — from a single device to a small fleet. They let you define, update, and control infrastructure via container images, Git workflows, or declarative configs, bringing practical DevOps to embedded, edge, server, and cloud environments.

The CuOS operating system is also a solid base for IoT, edge, and VM-based products.

## Start here

**To build a bootable system**, start at [cuos-release](https://github.com/cuos-dev/cuos-release#readme): describe the system you want in a `system.json` and run `./cuos-release/tool.sh image`. It produces a disk image, an ISO installer or an LXC container.

## Framework overview

Components are organized in layers from device to service:

| Layer | Component & purpose | Repository |
| --- | --- | --- |
| Device management | CuOS Fleet Management — agent + server for device enrollment, health telemetry, remote commands, and rollout orchestration. | [cuos-iac](https://github.com/cuos-dev/cuos-iac#readme) |
| Service management | CuOS IaC — Infrastructure-as-Code manager and Web UI for defining services, builds, deployments, and release channels. | [cuos-iac](https://github.com/cuos-dev/cuos-iac#readme) |
| Operating system | CuOS (OS) — minimal OS image with updater, OTA tooling and reproducible builds. | [cuos](https://github.com/cuos-dev/cuos#readme) |
| Build & release | CuOS Release Tooling — `tool.sh`, the image and installer factories, pinned image versions, configuration merging, signing and encryption. | [cuos-release](https://github.com/cuos-dev/cuos-release#readme) |

All components can be used independently — each CuOS component works standalone (you don’t need to run the others to use a single component).

## Boiler plates and examples

CuOS can be taken up at four levels, from running services on a ready-made system to building an OS from scratch. The [Development Guide](https://github.com/cuos-dev/cuos/blob/main/docs/development-guide.md) explains which one is yours; these repositories are the starting points.

| Level | Repository |
| --- | --- |
| Container Service — run services, build nothing | [iac-hello-world-system](https://github.com/cuos-dev/iac-hello-world-system#readme) |
| Own CuOS Init App — your own update or deployment mechanism | [boilerplate-own-cuos-init-app](https://github.com/cuos-dev/boilerplate-own-cuos-init-app#readme) |
| Own OS based on the CuOS system — another board, or your own kernel drivers | [boilerplate-own-os-based-on-cuos](https://github.com/cuos-dev/boilerplate-own-os-based-on-cuos#readme) |

## Need help or want to collaborate?

* Open an issue in the relevant repo.
* Contact us directly (contact AT simonwalz.de or via [LinkedIn](https://www.linkedin.com/in/simon-walz/))


<!--
Planned:

* Monitoring (e.g. notifications, when healthchecks or updates fail)
* Log analysis / telemetry
-->