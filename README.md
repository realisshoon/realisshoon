<div align="center">

# 한승훈 | RTL Design & Verification Engineer

**RTL을 설계하고, Simulation·Coverage·FPGA Validation으로 동작을 증명하는 엔지니어를 목표로 합니다.**

`SystemVerilog` · `UVM` · `Verilog HDL` · `AXI4-Lite` · `Zynq / FPGA`

[Portfolio](https://app.notion.com/p/ace61f2920548207b58d01260d14c80a) · [Email](mailto:hsgn21@naver.com)

</div>

---

## About Me

온디바이스 AI 시스템반도체 설계 과정에서 **RTL 설계부터 SystemVerilog/UVM 검증, SoC 통합, FPGA 구현**까지 경험했습니다.

설계와 검증을 분리해서 보지 않고, **DUT 구조와 프로토콜을 이해한 뒤 Test Scenario·Scoreboard·Coverage·Waveform으로 동작을 확인하는 과정**에 집중하고 있습니다.

- **Target**: RTL Verification Engineer / RTL·SoC Design Engineer
- **Verification**: UVM, SystemVerilog OOP, Directed/Random Test, Scoreboard, Functional Coverage
- **RTL / SoC**: AXI4-Lite, MMIO, FSM, SPI, I2C, UART, FIFO, RISC-V, CNN Accelerator
- **Implementation**: Vivado, Vitis, VCS, Verdi, Basys3, Zybo Z7-20
- **Work Style**: 명세·코드·파형·수치 결과를 기준으로 구현 범위와 검증 결과를 구분해 기록합니다.

## Verification Flow

`Spec / DUT 이해` → `Test Scenario` → `Self-checking Testbench` → `Scoreboard / Coverage` → `Waveform Debugging` → `FPGA Validation`

## Current Project

### [Zynq CNN Motion Robot SoC](https://github.com/realisshoon/zynq-cnn-motion-robot-soc) — In Progress

Zybo Z7-20 기반으로 **카메라 입력 → CNN Accelerator → Human Motion Data → Robot Arm / Virtual Arm**까지 연결하는 HW/SW 통합 프로젝트를 진행하고 있습니다.

- **My Focus**: CNN Accelerator RTL, Golden Model 기반 수치 검증, CNN subsystem integration
- **Architecture**: INT8 CNN datapath, line buffer, depthwise/pointwise convolution, requantization, postprocess
- **Verification**: Python Golden Model → directed vector → RTL simulation → bit-exact comparison
- **Integration**: Zynq PS/PL, AXI/DDR data path, camera frame processing 및 robot control interface
- **Status**: CNN 연산 블록과 control/dataflow를 단계적으로 구현·검증 중

> 진행 중인 프로젝트이므로 완료된 기능과 검증 결과만 저장소에 순차적으로 반영하고 있습니다.

## Featured Projects

| Project | What I Built | Verification / Result |
|---|---|---|
| **[FPGA VGA Conductor Game](https://github.com/realisshoon/fpga-vga-conductor-game)** | OV7670 영상에서 색상·좌표를 추출하고 FPGA에서 4박 패턴·BPM·음량·점수를 계산해 PC UI/MIDI와 연동 | RGB Detect UVM, module-level TB, FPGA-PC 통합 시연 |
| **[AXI4-Lite Multi-Peripheral SoC](https://github.com/realisshoon/axi4-lite-multi-peripheral-soc)** | MicroBlaze와 UART·Timer·I2C·SPI IP를 MMIO로 통합한 개인 SoC 프로젝트 | AXI-SPI UVM **32 Pass / 0 Fail**, Functional Coverage **100%** |
| **[SPI / I2C RTL & UVM Verification](https://github.com/realisshoon/spi_i2c_uvm)** | SPI Master/Slave RTL 설계, SPI/I2C UVM 환경 및 FPGA 통신 검증 | SPI **48 Pass / 0 Fail**, I2C **14 Pass / 0 Fail**, I2C Coverage **100%** *(team result)* |
| **[RV32I Single-Cycle CPU](https://github.com/realisshoon/RV32i-CPU)** | RV32I Datapath·Control Unit·Memory Interface 구현 | Instruction-level simulation 및 Bubble Sort 동작 확인 |

## Additional Verification / RTL Projects

- **[SystemVerilog UART / FIFO Verification](https://github.com/realisshoon/UART_OOP_Verification)**  
  Transaction·Generator·Driver·Monitor·Scoreboard 기반 self-checking 환경 구성  
  UART/FIFO Unit Test 및 UART RX–FIFO Integration Test 수행

- **[UART / FIFO / Sensor FPGA System](https://github.com/realisshoon/UART_FIFO_SENSOR_CLOCK)**  
  SR04·DHT11 Controller/Datapath, Watch/Stopwatch, 2-stage synchronizer 구현  
  `WNS 0.606 ns` · `WHS 0.094 ns` · `LUT 3.71%` · `FF 1.07%`

- **[Stopwatch / Watch RTL](https://github.com/realisshoon/STOPWATCH-WATCH_Verilog-HDL)**  
  FSM, Control Unit, FND MUX/Decoder 및 Basys3 FPGA 통합

## System Integration Experience

- **[Jetson Multi-Camera Tracking & Re-ID](https://github.com/realisshoon/jetson-multicam-re_id-tracking)**  
  4대 Jetson 보드, MQTT, 중앙 서버·DB를 통합해 인물 이동 경로와 재방문 판정을 구현한 팀 프로젝트  
  중앙 서버·DB 구조, 보드 간 메시지 흐름 및 통합 검증 담당

## Tech Stack

| Area | Stack |
|---|---|
| **HDL / Verification** | Verilog HDL, SystemVerilog, UVM |
| **Bus / Protocol** | AXI4-Lite, MMIO, SPI, I2C, UART |
| **Architecture** | FSM, FIFO, CDC Synchronizer, RISC-V RV32I, INT8 CNN Accelerator |
| **Tools / Board** | Vivado, Vitis, VCS, Verdi, Basys3, Zybo Z7-20 |
| **Programming** | C, Python, Linux |
| **Integration** | FPGA–PC UART, Zynq PS/PL, MQTT, Database |

## Current Focus

- Zynq 기반 INT8 CNN Accelerator의 RTL datapath/control 구조 구현
- Python Golden Model과 RTL simulation 간 bit-exact 검증
- 재사용 가능한 UVM component와 coverage-driven verification 역량 강화
- AXI/DDR 기반 IP integration 및 HW/SW register-level validation 심화
