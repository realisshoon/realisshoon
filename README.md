<div align="center">

# Han SeungHun

### RTL Design & Verification Engineer

**RTL을 설계하고, Simulation · Coverage · FPGA Validation으로 동작을 증명합니다.**

<br>

<img src="https://img.shields.io/badge/SystemVerilog-RTL-4A4A4A?style=for-the-badge">
<img src="https://img.shields.io/badge/UVM-Verification-2E8B57?style=for-the-badge">
<img src="https://img.shields.io/badge/AXI4--Lite-SoC-D97706?style=for-the-badge">
<img src="https://img.shields.io/badge/FPGA-Zynq-2563EB?style=for-the-badge">

<br><br>

[**Portfolio**](https://app.notion.com/p/ace61f2920548207b58d01260d14c80a)
&nbsp;&nbsp;•&nbsp;&nbsp;
[**GitHub**](https://github.com/realisshoon)
&nbsp;&nbsp;•&nbsp;&nbsp;
[**Email**](mailto:hsgn21@naver.com)

</div>

---

## 👋 About Me

- **RTL Design · Verification · SoC Integration · FPGA Implementation**을 경험하고 있습니다.
- DUT와 Protocol을 이해한 뒤 **Test Scenario → Scoreboard → Coverage → Waveform Debug**로 동작을 검증합니다.
- 현재는 **Zynq 기반 INT8 CNN Accelerator RTL 설계 및 검증**을 진행하고 있습니다.

> **Target**  
> RTL Verification Engineer / RTL · SoC Design Engineer

---

# 🚀 Current Project

## Zynq CNN Motion Robot SoC

[![Repository](https://img.shields.io/badge/GitHub-View_Repository-181717?style=flat-square&logo=github)](https://github.com/realisshoon/zynq-cnn-motion-robot-soc)
![Status](https://img.shields.io/badge/Status-In_Progress-F59E0B?style=flat-square)

**카메라에서 사람의 움직임을 인식하고 FPGA CNN Accelerator에서 처리한 Human Motion Data로 실제·가상 로봇팔을 제어하는 시스템입니다.**

```mermaid
flowchart LR
    A[Camera] --> B[MIPI CSI / Video Pipeline]
    B --> C[DDR Frame Buffer]
    C --> D[INT8 CNN Accelerator]
    D --> E[Pose / Coordinate]
    E --> F[Human Motion Data]
    F --> G[Robot Arm]
    F --> H[Virtual Arm]
```

### My Focus

`CNN Accelerator RTL`
&nbsp; `Golden Model Verification`
&nbsp; `INT8 Datapath`
&nbsp; `System Integration`

| Module | Status | Verification |
|---|:---:|---|
| **Postprocess** | ✅ | Python Golden Model ↔ RTL Bit-exact |
| **Depthwise Conv PE** | ✅ | Directed Vector / RTL Simulation |
| **Pointwise Conv PE** | 🛠 | RTL / Verification 진행 |
| **CNN Top / Dataflow** | 🛠 | Integration 진행 |
| **Zynq System Integration** | 🛠 | PS/PL · AXI/DDR 연동 진행 |

### Verification Strategy

```mermaid
flowchart LR
    A[Python<br>Golden Model]
    --> B[Test Vector]
    --> C[RTL Simulation]
    --> D[Bit-exact Compare]
    --> E[Waveform Debug]
```

> 진행 중인 프로젝트로, **구현·검증이 완료된 기능과 진행 중인 기능을 구분하여 기록**하고 있습니다.

---

# ⭐ Featured Projects

<table>
<tr>

<td width="50%" valign="top">

### 🎥 FPGA VGA Conductor Game

<a href="https://github.com/realisshoon/fpga-vga-conductor-game">
<img src="https://raw.githubusercontent.com/realisshoon/fpga-vga-conductor-game/main/docs/images/demo-pattern-playing.jpg" width="100%">
</a>

<br>

`SystemVerilog` `UVM` `OV7670` `UART`

**OV7670 → RGB Detect → Pattern FSM → BPM/Volume → PC UI**

- RGB Filter / Coordinate Detect Integration
- Top RTL Integration
- RGB Detect UVM
- FPGA ↔ PC UART Integration

<br>

[**→ View Repository**](https://github.com/realisshoon/fpga-vga-conductor-game)

</td>

<td width="50%" valign="top">

### 🔗 AXI4-Lite Multi-Peripheral SoC

<a href="https://github.com/realisshoon/axi4-lite-multi-peripheral-soc">
<img src="https://raw.githubusercontent.com/realisshoon/axi4-lite-multi-peripheral-soc/main/docs/assets/slide-3.png" width="100%">
</a>

<br>

`AXI4-Lite` `MicroBlaze` `UVM` `MMIO`

**MicroBlaze + AXI Interconnect + Custom Peripheral**

- UART · Timer · I2C · SPI Integration
- AXI4-Lite Register / MMIO
- Vitis HW/SW Integration
- Basys3 FPGA Validation

**UVM : 32 Pass / 0 Fail · Coverage 100%**

<br>

[**→ View Repository**](https://github.com/realisshoon/axi4-lite-multi-peripheral-soc)

</td>

</tr>

<tr>

<td width="50%" valign="top">

### 🧪 SPI / I2C RTL & UVM

<a href="https://github.com/realisshoon/spi_i2c_uvm">
<img src="https://raw.githubusercontent.com/realisshoon/spi_i2c_uvm/main/docs/assets/slide-7.png" width="100%">
</a>

<br>

`SystemVerilog` `UVM` `SPI` `I2C`

**Peripheral RTL → UVM → FPGA Board Validation**

- SPI Master / Slave RTL
- UVM Driver · Monitor · Scoreboard
- Functional Coverage
- Board-to-Board Communication

**SPI : 48 Pass / 0 Fail**  
**I2C : 14 Pass / 0 Fail · Coverage 100%** *(Team Result)*

<br>

[**→ View Repository**](https://github.com/realisshoon/spi_i2c_uvm)

</td>

<td width="50%" valign="top">

### 🧠 RV32I Single-Cycle CPU

<a href="https://github.com/realisshoon/RV32i-CPU">
<img src="https://raw.githubusercontent.com/realisshoon/RV32i-CPU/main/docs/assets/architecture.png" width="100%">
</a>

<br>

`SystemVerilog` `RISC-V` `RTL` `Vivado`

**Instruction Fetch → Decode → Execute → Memory → Write-back**

- Datapath
- Control Unit
- Register File
- ALU / Memory Interface
- Branch / JAL / JALR

**Bubble Sort Program Simulation 검증**

<br>

[**→ View Repository**](https://github.com/realisshoon/RV32i-CPU)

</td>

</tr>
</table>

---

# 🔍 Verification Workflow

```mermaid
flowchart LR
    A["SPEC / DUT<br>Understanding"]
    --> B["Test<br>Scenario"]
    --> C["Self-checking<br>Testbench"]
    --> D["Scoreboard"]
    --> E["Functional<br>Coverage"]
    --> F["Waveform<br>Debug"]
    --> G["FPGA<br>Validation"]
```

### What I Verify

`Protocol Timing`
&nbsp; `Handshake`
&nbsp; `FSM Transition`
&nbsp; `Corner Case`
&nbsp; `Data Integrity`
&nbsp; `Coverage`

---

# 🧩 Additional RTL / Verification Projects

| Project | Core | Result |
|---|---|---|
| [**UART / FIFO OOP Verification**](https://github.com/realisshoon/UART_OOP_Verification) | SystemVerilog OOP · Scoreboard | UART/FIFO Unit + Integration Test |
| [**UART / FIFO / Sensor FPGA System**](https://github.com/realisshoon/UART_FIFO_SENSOR_CLOCK) | UART · FIFO · SR04 · DHT11 | WNS **0.606 ns**, WHS **0.094 ns** |
| [**Stopwatch / Watch RTL**](https://github.com/realisshoon/STOPWATCH-WATCH_Verilog-HDL) | FSM · Datapath · FPGA | Basys3 Implementation |
| [**Jetson Multi-Camera Tracking**](https://github.com/realisshoon/jetson-multicam-re_id-tracking) | Jetson · MQTT · DB | 4-board System Integration |

---

# 🛠 Tech Stack

### HDL / Verification

![Verilog](https://img.shields.io/badge/Verilog-RTL-4A4A4A?style=flat-square)
![SystemVerilog](https://img.shields.io/badge/SystemVerilog-Verification-2563EB?style=flat-square)
![UVM](https://img.shields.io/badge/UVM-1.2-2E8B57?style=flat-square)

### SoC / Protocol

![AXI4-Lite](https://img.shields.io/badge/AXI4--Lite-SoC-D97706?style=flat-square)
![SPI](https://img.shields.io/badge/SPI-Protocol-6B7280?style=flat-square)
![I2C](https://img.shields.io/badge/I2C-Protocol-6B7280?style=flat-square)
![UART](https://img.shields.io/badge/UART-Protocol-6B7280?style=flat-square)
![MMIO](https://img.shields.io/badge/MMIO-Register_Interface-6B7280?style=flat-square)

### Architecture

![FSM](https://img.shields.io/badge/FSM-Control-7C3AED?style=flat-square)
![FIFO](https://img.shields.io/badge/FIFO-Buffer-7C3AED?style=flat-square)
![RISC-V](https://img.shields.io/badge/RISC--V-RV32I-7C3AED?style=flat-square)
![CNN](https://img.shields.io/badge/CNN-INT8_Accelerator-7C3AED?style=flat-square)

### FPGA / Tools

![Vivado](https://img.shields.io/badge/Vivado-FPGA-E01F27?style=flat-square)
![Vitis](https://img.shields.io/badge/Vitis-Embedded-E01F27?style=flat-square)
![VCS](https://img.shields.io/badge/VCS-Simulation-8B5CF6?style=flat-square)
![Verdi](https://img.shields.io/badge/Verdi-Debug-8B5CF6?style=flat-square)
![Basys3](https://img.shields.io/badge/Basys3-Artix--7-0F766E?style=flat-square)
![Zybo](https://img.shields.io/badge/Zybo_Z7--20-Zynq--7000-0F766E?style=flat-square)

### Programming

![Python](https://img.shields.io/badge/Python-Development-3776AB?style=flat-square)
![C](https://img.shields.io/badge/C-Embedded-555555?style=flat-square)
![Linux](https://img.shields.io/badge/Linux-Development-FCC624?style=flat-square)

---

# 🎯 Current Focus

<table>
<tr>
<td>🧠 <b>INT8 CNN Accelerator</b></td>
<td>RTL Datapath / Control Architecture</td>
</tr>

<tr>
<td>🔬 <b>Bit-exact Verification</b></td>
<td>Python Golden Model ↔ RTL Simulation</td>
</tr>

<tr>
<td>🧪 <b>UVM Verification</b></td>
<td>Scoreboard / Coverage / Corner Case</td>
</tr>

<tr>
<td>🔗 <b>SoC Integration</b></td>
<td>AXI / DDR / PS-PL Integration</td>
</tr>

<tr>
<td>⏱ <b>FPGA Implementation</b></td>
<td>Timing / Resource / Critical Path</td>
</tr>
</table>

---

<div align="center">

### 📫 Contact

**Han SeungHun**

[Portfolio](https://app.notion.com/p/ace61f2920548207b58d01260d14c80a)
&nbsp; · &nbsp;
[GitHub](https://github.com/realisshoon)
&nbsp; · &nbsp;
[Email](mailto:hsgn21@naver.com)

<br>

**RTL Design · Verification · SoC Integration · FPGA**

</div>
