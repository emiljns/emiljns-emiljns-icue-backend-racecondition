# Corsair iCUE 5 – Configuration Write Loop & CPUID Deadlock  
**Security Advisory SA-2025-001 | Independent Analysis by Emil**

iCUE 5.x contains a critical backend flaw causing a high frequency write loop on `config.cuecfg` and log files.  
This leads to excessive disk I/O, SSD wear, and a dependent service (CPUID) failing to initialize, resulting in loss of temperature and fan control.

---

## 🔥 Key Problems
- Continuous rewrite loop on `config.cuecfg`
- ~1 GB/hour unnecessary disk writes
- NVMe/SSD wear amplification
- CPUID service stuck in **Starting**
- Cooling curves fail to load
- Sensor mapping corruption (swapped CPU/GPU sensors)
- No rollback mechanism, no archived builds

---

## 📄 Full Security Advisory  
See: **[SA-2025-001.md](SA-2025-001.md)**

---

## 📅 Disclosure Timeline  
See: **[DISCLOSURE-TIMELINE.md](DISCLOSURE-TIMELINE.md)**

---
