I would like to add my own presets to this repository. I will search for them by Author so they need to be tagged with "JRo"

JRo, Rates: Include also craft name and pilot name.

JRo, OSD:

JRo, ELRS: This should be identical to the ELRS 500Hz settings for the RCLINK settings

JRo, Modes: Set the switches as well as the VTX power change switch.

JRo, Dash Filters: This is with both LPF gyro filters turned off
                    This is with the second harmonic for 3 bladed prop turned down to 20% and the third to 80%

JRo, Dash PID Tune: Set the pidsum both to yaw to max. Set the feedforward to 1.1


For information about each of the CLI commands for these presets see the following log file: 

# version
# Betaflight / STM32H743 (SH74) 4.5.2 Mar 31 2025 / 00:32:56 (024f8e13d) MSP API: 1.46
# config rev: 48588b7

# start the command batch
batch start

# reset configuration to default settings
defaults nosave

board_name HDZERO_HALO
manufacturer_id HDZO
mcu_id 0037001c3233510335323939
signature 

# name: Dash

# resources
resource LED 2 C14

# serial
serial 4 0 115200 57600 0 115200
serial 6 131073 115200 57600 0 115200

# led
led 0 3,0::CT:14
led 1 4,0::CT:14
led 2 5,0::CT:14
led 3 6,0::CT:14
led 4 7,0::CT:14
led 5 8,0::CT:14
led 6 9,0::CT:14
led 7 10,0::CT:14
led 8 11,0::CT:14
led 9 12,0::CT:14

# color
color 13 0,0,255
color 14 120,0,255
color 15 240,0,255

# mode_color
mode_color 7 0 9

# aux
aux 0 0 0 1725 2100 0 0
aux 1 1 2 1300 1700 0 0
aux 2 13 1 1750 2100 0 0
aux 3 26 3 1300 2100 0 0
aux 4 35 1 1725 2100 0 0

# vtxtable
vtxtable bands 6
vtxtable channels 8
vtxtable band 1 BOSCAM_A A CUSTOM     0    0    0    0    0    0    0    0
vtxtable band 2 BOSCAM_B B CUSTOM     0    0    0    0    0    0    0    0
vtxtable band 3 BOSCAM_E E CUSTOM  5705    0    0    0    0    0    0    0
vtxtable band 4 FATSHARK F CUSTOM  5740 5760    0 5800    0    0    0    0
vtxtable band 5 RACEBAND R CUSTOM  5658 5695 5732 5769 5806 5843 5880 5917
vtxtable band 6 LOWBAND  L CUSTOM     0    0    0    0    0    0    0    0
vtxtable powerlevels 3
vtxtable powervalues 14 23 0
vtxtable powerlabels 25 200 0

# vtx
vtx 0 4 0 0 1 900 1200
vtx 1 4 0 0 1 1300 1700
vtx 2 4 0 0 3 1800 2100

# master
set gyro_lpf1_static_hz = 0
set gyro_lpf2_static_hz = 0
set dyn_notch_count = 1
set dyn_notch_q = 500
set gyro_lpf1_dyn_min_hz = 0
set acc_calibration = 1,-100,-28,1
set rc_smoothing_auto_factor = 25
set rc_smoothing_auto_factor_throttle = 25
set dshot_bidir = ON
set yaw_motors_reversed = ON
set simplified_gyro_filter_multiplier = 200
set report_cell_voltage = ON
set ledstrip_brightness = 12
set osd_rssi_pos = 3150
set osd_link_quality_pos = 3116
set osd_tim_1_pos = 3628
set osd_vtx_channel_pos = 2592
set osd_mah_drawn_pos = 2080
set osd_pilot_name_pos = 2560
set osd_warnings_pos = 14836
set osd_avg_cell_voltage_pos = 2112
set osd_rate_profile_name_pos = 558
set osd_canvas_width = 50
set osd_canvas_height = 18
set vtx_band = 5
set vtx_channel = 5
set vtx_power = 1
set vtx_freq = 5806
set rpm_filter_weights = 100,20,70
set craft_name = Dash
set pilot_name = JRo

profile 0

# profile 0
set iterm_relax_cutoff = 30
set pidsum_limit = 1000
set pidsum_limit_yaw = 1000
set p_pitch = 59
set i_pitch = 105
set d_pitch = 48
set f_pitch = 144
set p_roll = 56
set i_roll = 100
set d_roll = 42
set f_roll = 138
set p_yaw = 56
set i_yaw = 100
set f_yaw = 138
set d_min_roll = 31
set d_min_pitch = 35
set d_max_advance = 0
set feedforward_averaging = 2_POINT
set feedforward_smooth_factor = 65
set feedforward_jitter_factor = 3
set feedforward_boost = 18
set dyn_idle_min_rpm = 30
set simplified_master_multiplier = 105
set simplified_pi_gain = 120
set simplified_feedforward_gain = 110

profile 1

profile 2

profile 3

# restore original profile selection
profile 0

rateprofile 0

# rateprofile 0
set rateprofile_name = Rate 1
set roll_rc_rate = 12
set pitch_rc_rate = 11
set yaw_rc_rate = 11
set roll_expo = 32
set pitch_expo = 32
set yaw_expo = 32
set roll_srate = 50
set pitch_srate = 40
set yaw_srate = 25
set throttle_limit_type = SCALE
set throttle_limit_percent = 75

rateprofile 1

# rateprofile 1
set rateprofile_name = Rate 1
set roll_rc_rate = 14
set pitch_rc_rate = 13
set yaw_rc_rate = 13
set roll_expo = 32
set pitch_expo = 32
set yaw_expo = 32
set roll_srate = 55
set pitch_srate = 44
set yaw_srate = 27
set throttle_limit_type = SCALE
set throttle_limit_percent = 80

rateprofile 2

rateprofile 3

# restore original rateprofile selection
rateprofile 1

# save configuration
save
