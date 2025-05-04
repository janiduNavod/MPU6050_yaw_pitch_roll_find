# MPU6050 Orientation Tracker (Pitch, Roll, Yaw)

This project uses an **MPU6050** sensor with an **Arduino** to measure and calculate orientation angles: **Pitch**, **Roll**, and **Yaw** using both accelerometer and gyroscope data.

Yaw is calculated from the gyroscope only, which may drift over time. For stable yaw, you may consider using a magnetometer (e.g., HMC5883L).

## 📷 Sensor Used
- [MPU6050](https://learn.adafruit.com/adafruit-mpu6050-6-dof-accel-and-gyro/overview) - 6 DOF (3-axis Accelerometer + 3-axis Gyroscope)

## 🧠 Libraries Required
- `Adafruit_MPU6050`
- `Adafruit_Sensor`
- `Wire.h`

Install via Arduino Library Manager.

## 💻 Code Overview

- Uses complementary filtering to calculate accurate **pitch** and **roll**
- Uses gyroscope integration to estimate **yaw** (subject to drift)
- Outputs angles via Serial Monitor at 115200 baud
