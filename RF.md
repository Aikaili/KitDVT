# Functional Requirements

##RF distance from host to 1 slave is 10 meters
### Setup  
- Slave ID 2001
- Network X1000
- Channel 15
- TX Power -6 dBm
- Time Slot 1sec
- Encryption Key ABCDEFGHIJKLMNOP
- Firmware Version 1.00

####Add a 2" slave

1. Measure 10 meters from USB host to one 2" slave device.
1. Open Adaptag Manager
1. Deselect 1401 and 2701
1. Poll slave
1. Send a 2" image to the 2" slave and **verify it is received by the slave**.

####Add a 2.7" slave
1. Place a 2.7" slave beside the 2.0" slave
1. Deselect 2001 and select the 2701
1. Poll the 2.7"
1. Send a 2.7" image to the 2.7" slave and **verify it is received by the slave.**

####Test with 2" and 2.7" slave
1. Select the 2001 and keep the 2701.
1. Poll all slaves
1. Deselect the 1.44"
1. Send a 2" image to both.
1. **Results: Image is OK on the 2" and garbled on the 2.7"**
1. Send a 2.7" image to both
1. **Results: 2.7" slave is OK, 2" slave did not update**

####Test with 2" to recover it
1. Deselect 2701 and keep 2001
1. Poll 2001
1. Send a 2" image to 2001
1. **FAIL - Verify image is updated**

####Test to recover the 2"
1. Unplug and replug USB host
1. Poll 2001
1. Send a 2" Image to 2001
1. **AdapTag did one retry and recovered 2001**




