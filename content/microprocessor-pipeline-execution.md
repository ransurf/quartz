---
title: Microprocessor Pipeline Execution
---
Status: 
Tags: #cards/cmpt295/mp 
Links: [Microprocessor](out/microprocessor.md)
___

# Microprocessor Pipeline Execution
## Principles
- Start executing 1 instruction at each clock cycle
- Overlap different stages as different instructions are executing
- Higher throughput
[![Image from Gyazo](https://i.gyazo.com/a8e2b4038d7cd67ef544f50413b3ca25.png)](https://gyazo.com/a8e2b4038d7cd67ef544f50413b3ca25)
### Stages
> Assume each stage takes 80, register is 20
- Same as [Microprocessor Staged Execution](out/microprocessor-staged-execution.md#Stages FDEMW)
- Latency (Cost per instruction)
	- (400/5 ps + 20px)5 = 500ps
	- `# blocks x `longest cycle` = latency
- CPU throughput
	- 1 / `longest cycle` = throughput
	- 5/500ps = 10 GIPS
- CPI: 5
- Clock cycle: 80 + 20ps = 100ps

### Limitations
- Doubling number of stages would not double throughput
- Clock cycle would be limited by latency of the slowest stage
- Contains [Pipeline Hazards](out/pipeline-hazards.md)
- Same register is used after the same step, so there may be overwriting complications

___
References:

Created:: 2022-04-03 17:18
