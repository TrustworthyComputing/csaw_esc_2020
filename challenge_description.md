ESC 2020 Challenge Description
==============================


The theme of this year's ESC competition is **exploiting the firmware of a custom IoT WiFi access point**. IoT are embedded devices that are widely in the modern smart infrastructure, including smart homes, wireless sensor networks, wearables and connected cars. While it is possible to launch network-level attacks to connected devices, this year's challenge will go one step further, tasking the contestants to reverse engineer the custom Wi-Fi access point's firmware and break the security of the system. Contestants will be provided with a **HiFive1-revB** IoT board with the corresponding firmware binary, and will utilize open-source reverse engineering tools hack the system.

The ESC 2020 competition will strengthen students' understanding of firmware exploitation and familiarize them with industry tools in an interactive environment.

See the [grading details](#evaluation-and-grading-policies) below for more information on evaluation.


## Challenge structure

The ESC20 competition is divided into three phases:

1. A preliminary **qualification phase**, where teams must compile and submit a written report characterizing exploits and reverse engineering techniques that they utilized to break a provided RISC-V program.

2. A **final phase**, where qualified teams are invited to the *CSAW virtual event* of their region to present and demonstrate their attack implementations on the custom systems provided by the organizers.

3. A **timed-attack phase**, where qualified teams will be provided with a special challenge binary on the day of the virtual ESC finals in their region. The contestants will then race to solve the challenge, demonstrating their reverse engineering prowess!

See below for more details on the requirements of each phase.


### Qualification Phase

For the qualification phase, participating teams are invited to **reverse engineer** a provided [qualification binary](https://github.com/TrustworthyComputing/csaw_esc_2020/blob/master/qual-esc2020.elf) using open-source reverse-engineering tools and recover secret values that unlock its functionality using different approaches and techniques. To qualify for the final phase, the teams should submit a **short report** that outlines their approaches and techniques (not necessarily only one approach/technique) utilized to reverse engineer the provided binary. To that end, the report should also explore existing techniques on the topic, focusing on (but not necessarily limited to) firmware exploitation and RISC-V hacking. The best approaches will include a discussion of existing techniques, a clear outline of reverse engineering methodologies, and a demonstration of the success and effectiveness of the team's methodology.

Qualification phase reports will be evaluated by a team of experts, and will take into account the **correctness** and **creativity** of the applied reverse-engineering techniques, as well as the completeness and quality of the compiled report.

Hint 1: `qemu-system-riscv32 -nographic -machine sifive_e -kernel file.elf`

Hint 2: Some [clones](https://github.com/mumbel/ghidra_riscv.git) are more important than others.


### Final Phase

The top teams of each region (US-Canada, Europe, MENA, India) will qualify for the final phase, which will require **implementing** and **demonstrating** firmware-level reverse-engineering of different RISC-V programs. Each exploited program will be worth a number of points depending on its difficulty.

A detailed description of the final phase will be provided when the finalists are announced.

The teams should compose a **final report** detailing their approaches. The definitive goal is to demonstrate their methods during the finals.

### Timed-Attack Phase

On the day of the virtual finals, each region will receive a timed-attack challenge binary. This binary will have a new challenge that teams will race to solve as quickly as possible during the competition. Teams should be prepared with the provided RISC-V board and be able to program it with a vulnerable payload to defeat this timed challenge. As this phase is a race, the first team to successfully solve the challenge completely will receive 200 extra points to their final challenge score. The second team will receive 100 extra points, and the third team will receive 50 extra points (other teams will not receive extra points).


## Evaluation and Grading Policies

The evaluation of the finalists will be the responsibility of a team of **expert judges** in each region. During the virtual finals, each team should be able to answer the questions posed by the judges and **demonstrate their methods**. Furthermore, the finalists will prepare a **Powerpoint presentation** of their work and a **short video** to present on the day of the finals, complementing their submitted **final report**. During the virtual finals, each team should be ready to demonstrate their solved challenges.

The final phase will be graded as follows:
- 50% of the final score will be correctness. The points awarded in this section are based on successfully solving the provided challenges and depend on the difficulty of each challenge. The awarded points will be determined automatically by the provided firmware.
- 10% of the score will be performance and efficiency. Performance will be evaluated by a team of expert judges and will encompass the techniques that the participants utilize to solve the challenges. For example, utilizing an exhaustive test for every possible answer would be rated as very inefficient, whereas a solution that examines a process and can determine an exact solution would be rated as very efficient.
- 10% of the score will be novelty. This will be judged based on the uniqueness of the solution methodology by the team of expert judges.
- 30% of the score will be the quality of the final report, video and presentation. The final report will be graded based on organization, clearness of presentation, and detail of explanations. This will also be judged by the team of expert judges.

 **Note that use of software tools requiring a paid license or a demo license of a non-free tool is not allowed**.


You can refer to the [deliverables section](logistics.md#deliverables) for more details on the qualification and final phase deliverables.


To find more information regarding how to register and participate click [here](logistics.md).
