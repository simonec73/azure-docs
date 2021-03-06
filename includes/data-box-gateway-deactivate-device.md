---
author: alkohli
ms.service: databox  
ms.topic: include
ms.date: 10/15/2020
ms.author: alkohli
---

To reset your device, you need to securely wipe out all the data on the data disk and the boot disk of your device. 

Use the `Reset-HcsAppliance` cmdlet to wipe out both the data disks and the boot disk or just the data disks. The `ClearData` and `BootDisk` switches allow you to wipe the data disks and the boot disk respectively.

The `BootDisk` switch wipes the boot disk and makes the device unusable. It should be used only when the device needs to be returned to Microsoft. For more information, see [Return the device to Microsoft](/azure/databox-online/data-box-edge-return-device.md).

If you use the device reset in the local web UI, only the data disks are securely wiped, but the boot disk is kept intact. The boot disk contains the device configuration.

1. [Connect to the PowerShell interface](#connect-to-the-powershell-interface).
2. At the command prompt, type:

    `Reset-HcsAppliance -ClearData -BootDisk`

    The following example shows how to use this cmdlet:

    ```powershell
    [10.128.24.33]: PS>Reset-HcsAppliance -ClearData -BootDisk

    Confirm
    Are you sure you want to perform this action?
    Performing the operation "Reset-HcsAppliance" on target "ShouldProcess appliance".
    [Y] Yes  [A] Yes to All  [N] No  [L] No to All  [?] Help (default is "Y"): N
    ```
