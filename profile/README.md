# cuos.dev

What is CuOS?

🚀 CuOS components help you keep systems and services secure, up-to-date, and easy to manage — from a single device to a small fleet. They let you define, update, and control infrastructure via container images, Git workflows, or declarative configs, bringing practical DevOps to embedded, edge, server, and cloud environments.

The CuOS operating system is also a solid base for IoT, edge, and VM-based products.

## Framework overview:

Components are organized in layers from device to service:

| Layer | Component & purpose | Repository |
| --- | --- | --- |
| Device management | CuOS Fleet Management — agent + server for device enrollment, health telemetry, remote commands, and rollout orchestration. | [cuos-iac](https://github.com/cuos-dev/cuos-iac#readme) |
| Service management | CuOS IaC — Infrastructure-as-Code manager and Web UI for defining services, builds, deployments, and release channels. | [cuos-iac](https://github.com/cuos-dev/cuos-iac#readme) |
| Operating system | CuOS (OS) — minimal OS image with updater, image and installer factories, OTA tooling and reproducible builds. | [cuos](https://github.com/cuos-dev/cuos#readme) |

All components can be used independently — each CuOS component works standalone (you don’t need to run the others to use a single component).

# Need help or want to collaborate?

* Open an issue in the relevant repo.
* Contact us directly (contact AT simonwalz.de or via [LinkedIn](https://www.linkedin.com/in/simon-walz/))


<!--
Planned:

* Monitoring (e.g. notifications, when healthchecks or updates fail)
* Log analysis / telemetry
-->