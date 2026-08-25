<div align="center">

# 한승훈 | RTL Verification Engineer

**RTL을 이해하고, 검증 결과로 설계 품질을 설명하는 엔지니어를 목표로 합니다.**

`SystemVerilog` · `UVM` · `AXI4-Lite` · `Verilog HDL` · `FPGA`

[Portfolio](https://app.notion.com/p/ace61f2920548207b58d01260d14c80a) · [Email](mailto:hsgn21@naver.com)

</div>

---

## About Me

온디바이스 AI 시스템반도체 설계 과정에서 **RTL 설계부터 SystemVerilog/UVM 검증, SoC 통합, FPGA 구현**까지 경험했습니다.

설계와 검증을 분리해서 보지 않고, **DUT 구조와 프로토콜을 이해한 뒤 Test Scenario·Scoreboard·Coverage·Waveform으로 동작을 확인하는 과정**에 집중하고 있습니다.

- **Target**: RTL Verification Engineer → RTL / SoC Design Engineer
- **Verification**: UVM, SystemVerilog OOP, Directed/Random Test, Scoreboard, Functional Coverage
- **RTL / SoC**: AXI4-Lite, MMIO, FSM, SPI, I2C, UART, FIFO, RISC-V
- **Implementation**: Vivado, Vitis, VCS, Verdi, Basys3 FPGA
- **Work Style**: 구현 범위와 팀 결과를 구분하고, 확인 가능한 코드·파형·수치로 기록합니다.

## Verification Flow

`DUT / Protocol 이해` → `Test Scenario` → `Self-checking Testbench` → `Scoreboard / Coverage` → `Waveform Debugging`

## Featured Projects

| Project | What I Built | Verification / Result |
|---|---|---|
| **[SPI / I2C RTL & UVM Verification](https://github.com/realisshoon/spi_i2c_uvm)** | SPI Master/Slave RTL 설계, SPI/I2C UVM 환경 및 FPGA 통신 검증 | SPI **48 Pass / 0 Fail**, I2C **14 Pass / 0 Fail**, I2C Coverage **100%** *(team result)* |
| **[AXI4-Lite Multi-Peripheral SoC](https://github.com/realisshoon/axi4-lite-multi-peripheral-soc)** | MicroBlaze와 UART·Timer·I2C·SPI IP를 MMIO로 통합한 개인 SoC 프로젝트 | AXI-SPI UVM **32 Pass / 0 Fail**, Functional Coverage **100%** |
| **[SystemVerilog UART / FIFO Verification](https://github.com/realisshoon/UART_OOP_Verification)** | Transaction·Generator·Driver·Monitor·Scoreboard 기반 self-checking 환경 | UART, FIFO Unit Test 및 UART RX–FIFO Integration Test |
| **[RV32I Single-Cycle CPU](https://github.com/realisshoon/RV32i-CPU)** | RV32I Datapath·Control Unit·Memory Interface 구현 | Instruction-level simulation 및 Bubble Sort 동작 확인 |

## Additional RTL Projects

- **[UART / FIFO / Sensor FPGA System](https://github.com/realisshoon/UART_FIFO_SENSOR_CLOCK)**  
  SR04·DHT11 Controller/Datapath, Watch/Stopwatch, 2-stage synchronizer 구현  
  `WNS 0.606 ns` · `WHS 0.094 ns` · `LUT 3.71%` · `FF 1.07%`

- **[Stopwatch / Watch RTL](https://github.com/realisshoon/STOPWATCH-WATCH_Verilog-HDL)**  
  FSM, Control Unit, FND MUX/Decoder 및 Basys3 FPGA 통합

## Tech Stack

| Area | Stack |
|---|---|
| **HDL / Verification** | Verilog HDL, SystemVerilog, UVM |
| **Bus / Protocol** | AXI4-Lite, MMIO, SPI, I2C, UART |
| **Architecture** | FSM, FIFO, CDC Synchronizer, RISC-V RV32I |
| **Tools / Board** | Vivado, Vitis, VCS, Verdi, Basys3 |
| **Programming** | C, Python, Linux |

## Current Focus

- Coverage와 corner case를 기준으로 설명 가능한 Verification Plan 구성
- 재사용 가능한 UVM component와 protocol verification 역량 강화
- AXI 기반 IP integration 및 HW/SW register-level validation 심화
