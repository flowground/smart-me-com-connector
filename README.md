# ![LOGO](logo.png) smart-me **flow**ground Connector

## Description

A generated **flow**ground connector for the smart-me API (version v1).

Generated from: https://api.apis.guru/v2/specs/smart-me.com/v1/swagger.json<br/>
Generated at: 2019-05-07T17:44:07+03:00

## API Description

With the smart-me REST API you get Access to all your devices in the smart-me Cloud and you can add your own devices. So it's a easy way to add the smart-me Cloud support to your Hardware or Software Product.

## Authorization

Supported authorization schemes:
- Basic Authentication

## Actions

### Creates a Access Token to write on a Card (e.g. NFC)

*Tags:* `AccessToken`

### Set an action for the specified device.

*Tags:* `Actions`

### Gets all available Actions of a Device

*Tags:* `Actions`

#### Input Parameters
* `id` - _required_ - The ID of the device

### Gets the additional information (e.g. Firmware Version) about a device.

*Tags:* `AdditionalDeviceInformation`

#### Input Parameters
* `id` - _required_ - The ID of the device

### Gets all Custom Devices

> Gets all Devices

*Tags:* `CustomDevice`

### Creates or updates a Custom Device or updates it's values.

> Creates or updates a Custom Device or updates it's values.<br/>
>             A Custom Device can be any device that like to add some measurement values to the smart-me Cloud.<br/>
>             Only use a custom device for all non meters.<br/>
>             For a new device leave the ID empty. To create a device you have to set the DeviceEnergyType.<br/>
>             To update values, add the ID of the device and the values you like to set.  (See the Data Type Model for more Information)

*Tags:* `CustomDevice`

### Gets a Custom Device by it's ID

> Gets a Device by it's ID

*Tags:* `CustomDevice`

#### Input Parameters
* `id` - _required_ - The ID of the device

### Gets a Device by it's Serial Number. The Serial is the part before the "-".

*Tags:* `DeviceBySerial`

#### Input Parameters
* `serial` - _required_ - The Serial Number of the device

### Gets all Devices

*Tags:* `Devices`

### Creates or updates a Device or updates it's values.

> Creates or updates a Device or updates it's values. <br/>
>             For a new device leave the ID empty. To create a device you have to set the DeviceEnergyType.<br/>
>             To update values, add the ID of the device and the values you like to set.  (See the Data Type Model for more Information)

*Tags:* `Devices`

### Gets a Device by it's ID

*Tags:* `Devices`

#### Input Parameters
* `id` - _required_ - The ID of the device

### Updates the On/Off Switch on a device. <br/>
>             For new implementations please use the "actions" command

> Updates the On/Off Switch on a device<br/>
>             For new implementations please use the "actions" command

*Tags:* `Devices`

#### Input Parameters
* `id` - _required_ - The ID of the device
* `switchState` - _required_ - The new state of the switch
* `switchNumber` - _optional_ - The number of the switch if there are multiple (1 for L1, 3 for L3)

### Gets all Devices for an Energy Type

*Tags:* `DevicesByEnergy`

#### Input Parameters
* `meterEnergyType` - _required_
    Possible values: MeterTypeUnknown, MeterTypeElectricity, MeterTypeWater, MeterTypeGas, MeterTypeHeat, MeterTypeHCA, MeterTypeAllMeters, MeterTypeTemperature, MeterTypeMBusGateway, MeterTypeRS485Gateway, MeterTypeCustomDevice, MeterTypeCompressedAir, MeterTypeSolarLog, MeterTypeVirtualMeter.

### Gets all Devices by it's Sub Type (e.g. E-Charging Station)

*Tags:* `DevicesBySubType`

#### Input Parameters
* `meterSubType` - _required_
    Possible values: MeterSubTypeUnknown, MeterSubTypeCold, MeterSubTypeHeat, MeterSubTypeChargingStation, MeterSubTypeElectricity, MeterSubTypeWater, MeterSubTypeGas, MeterSubTypeElectricityHeat, MeterSubTypeTemperature, MeterSubTypeVirtualBattery.

### Gets the Values for a folder or a meter

*Tags:* `Folder`

#### Input Parameters
* `id` - _required_

### M-BUS API: Adds data of a M-BUS Meter to the smart-me Cloud.<br/>
>             Just send us the M-BUS Telegram (RSP_UD) and we will do the Rest.

*Tags:* `MBus`

### Sets the Name of a Meter or a Folder

*Tags:* `MeterFolderInformation`

### Beta: Gets the General Information for a Meter or a Folder

*Tags:* `MeterFolderInformation`

#### Input Parameters
* `id` - _required_

### Gets the Values for a Meter at a given Date. <br/>
>             The first Value found before the given Date is returned.

> Gets the Values for a Meter at a given Date. The first Value found before the given Date is returned.

*Tags:* `MeterValues`

#### Input Parameters
* `id` - _required_
* `date` - _required_

### Gets all registrations for the Realtime API.

*Tags:* `RegisterForRealtimeApi`

### Creates a new registration for the realtime API. The Realtime API sends you the data of the registred devices as soon as we have them on the cloud.<br/>
>              More Information about the realtime API: https://www.smart-me.com/Description/api/realtimeapi.aspx

> Creates a new registration for the realtime API. The Realtime API sends you the data of the registred devices as soon as we have them on the cloud. More Information about the realtime API: https://www.smart-me.com/Description/api/realtimeapi.aspx

*Tags:* `RegisterForRealtimeApi`

### Deletes a realtime API registration.

*Tags:* `RegisterForRealtimeApi`

#### Input Parameters
* `id` - _required_ - The ID of the realtime API registration

### Sets the configuration of a smart-me device. The device needs to be online.

*Tags:* `SmartMeDeviceConfiguration`

### Gets the configuration of a smart-me device.

*Tags:* `SmartMeDeviceConfiguration`

#### Input Parameters
* `id` - _required_

### Gets the informations for the user.

*Tags:* `User`

### Gets all (last) values of a device

*Tags:* `Values`

#### Input Parameters
* `id` - _required_ - The ID of the device

### Gets all (last) values of a device<br/>
>             The first Value found before the given Date is returned.

> Gets the Values for a device at a given Date. The first Value found before the given Date is returned.

*Tags:* `ValuesInPast`

#### Input Parameters
* `id` - _required_ - The ID of the device
* `date` - _required_ - the date of the value

### Gets multiple values of a device. This call needs a smart-me professional licence.

*Tags:* `ValuesInPastMultiple`

#### Input Parameters
* `id` - _required_ - The ID of the device
* `startDate` - _required_ - The date when the first value should start
* `endDate` - _required_ - The date when the last value should start
* `interval` - _required_ - The interval in minutes betwenn the values. 0 means as fast as possible. Only 1000 values can be get in one call.

### Beta: Gets all active virtual meters

> Beta: Gets all active virtual meters.

*Tags:* `VirtualBillingMeterActive`

### Beta: Virtual Meter API: Activates a Meter and add the Consumption to a Virtual Meter assosiated with the User.

*Tags:* `VirtualBillingMeterActive`

### Beta: Virtual Meter API: Deactivates a Virtual Meter.

*Tags:* `VirtualBillingMeterDeactivate`

### Beta: Gets all Meters available to activate as a Virtual Meter.

*Tags:* `VirtualBillingMeters`

### Calculates a virtual meter from a formula. <br/>
>             A meter is coded as ID("METERID")

> Calculates a virtual meter from a formula.<br/>
>             <br/>
>             A meter is coded as ID("METERID")<br/>
>             Ariphmetical operators:<br/>
>              ()  parentheses;  <br/>
>              +   plus (a + b); <br/>
>              -  minus (a - b); <br/>
>              *  multiplycation symbol (a * b); <br/>
>              /  divide symbol (a / b); <br/>
>             Example: (ID("63ac09cb-4e5f-4f3e-bd27-ad8c30bdfc0c") + ID("0209555e-9dc4-4e84-a166-a864488b4b12")) * 2

*Tags:* `VirtualMeterCalculateFormula`

#### Input Parameters
* `formula` - _required_

### Gets all Virtual Tariffs of a user

*Tags:* `VirtualTariff`

### Gets all virtual tariffs of a folder

*Tags:* `VirtualTariff`

#### Input Parameters
* `id` - _required_ - The ID of the Folder

### Gets the consumption of a folder with a virtuall tariffs.

*Tags:* `VirtualTariffConsumption`

#### Input Parameters
* `folderId` - _required_ - The ID of the Folder
* `startDate` - _required_ - The start date (UTC)
* `endDate` - _required_ - The end date (UTC)

## License

**flow**ground :- Telekom iPaaS / smart-me-com-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
