# Watlow-PM
EPICS module, IOC and OPI device support for the Watlow EZ-ZONE® PM Integrated PID Controller, Model Number: PM862FJ-3LEJAA

## Watlow Module
Templates to include in the makefile to build the database are listed below:
  - DB += Watlow_PM_Alarm.template
  - DB += Watlow_PM_General.template
  - DB += Watlow_PM_Limits.template
  - DB += Watlow_PM_Loop.template
  - DB += Watlow_PM_Monitor.template
  - DB += Watlow_PM_Output_1.template
  - DB += Watlow_PM_Output_2_and_3.template
  - DB += Watlow_PM.template
  - DB += Watlow_PM_IOC_Alarms.template
  - DB += Watlow_PM_Loop_PID.template
  - DB += pid_set_window.template
  - DB += Update_PID_Set.template

Templates included in the repository but not in the module:
  - DB += Watlow_PM_Analog_Input.template
  - DB += Watlow_PM_Linearization.template
  - DB += Watlow_PM_Process_Value.template
  
## Watlow IOC
The files included for building the IOC must be edited for the specific purposes of the end use developer.  Content of the substitution files and the st.cmd file have been removed prior to committing to the repository in order to maintain a generic level of information but maintain the core content.  

The st.cmd file has had all content removed other than the asyn configuration and Modbus register definitions.  This IOC was developed to work with the Modbus over TCP protocol however, the **drvAsynIPPortConfigure("watlow1", "", 0, 0, 0)** does not include the IP Address.

Rename the files and place in the appropriate directories.

Libraries included in the IOC build:
  - base.dbd
  - asSupport.dbd
  - modbusSupport.dbd
  - asyn.dbd
  - drvAsynIPPort.dbd
  - devIocStats.dbd
  - busySupport.dbd
  - calc.dbd


## Watlow OPI
Not all files included in the OPI folder are used.

The Watlow_Single.bob file was developed for the end user in mind.  The detailed UI, Watlow_Module.bob is linked in this interface.



## Release History
1.0:  Initial Release.

