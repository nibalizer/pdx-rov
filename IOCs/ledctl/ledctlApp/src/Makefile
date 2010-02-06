TOP=../..

include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================

#=============================
# Build the IOC application

PROD_IOC = ledctl
# ledctl.dbd will be created and installed
DBD += ledctl.dbd

# ledctl.dbd will be made up from these files:
ledctl_DBD += base.dbd

# Include dbd files from all support applications:
#ledctl_DBD += xxx.dbd

# Add all the support libraries needed by this IOC
#ledctl_LIBS += xxx

# ledctl_registerRecordDeviceDriver.cpp derives from ledctl.dbd
ledctl_SRCS += ledctl_registerRecordDeviceDriver.cpp

# Build the main IOC entry point on workstation OSs.
ledctl_SRCS_DEFAULT += ledctlMain.cpp
ledctl_SRCS_vxWorks += -nil-

# Add support from base/src/vxWorks if needed
#ledctl_OBJS_vxWorks += $(EPICS_BASE_BIN)/vxComLibrary

# Finally link to the EPICS Base libraries
ledctl_LIBS += $(EPICS_BASE_IOC_LIBS)

#===========================

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

