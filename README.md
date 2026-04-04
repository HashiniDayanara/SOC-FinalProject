# SOC-FinalProject

## Setup NEORV32 IP

### Prerequisites
Clone the NEORV32 repository close to your `C:` drive:
```bash
git clone https://github.com/stnolting/neorv32.git
```

### Steps
1. Open the TCL shell in Vivado via **Window → Tcl Console**

2. Navigate to the system integration folder:
```tcl
cd C:/neorv32/rtl/system_integration
```

3. Execute the IP packaging script:
```tcl
source neorv32_vivado_ip.tcl
```

4. A second Vivado instance will open automatically to package the IP — it will close on its own when done

5. A new folder `neorv32_vivado_ip_work` will be created inside `neorv32/rtl/system_integration` containing the IP-packaging Vivado project

6. The `packaged_ip` sub-folder contains the actual IP module, which is automatically added to the project's IP repository

7. Find the NEORV32 in the **User Repository** section of the Vivado IP catalog

## Project Setup 
1. Create project using provided constraints file

2. Use part number `xc7s50csga324-1`

3. Use the provided .tcl script 
```bash
cd path/to/SOC-FinalProject
source ./final_project.tcl
```

## Source Control 
4. Save new .tcl file for source control
```bash
write_bd_tcl -force path/to/SOC-FinalProject/final_project.tcl 
```