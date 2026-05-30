<p align="center">
  <img src="./PreciCore_Logo.png" alt="PreciCore Logo" width="420"/>
</p>

<p align="center">
  <b>Precision beyond the human hand.</b>
</p>

---

PreciCore is a surgical robotics project building the first dedicated robotic assistant for corneal surgery. The system combines tremor suppression, motion scaling, force feedback, and camera-guided needle positioning — all connected over a custom-built real-time communication protocol.

This organization hosts all software components of the PreciCore system.

---

## Repositories

### [`spine-go`](https://github.com/poisnoir/spine-go)
A lightweight, ROS-like robotics communication middleware written in Go. Provides pub/sub and RPC service calls over KCP/UDP with zero-config mDNS discovery and AES-GCM encrypted namespaces. Serves as the real-time communication backbone connecting all PreciCore modules.
**License:** MIT

---

### [`crackhead`](https://github.com/poisnoir/crackhead)
A MuJoCo-powered physics simulator for the PreciCore robotic arm and surgical environment. Used to develop, test, and validate control algorithms and needle trajectories on a virtual phantom cornea before any hardware is involved.
**License:** MIT

---

### [`purifier`](https://github.com/poisnoir/purifier)
A Kalman filter-based signal processing system for real-time tremor suppression and sensor noise reduction. Sits between raw operator input and the control system — turning shaky human movement into stable, precise commands.
**License:** MIT

---

### `precicore` *(private)*
The main robot control system. Integrates all modules into a working end-to-end pipeline — from operator input through Purifier and Spine-Go, to the STM32-driven robotic arm and camera vision system.
**License:** Proprietary

---

## Status

The project is currently in active development. Simulation and software infrastructure (Spine-Go, CrackHead, Purifier) are the current focus ahead of hardware prototyping.

---

## Team

Built by a team of Computer and Electrical Engineering students at Concordia University's Gina Cody School of Engineering and Computer Science, Montreal, QC.

---

<p align="center"><i>PreciCore is supported by District 3, Concordia University's startup incubator.</i></p>
