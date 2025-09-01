# Nebula Software.

This project is a secure loader that validates its **status** and **version** before injection.  
It ensures users are always running the latest version and prevents usage when the cheat is in a risky or disabled state.

---

## Features
- **Remote Status Validation**  
  - Loader fetches `status.txt` from the GitHub repository.  
  - Status can be:  
    - `undetected` → Safe to inject  
    - `detected` → Blocks injection for safety  
    - `updating` → Temporarily unavailable (auto-blocks injection)  
    - `development` → Experimental state (for testers/devs only)

- **Remote Version Control**  
  - Loader fetches `version.txt` from the GitHub repository.  
  - Compares against the local loader version.  
  - If outdated, it automatically launches the new loader version (if available).  

- **Injection Safety**  
  - Loader will not inject unless both **remote status** and **remote version** are validated.  

