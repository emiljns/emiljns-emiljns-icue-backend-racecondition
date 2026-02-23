# Corsair iCUE 5 Configuration Write Loop and CPUID Service Deadlock  
TA-2025-001 | Independent Technical Analysis by Emil

iCUE 5.x contains a backend defect that triggers a high frequency write loop affecting `config.cuecfg` and associated log files.  
This behavior results in excessive disk activity, accelerated SSD or NVMe wear, and failure of the dependent CPUID service to initialize properly. In affected systems this may result in loss of temperature telemetry and fan or pump control.

This document is classified as a Technical Advisory. No security boundary violation or privilege escalation has been demonstrated.

---

## Key Problems

- Continuous rewrite loop on `config.cuecfg`
- Approximately 1 GB per hour unnecessary disk writes
- SSD or NVMe endurance amplification
- CPUID service stuck in Starting state
- Cooling curves fail to load
- Sensor mapping inconsistencies in some configurations
- No official rollback archive available

---

## Full Technical Advisory  
See: **SA-2025-001.md**

---

## Disclosure Timeline  
See: **DISCLOSURE-TIMELINE.md**
