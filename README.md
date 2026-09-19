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
| **Pointwise Conv PE** | ✅ | RTL Regression / Review-ready |
| **CNN Top / Dataflow** | 🛠 | Integration 진행 |
| **Zynq System Integration** | 🛠 | PS/PL · AXI/DDR 연동 진행 |

### Engineering Approach

```mermaid
flowchart LR
    A[Spec / Golden Model]
    --> B[RTL Implementation]
    --> C[Directed Vector]
    --> D[RTL Simulation]
    --> E[Bit-exact Compare]
    --> F[Waveform Debug]
```

> CNN 연산은 Python Golden Model을 기준으로 비교하며,  
> **단순히 동작 여부만 확인하지 않고 정수 연산 결과가 기준 모델과 일치하는지 검증**하고 있습니다.

> 현재 진행 중인 프로젝트로, **완료된 기능과 진행 중인 기능을 구분하여 기록**하고 있습니다.

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

**My Role**
- RGB Filter · Coordinate Detection Integration
- Top RTL · FPGA-PC Integration
- RGB Detect UVM
- Repository / Branch Integration

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

**32 Pass / 0 Fail · Functional Coverage 100%**

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

**My Role**
- SPI Master / Slave RTL
- SPI Full-Duplex 검증
- Waveform Debug
- FPGA Board Validation

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

**Fetch → Decode → Execute → Memory → Write-back**

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

# 🛠 Troubleshooting & Debugging

> 결과만 기록하지 않고, **문제 발견 → 원인 분석 → 수정 → 재검증** 과정을 중요하게 생각합니다.

| Case | How I Found It | Root Cause / Action | Result |
|---|---|---|---|
| **⏱ Setup Timing Violation** | Vivado Implementation의 Timing Report에서 Setup Slack 문제 확인 | Worst Path에서 `60000 / count_reg` Divider 경로 확인 → FSM의 데이터 유효 시점을 분석해 Multicycle Path 적용 | Setup/Hold Constraint 적용 후 Timing 재확인 |
| **🧪 I2C Coverage Hole** | Functional Coverage **85.71%**, ACK/NACK bin **0%** 확인 | Waveform에서 ACK Sampling 시점 오류 확인 → 9번째 SCL High 기준으로 Driver 수정 | **14 Pass / 0 Fail · Coverage 100%** |
| **🔄 UART/FIFO Event Loss** | 통합 동작에서 일부 Control Event 누락을 Waveform으로 추적 | FIFO 상태와 1-cycle Pulse의 생성·소비 시점 불일치 확인 → Pulse Timing 조정 | UART/FIFO 통합 동작 재검증 |

<details>
<summary><b>🔎 Case Study — Setup Timing Violation 상세 보기</b></summary>

<br>

### 1. Problem

Functional Simulation에서는 정상적으로 동작했지만,  
Vivado Implementation 이후 Timing Report에서  
**BPM 계산 경로의 Setup Timing 문제**를 확인했습니다.

### 2. Analysis

Worst Timing Path를 추적한 결과,  
지휘 간격을 BPM으로 변환하는 다음 나눗셈 연산이  
긴 Combinational Path를 형성하고 있음을 확인했습니다.

```systemverilog
bpm_calc = 16'd60000 / count_reg;
```

단순히 Clock 주기를 낮추거나 Constraint를 추가하기 전에  
해당 계산 결과가 **실제로 언제 필요한 데이터인지 FSM을 기준으로 다시 분석**했습니다.

```text
COUNT
  ↓
WAIT
  ↓
CALC
  ↓
COMP
```

`count_reg`는 지휘 간격 측정이 끝난 뒤 유지되며,  
BPM 계산 결과는 `WAIT → CALC` 단계를 거쳐 사용됩니다.

따라서 해당 경로의 결과가 반드시  
**다음 1 Clock 안에 도착해야 하는 구조가 아님을 확인**했습니다.

### 3. Action

실제 데이터 유효 시점에 맞춰  
`count_reg → reg_bpm_comp` 경로를 **3-cycle Multicycle Path**로 정의했습니다.

```tcl
set_multicycle_path 3 -setup \
-from [get_pins {U_GAME_LOGIC/u_speed_calc/count_reg_reg[*]/C}] \
-to   [get_pins {U_GAME_LOGIC/u_speed_calc/reg_bpm_comp_reg*[*]/D}]

set_multicycle_path 2 -hold \
-from [get_pins {U_GAME_LOGIC/u_speed_calc/count_reg_reg[*]/C}] \
-to   [get_pins {U_GAME_LOGIC/u_speed_calc/reg_bpm_comp_reg*[*]/D}]
```

### 4. Takeaway

Timing Violation을 단순히 Constraint로 숨기는 것이 아니라,

**Timing Report → Critical Path → RTL 연산 → FSM 데이터 유효 시점**

순서로 원인을 확인한 뒤  
설계 의도에 맞는 Timing Constraint를 적용했습니다.

[**→ View FPGA VGA Conductor Game**](https://github.com/realisshoon/fpga-vga-conductor-game)

</details>

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
&nbsp; `Coverage Closure`

---

# 🧩 Additional RTL / Verification Projects

| Project | Core Tech | Result |
|---|---|---|
| [**UART / FIFO OOP Verification**](https://github.com/realisshoon/UART_OOP_Verification) | SystemVerilog OOP · Scoreboard | UART/FIFO Unit + Integration Test |
| [**UART / FIFO / Sensor FPGA System**](https://github.com/realisshoon/UART_FIFO_SENSOR_CLOCK) | UART · FIFO · SR04 · DHT11 | WNS **0.606 ns** · WHS **0.094 ns** |
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
![MMIO](https://img.shields.io/badge/MMIO-Register_Interface-6B7280?style=flat-square)
![SPI](https://img.shields.io/badge/SPI-Protocol-6B7280?style=flat-square)
![I2C](https://img.shields.io/badge/I2C-Protocol-6B7280?style=flat-square)
![UART](https://img.shields.io/badge/UART-Protocol-6B7280?style=flat-square)

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

### Programming / Environment

![Python](https://img.shields.io/badge/Python-Golden_Model-3776AB?style=flat-square)
![C](https://img.shields.io/badge/C-Embedded-555555?style=flat-square)
![Linux](https://img.shields.io/badge/Linux-Development-FCC624?style=flat-square)

---

<div align="center">

## 📫 Contact

**Han SeungHun**

[**Portfolio**](https://app.notion.com/p/ace61f2920548207b58d01260d14c80a)
&nbsp; · &nbsp;
[**GitHub**](https://github.com/realisshoon)
&nbsp; · &nbsp;
[**Email**](mailto:hsgn21@naver.com)

<br>

**RTL Design · Verification · SoC Integration · FPGA**

</div>
