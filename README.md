# JMeter Assignment

This repository contains the results of Load, Endurance, and Spike testing performed on a test API using JMeter.  

## Load Test
- **Purpose:** Determine the maximum sustainable load the system can handle with error rate below 1%.  
- **Configuration:**  
  - Threads (users): 900 (baseline)  
  - Ramp-up: 3 seconds
  - Duration: until steady-state achieved  
- **Results:**  
  - Maximum sustainable load: 900 threads  
  - Error % remained below 1%  

## Endurance Test
- **Purpose:** Verify system stability under sustained load for a long period.  
- **Configuration:**  
  - Threads: 900 (maximum sustainable load)  
  - Thread lifetime: 600 seconds (10 minutes)  
  - Ramp-up: 3 seconds  
- **Results:**  
  - System remained stable under sustained load  
  - Error % stayed below 1%  

## Spike Test
- **Purpose:** Observe system behavior under sudden extreme load.  
- **Configuration:**  
  - Threads: 1500 (1.5× baseline)  
  - Ramp-up: 3 seconds  
  - Thread lifetime: 120 seconds  
- **Results:**  
  - Expected higher error % due to sudden load spike  
  - Response times spiked as expected  


## Files Included

- [TestPlan.jmx](./TestPlan.jmx) — JMeter test plan  
- [load_results.jtl](./load_results.jtl) — Load test results  
- [load_results.html](./load.html) — Load test results
- [endurance_results.html](./endurance.html) — Endurance test results

