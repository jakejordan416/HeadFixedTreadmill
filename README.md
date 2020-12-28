# HeadFixedTreadmill

This repository contains Arduino and MATLAB files for a head-fixed treadmill with water reward set-up and related data analysis.

The treadmill consists of a rotary optical encoder, an RFID scanner, a lick sensor, a small buzzer and a pump for administering water rewards. All components feed into/out of National Instruments (NI) data acquisition hardware interfacing with MATLAB for task programming and data storage.

#Rotary Optical Encoder The rotary optical encoder we use is . This optical encoder is powered by an Arduino Due. This Arduino is constantly outputting a resting voltage of 1.38V to the NI acquisition hardware. Forward or reverse rotation of the optical encoder raises or lowers this output, respectively. This is then translated into running speed during analysis.

The RFID scanner we use is . RFID tags are adhered to the bottom of the treadmill belt and can be read by the RFID scanner attached the bottom of the platform. We typically use four RFID tags to signal transitions between zone textures and an additional RFID tag to trigger water reward.

We use the dual port lick sensor developed at Jenlia for lick counting. This sensor is very sensitive and may trigger false positives, however, we have found this rate to be very low.

We use a small buzzer early in training to facilitate water reward learning.

We use a microinfusion pump from Braintree Scientific (BS-8000). Output from the NI hardware delivers a TTL pulse to the pump which is programmed to adminster 10 microliters of water.
