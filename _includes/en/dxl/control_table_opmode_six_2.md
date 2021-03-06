
|Value|Operating Mode| Description     |
| :---- | :------------------------------ | :------------------------------------------- |
| 0 | Current Control Mode | DYNAMIXEL only controls current(torque) regardless of speed and position. This mode is ideal for a gripper or a system that only uses current(torque) control or a system that has additional velocity/position controllers. |
| 1 | Velocity Control Mode | This mode controls velocity. This mode is identical to the Wheel Mode(endless) from existing DYNAMIXELs. This mode is ideal for wheel-type robots. |
| 3(Default) | Position Control Mode  |  This mode controls position. This mode is identical to the Joint Mode from existing DYNAMIXELs. Operating position range is limited by Max Position Limit(48) and Min Position Limit(52). This mode is ideal for articulated robots that each joint rotates less than 360 degrees.  |
|  4  |  Extended Position Control Mode(Multi-turn)  |  This mode controls position. This mode is identical to the Multi-Turn Mode from existing DYNAMIXELs. 512 turns are supported(-256[rev] ~ 256[rev]). This mode is ideal for multi-turn wrists or conveyer systems or a system that requires an additional reduction gear.  |
|  5  |  Current-based Position Control Mode  |  This mode controls both position and current(torque). Up to 512 turns are supported(-256[rev] ~ 256[rev]). This mode is ideal for a system that requires both position and current control such as articulated robots or grippers.  |
|  16  |  PWM Control Mode  (Voltage Control Mode)  |  This mode directly controls PWM output. (Voltage Control Mode)  |


{% capture group_notice_01 %}
**NOTE** : Switching Operating Mode will reset gains(PID, Feedfoward) properly to the selected Operating Mode. The profile generator and limits will also be reset.
1. Profile Velocity(112), Profile Acceleration(108) : Reset to ‘0’
2. Goal PWM(100), Goal Current(102) : Reset to PWM Limit(36), Current Limit(38) respectively
3. Current-based Position Control Mode : Reset to Position Gain(PID) and PWM Limit(36) values.

Changed Position Gain(PID) and PWM Limit(36) values can be read from the Control Table.
{% endcapture %}

<div class="notice">
  {{ group_notice_01 | markdownify }}
</div>

**NOTE** : PWM is the abbreviation for Pulse Width Modulation that modulates PWM Duty to control motors.  
The PWM Control Mode changes pulse width to control average supply voltage to the motor and this technique is widely used in the motor control field.  
Therefore, PWM Control Mode uses Goal PWM(100) value to control supply voltage for DYNAMIXEL.  
PWM Control Mode is similar to the Wheel Mode of DYNAMIXEL AX and RX series.
{: .notice}
