# Exercise 3. Creating an application to monitor room temperature and humidity

#### Estimated time

00:45

## Overview

In this exercise, you create an IoT system by using IBM Watson IoT
Platform. The purpose of the system is to monitor the temperature and
humidity of a facility and optimize the use of air conditioning. You use
the Watson IoT Platform device simulator to simulate the devices that
send temperature and humidity values through the internet to Watson IoT
Platform. Finally, you visualize the data that is sent by the devices in
real time by using the dashboard.

## Objectives

After completing this exercise, you should be able to:

  - Add a device to Watson IoT Platform and retrieve the credentials.

  - Use the Watson IoT Platform simulator to monitor temperature and
    humidity.

  - Chart the data on Watson IoT Platform.

## Introduction

Watson IoT Platform provides the building blocks for any IoT system,
device registry, authentication and authorization for devices and
applications, and data visualization.

You can have an end to end functioning system without writing a single
line of code for the back end. In this solution, you are concerned only
with device connectivity.

## Prerequisites

Complete exercise *Creating your first IoT application*.

## Requirements

You must have an active IBM Cloud account.

## Exercise instructions

In this exercise, you complete the following tasks:

- [X] Configure devices on Watson IoT Platform.

- [X] Connect the device to the simulator.

## _Part 1. Configuring devices on Watson IoT Platform_ 

This part shows how to access Watson IoT Platform over IBM
Cloud, add a device and configure it, and generate an API key and
authentication token that are required to link real devices or external
simulators to IBM Watson IoT Platform.

Complete the following steps:

1. Log in to IBM Cloud . From the Navigation Menu (hamburger button),
    select **Resource List** as shown in the following figure.

   ![](/media/SAIOT2EX03-mon-temp-hum_001.jpg)
1. testing step 1 

2. Expand the **Services** section and double-click the **Internet of
    Things Platform** service.

   ![](/media/SAIOT2EX03-mon-temp-hum_002.jpg)

3. Click **Launch** to get started with Watson IoT Platform.

   ![](/media/SAIOT2EX03-mon-temp-hum_003.jpg)

4. The Browse Devices window opens, as shown in the following
    figure.

   ![](/media/SAIOT2EX03-mon-temp-hum_004.jpg)

5. Select the **Device Types** tab and click **Add Device Type** in the
    upper right, as shown in the following figure.

   ![](/media/SAIOT2EX03-mon-temp-hum_005.jpg)

6. Specify the device type, name, and description as follows:

- **Type**: Select **Device**.

- **Name**: Enter **RoomSensors**

- **Description**: This device monitors room temperature and humidity
    
    Click **Next.**

   ![](/media/SAIOT2EX03-mon-temp-hum_006.jpg)

   >**Note:** In this step, you create the **device type**, which is not the device itself. The device type *name* is used to identify  the device type uniquely. For example, in a home automation system, a building can have multiple air-conditioners that send the same data points,
>temperature, and humidity. In this case, you define **Device Type** as air-conditioner and have multiple devices of this type, for example, 1<sup>st</sup> Floor air-conditioner and 2<sup>nd</sup>
>Floor air-conditioner. In this exercise, the device type name is *RoomSensors*.

   >**Information:** In certain situations, if the device cannot directly connect to the internet, it is aggregated first through a gateway. A gateway device can be built to retrieve and send data to applications in
>your Watson IoT Platform by using the MQTT or HTTP messaging protocol. In this exercise, you use the default device type (you do not need a gateway).

7. It is optional to add more information about the device type, such as *Serial Number*, *Model,* *Hardware Version,* and more.
    Click **Finish** as shown in the following figure.

   ![](/media/SAIOT2EX03-mon-temp-hum_007.jpg)

8. Click **Register Devices** to register a device of type RoomSensors.

   ![](/media/SAIOT2EX03-mon-temp-hum_008.jpg)

   >**Note:** The default way to add a device is to click **Devices** from the left navigation bar and then click **Add Device \+** as shown in the following figure.

  ![](/media/SAIOT2EX03-mon-temp-hum_011.png.png)

9. Select the device type that you previously created and enter a
    unique device ID as follows:

  - *Device Type*: **RoomSensors**

  - *Device ID*: **TempreatureAndHumidity1**
    
    Click **Next.**

   ![](/media/SAIOT2EX03-mon-temp-hum_012.jpg)

10. At the **Device Information** window, use the default values and click **Next**.

   >Optionally, you can modify the default device information and enter more information about the device for identification purposes.
    
   ![](/media/SAIOT2EX03-mon-temp-hum_013.jpg)

11. At the Security window, use the default option (Auto-generated authentication token) and click **Next**.

>Optionally, you can provide your own authentication token for this device. Do not use this option for this exercise.
    
![](/media/SAIOT2EX03-mon-temp-hum_014.jpg)

12. At the Summary window, click **Finish**.

![](/media/SAIOT2EX03-mon-temp-hum_015.jpg)

13. A window with the device credentials opens, as shown in the
    following figure.

>**IMPORTANT:** You must save the authentication token because after the window that is shown in the following figure closes, you cannot access the authentication token again. 
>If you lose the authentication token, you must reregister the device to generate a new authentication token.

![](/media/SAIOT2EX03-mon-temp-hum_017.jpg)

14. Copy the **Authentication Token** that is show in the credentials page, and save it in a safe place for later use.

15. Click the back arrow on the upper left to return to the Watson IoT
    Platform dashboard.
    
 ![](/media/SAIOT2EX03-mon-temp-hum_018.jpg)


