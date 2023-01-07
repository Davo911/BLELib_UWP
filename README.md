# BLELib_UWP

A library for working with Bluetooth Low Energy (BLE) devices on Universal Windows Platform (UWP) applications.

## Features

- Easy to use interface for connecting to and interacting with BLE devices
- Supports reading and writing characteristics and descriptors
- Supports subscribing to notifications and indications
- Supports automatic connection and reconnection to devices

## Getting Started

### Prerequisites

- Windows 10
- Visual Studio 2017 or later

### Installation

1. Clone or download the repository
2. Open the solution file `BLELib_UWP.sln` in Visual Studio
3. Build the solution

### Usage

To use the library in your own UWP application, add a reference to the `BLELib_UWP` project and use the `BleDevice` class to connect to and communicate with BLE devices.

```csharp
// Create a new BleDevice instance
var bleDevice = new BleDevice();

// Connect to the device with the given Bluetooth address
await bleDevice.ConnectAsync("00:11:22:33:44:55");

// Read the value of the "Temperature" characteristic
var temperature = await bleDevice.ReadCharacteristicAsync("Temperature");

// Write a new value to the "Light" characteristic
await bleDevice.WriteCharacteristicAsync("Light", new byte[] { 1 });
