# ScienceMode2

|                                                              |                                                              |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Device                                                       | RehaStim2                                                    |
| Protocol                                                     | ScienceMode2                                                 |
| Stim. channels                                               | 8                                                            |
| Current (at 1 kΩ load)                                       | 0 – 126 mA (2 mA steps)                                      |
| Pulse width                                                  | 0; 20 – 500 μs (1 μs steps)                                  |
| Frequency                                                    | up to 40 Hz (using all 8 channels)                           |
| Pulse shape                                                  | Biphasic pulse                                               |
| Compatibility                                                | ScienceMode1, ScienceMode2 and ScienceMode3 are incompatible |
| Stimulation commands (from PC to the stimulation device)     | 1. Initialize Stimulation: • contains parameters that must be adjusted before start (frequency, activated channels, activated channels with partial frequencies)<br/>• The Stimulator initializes the values and is waiting for the start of the stimulation.<br/>2. Update/Start Stimulation:<br/>• contains parameters pulse width and current; the settings can be adjusted<br/>• The Stimulator starts the stimulation (as start) respectively adapts the transferred parameter (as update).<br/>• enables doublets/triplets (multiple impulses instead of only one)<br/>3. Stop Stimulation:<br/>• The Stimulator stops the Stimulation.<br/>4. Single Impulse:<br/>• contains as parameter one channel, one current and one pulse width.<br/>• The Stimulator has a single output of the impulse with adequate parameters |
| Typical scenario of the commands                             | Initialize, start, update, update, …, stop                   |
| Latency in the execution of stim. commands                   | 10 - 24 ms                                                   |
| Electrode error de-tection/feedback                          | Yes/Yes                                                      |
| Emergency stop availabl./feedback                            | Yes/Yes                                                      |
| MOTOmed control                                              | Yes, with 12 commands:<br/>1. Start, Stop arm/leg trainer:<br/>• set resistance, passive speed, flywheel<br/>mass, spasticity<br/>detection and more<br/>2. Information from<br/>MOTOmed<br/>• angles of the pedals,<br/>speed, torque<br/>• values of the particular<br/>phases of training:<br/>active performance,<br/>active distance, passive<br/>distance, symmetry<br/>(balance) |
| ScienceMode together with other programs (RehaMove, Sequence Mode) | It is not possible to use ScienceMode2 and other programs together. |
| C-Library and API                                            | No                                                           |
| Simulink<br/>Control*                                        | There is an open source Simulink block.<br/>http://sourceforge.net/projects/sciencestim/<br/>(MOTOmed commands are not implemented) |
| Simulink hardware and operation system<br/>support of open source block | • Simulation with Sync-<br/>Block (soft real-time) Win32/64, Linux32/64<br/>• Eclipse IDE /<br/>Embedded Coder (soft<br/>real-time) Win32/64, Linux32, Linux64 (not<br/>tested)<br/>Not yet supported<br/>• Real-Time Windows<br/>Target (hard real-time)<br/>• xPC-Target |

*Simulink is a block diagram environment for multidomain simulation and Model-Based Design. It supports system-level design, simulation, automatic code generation, and continuous test and verification of embedded systems. Simulink provides a graphical editor, customizable block libraries, and solvers for modeling and simulating dynamic systems. It is integrated with MATLAB, enabling you to incorporate MATLAB algorithms into models and export simulation results to MATLAB for further analysis.





