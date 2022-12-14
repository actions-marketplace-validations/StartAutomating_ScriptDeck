Update-StreamDeckPlugin
-----------------------
### Synopsis
Updates a StreamDeck Plugin

---
### Description

Updates a StreamDeck Plugin

---
### Related Links
* [Get-StreamDeckPlugin](Get-StreamDeckPlugin.md)



---
### Examples
#### EXAMPLE 1
```PowerShell
Update-StreamDeckPlugin -PluginPath .\MyPlugin -Name "MyPluginName" -Author "MyPluginAuthor" -Description "MyPluginDescription"
```

#### EXAMPLE 2
```PowerShell
Get-StreamDeckPlugin -Name MyStreamDeckPlugin | # Get the plugin named MyStreamDeckPlugin 
    Update-StreamDeckPlugin -IncrementVersion Minor # Increment the minor version of the plugin.
```

---
### Parameters
#### **PluginPath**

The path to the streamdeck plugin.



> **Type**: ```[String]```

> **Required**: true

> **Position**: 1

> **PipelineInput**:true (ByPropertyName)



---
#### **Name**

The name of the plugin. This string is displayed to the user in the Stream Deck store.



> **Type**: ```[String]```

> **Required**: false

> **Position**: 2

> **PipelineInput**:true (ByPropertyName)



---
#### **Author**

The author of the plugin. This string is displayed to the user in the Stream Deck store.



> **Type**: ```[String]```

> **Required**: false

> **Position**: 3

> **PipelineInput**:true (ByPropertyName)



---
#### **Description**

Provides a general description of what the plugin does.
This is displayed to the user in the Stream Deck store.



> **Type**: ```[String]```

> **Required**: false

> **Position**: 4

> **PipelineInput**:true (ByPropertyName)



---
#### **Version**

The version of the plugin which can only contain digits and periods. This is used for the software update mechanism.



> **Type**: ```[Version]```

> **Required**: false

> **Position**: 5

> **PipelineInput**:true (ByPropertyName)



---
#### **AutoIncrement**

If provided, will auto-increment the version of the extension.
* Major increments the major version ( 1.0   -> 2.0  )
* Minor increments the minor version ( 0.1   -> 0.2  )
* Patch increments the patch version ( 0.0.1 -> 0.0.2)



Valid Values:

* Major
* Minor
* Patch



> **Type**: ```[String]```

> **Required**: false

> **Position**: 6

> **PipelineInput**:true (ByPropertyName)



---
#### **WhatIf**
-WhatIf is an automatic variable that is created when a command has ```[CmdletBinding(SupportsShouldProcess)]```.
-WhatIf is used to see what would happen, or return operations without executing them
#### **Confirm**
-Confirm is an automatic variable that is created when a command has ```[CmdletBinding(SupportsShouldProcess)]```.
-Confirm is used to -Confirm each operation.
    
If you pass ```-Confirm:$false``` you will not be prompted.
    
    
If the command sets a ```[ConfirmImpact("Medium")]``` which is lower than ```$confirmImpactPreference```, you will not be prompted unless -Confirm is passed.

---
### Syntax
```PowerShell
Update-StreamDeckPlugin [-PluginPath] <String> [[-Name] <String>] [[-Author] <String>] [[-Description] <String>] [[-Version] <Version>] [[-AutoIncrement] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```
---
