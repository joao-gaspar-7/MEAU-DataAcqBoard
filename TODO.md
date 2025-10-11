# TODO List

This is the TODO template to be use during the development to track project tasks.

This file tracks pending features, bug fixes, and cleanup tasks for the project.  
Format:
- `[ ]` = not started  
- `[x]` = completed  
- `P1` = high priority, `P2` = medium, `P3` = low  

---

## Project Overview

**Project Name:** PROJECT-ID 

**Last Updated:** 2025-09-29

---

## Features

[x] **P1** Add routine to save relevant machine_state members to EERPOM (implemented solution relies on VCU EEPROM to save Drive Profile data - see aa_can_nvm_data)

[x] **P2** Add routine to configure/load data from RTC

[x] **P2** Add routine that updates machine_state time and date members from RTC values at boot (time and date members of machine_state were separated into their own struct to avoid racing conditions)

[x] **P1** Finish integration of remaining error messages from BMS

---

## Bugs

[x] **P2** Swap "+" and "-" buttons on page 2 of Drive Profile Setup Screen (visually only)

---

## Refactoring / Cleanup

---

## Testing

---

## Notes / Links
- Link to project documentation:
- Related issue tracker / repo:
