# KoruGAN

KoruGAN is an application distribution and isolation system.

[English](README.md) | [Türkçe](README.tr.md)

## Containers and alternatives

Docker is a widely used container ecosystem, but its components and products have different roles and licenses:

- **Docker Engine** is the open-source container engine, primarily used on Linux.
- **Docker Desktop** is Docker's desktop application for macOS, Windows, and Linux. It includes open-source components, but Docker Desktop itself is distributed under Docker's subscription terms.
- **Images** package an application and its dependencies; **containers** are running instances of those images.

The projects below are not all drop-in replacements. Some build images, some run containers, and others provide a desktop interface or a Kubernetes-specific runtime.

### Open-source projects

| Project | Category | License | Best fit |
| --- | --- | --- | --- |
| [Docker Engine](https://docs.docker.com/engine/) | Container engine | Apache-2.0 | The Docker CLI, daemon, and container workflow on Linux |
| [Podman](https://podman.io/docs) | Container engine | Apache-2.0 | Daemonless container management, including rootless workflows |
| [containerd](https://containerd.io/) | Container runtime | Apache-2.0 | A lower-level runtime used by platforms such as Kubernetes; not a complete Docker Desktop replacement |
| [Buildah](https://buildah.io/) | Image builder | Apache-2.0 | Building OCI images without requiring the Docker daemon |
| [CRI-O](https://cri-o.io/) | Kubernetes runtime | Apache-2.0 | Running containers for Kubernetes; not a general-purpose Docker replacement |
| [LXC](https://linuxcontainers.org/lxc/introduction/) | System containers | LGPL-2.1 | Lightweight Linux system containers; a different model from OCI application containers |
| [Podman Desktop](https://podman-desktop.io/) | Desktop interface | Apache-2.0 | Managing Podman and other container tools through a graphical interface |
| [Rancher Desktop](https://rancherdesktop.io/) | Desktop environment | Apache-2.0 | Local container development with containerd or Moby, with optional Kubernetes |
| [Colima](https://github.com/abiosoft/colima) | Local container environment | MIT | A lightweight, command-line-managed container environment, especially on macOS |

### Proprietary or commercial desktop products

| Product | Platforms | Licensing notes |
| --- | --- | --- |
| [Docker Desktop](https://docs.docker.com/subscription-billing/desktop-license/) | macOS, Windows, Linux | Docker Desktop is proprietary and includes open-source components. Docker's current terms allow free use for personal use, education, non-commercial open-source projects, and small businesses with fewer than 250 employees **and** less than $10 million in annual revenue. Other commercial use and government use require a paid subscription. |
| [OrbStack](https://orbstack.dev/) | macOS | A proprietary desktop product. Review its current license and pricing before adopting it, especially for organizational use. |

Docker Engine and Docker Desktop are not licensed the same way. Docker's subscription terms apply to Docker Desktop; Docker says the licensing terms for the Docker Engine and Moby open-source projects have not changed. Always review the current license and subscription terms for the specific product and use case.

### Choosing a tool

- Choose **Docker Engine** when you want Docker's standard engine and CLI workflow, especially on Linux.
- Consider **Podman** for daemonless or rootless workflows, and test any Docker API or Compose-dependent tooling for compatibility.
- Choose **containerd** or **CRI-O** when selecting infrastructure for Kubernetes, rather than as a direct desktop replacement.
- Choose **Buildah** when image building is the need, or **LXC** when Linux system containers fit better than OCI application containers.
- For a graphical local environment, compare **Podman Desktop**, **Rancher Desktop**, **Docker Desktop**, and **OrbStack** against your operating system and licensing requirements.

### License

Copyright (C) 2026-2027 PSD Authors

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Affero General Public License as published
by the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.

See [CHANGELOG.md](CHANGELOG.md) for the project history.
