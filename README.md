# Katmai_Firmware
Katmai - Quantum Hardware you can hold in your hand. 



Below is one way to rank these core tasks by **overall importance** (i.e., what must be robust to keep the system safe and functional). Actual priority ordering will vary by application, but this gives a general sense of what typically matters most first:

1. **Fault Monitoring and Safety**  
   - Protects hardware and users.  
   - Monitors critical parameters (voltage, current, temperature).  
   - Shuts down or corrects operations if limits are exceeded.

2. **System Initialization**  
   - Establishes a stable hardware and firmware foundation (clocks, power, watchdog, GPIO).  
   - Must be performed correctly for the rest of the system to function reliably.

3. **Coil Driver Control**  
   - Directly responsible for energizing and managing coil power.  
   - Involves PWM, current/voltage regulation, and ensuring no hardware damage.

4. **ADC Interface**  
   - Critical for acquiring precise sensor data and enabling feedback/control loops.  
   - Must be accurate and well-timed to provide meaningful information to the rest of the system.

5. **Transmit/Receive Driver**  
   - Enables communication (commands in, data out), but system can often still function (at least locally) without a link.  
   - Important for remote configuration, diagnostics, or data logging, yet secondary to immediate safety/control tasks.

6. **Configuration and Diagnostics**  
   - Useful for calibration, system updates, and debug.  
   - While important for usability and long-term maintenance, the system can usually run in a default state without these.
