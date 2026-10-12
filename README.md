# Poster Abstract

**Background.** Electric motors drive critical equipment like pumps and fans, emitting distinct vibration signatures before mechanical failure. Unplanned breakdowns cause high operational costs and downtime. Existing monitoring relies on manual inspections that miss sudden faults or cloud systems burdened by high latency, bandwidth consumption, and network dependency. This project evaluates an offline Edge-AI solution on a low-cost STM32 microcontroller for real-time motor fault classification without cloud infrastructure.

**Methods.** Conducted at Dedan Kimathi University of Technology, the setup uses a motor test rig simulating shaft unbalance and structural looseness. An ADXL345 accelerometer rigidly mounted to the motor casing streams vibration data via SPI/I2C through a custom KiCad PCB shield to an STM32F411CEU6 MCU. On-chip features (RMS, Kurtosis, Crest Factor, CMSIS-DSP FFT) are processed by an INT8 quantized machine learning model deployed via ST X-CUBE-AI for local inference.

**Results.** The pipeline targets $\ge 90\%$ classification accuracy across healthy, unbalance, and looseness states on the test rig. INT8 quantization enables sub-$100\text{ ms}$ execution per cycle within the MCU's memory constraints ($512\text{ KB}$ Flash, $128\text{ KB}$ SRAM), providing $100\%$ offline fault detection without cloud or PC dependency.

**Conclusions.** Low-cost microcontrollers can replace cloud-dependent condition monitoring platforms through localized, real-time vibration diagnostics. Combining direct adhesive sensing, DSP feature extraction, and quantized neural networks eliminates network latency and inspection delays, delivering an accessible predictive maintenance tool for industrial operators.
