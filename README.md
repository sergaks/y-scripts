# y-scripts

Collection of hybris developer's bash scripts that:
 - simplify work process with multiple hybris project
 - allow using system wide commands and aliases  
 - enhance operations of initialization/update with error verifications
 - decompile all hybris jars

## Installation
- Clone or download this repository
- Add path to the folder to your system PATH (add line to ~/bash_profile)

```bash
export PATH="$PATH:~/y-scripts"
```

## Usage
- Open shell and navigate to a hybris folder - usually it's project/repository root. It isn't required to open hybris/bin/platform dir and setantenv.
- Scripts can identify where is nearest hybris platform based on current working directory
- If there is ambiguity in hybris platform selection scripts fail and returns non-zero code

### y-whereis
Service script - identifies where is hybris platform located based on current working directory

### y-ant
Wrapper for hybris platform's ant with calls of `. .\setantenv.sh`

### y-server
Alias for hybrisserver.sh in hybris platform

### y-install
Alias for hybris installer

### y-init
Performs hybris initialize and analyses errors in logs. 
Prints errors and warning in case of there are any failures in logs and returns non-zero code in this case

### y-update
Performs hybris update and analyses errors in logs. 
Prints errors and warning in case of there are any failures in logs and returns non-zero code in this case

### y-test
Runs all hybris tests for custom extensions. Optionally can be passed parameter for filtering list of custom 
extensions (grep).
```bash
y-test services
```
### y-decompile
Decompiles all hybris jar files using CFR decompiler

### y-build
Alias for and build with disabled items.xml verification to speed up rebuilding

### y-debug
Alias for hybris server start in debug mode

### y-up
Alias for ant all and hybrisserver start in debug mode