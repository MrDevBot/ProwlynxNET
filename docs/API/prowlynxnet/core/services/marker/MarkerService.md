# MarkerService `Public class`

## Diagram
```mermaid
  flowchart LR
  classDef interfaceStyle stroke-dasharray: 5 5;
  classDef abstractStyle stroke-width:4px
  subgraph ProwlynxNET.Core.Services.Marker
  ProwlynxNET.Core.Services.Marker.MarkerService[[MarkerService]]
  end
  subgraph ProwlynxNET.Core.Models.Services
  ProwlynxNET.Core.Models.Services.IMarkerService[[IMarkerService]]
  class ProwlynxNET.Core.Models.Services.IMarkerService interfaceStyle;
  end
  subgraph ProwlynxNET.Core.Models
  ProwlynxNET.Core.Models.IService[[IService]]
  class ProwlynxNET.Core.Models.IService interfaceStyle;
  end
ProwlynxNET.Core.Models.Services.IMarkerService --> ProwlynxNET.Core.Services.Marker.MarkerService
ProwlynxNET.Core.Models.IService --> ProwlynxNET.Core.Models.Services.IMarkerService
```

## Members
### Properties
#### Public  properties
| Type | Name | Methods |
| --- | --- | --- |
| [`MarkerInfo`](./MarkerInfo.md) | [`Database`](#database)<br>The database of marker information for the marker service. | `get` |
| `string` | [`Description`](#description)<br>Description of the service. | `get` |
| `string` | [`Name`](#name)<br>The unique name of the service. | `get` |

### Methods
#### Public  methods
| Returns | Name |
| --- | --- |
| `void` | [`AddMark`](#addmark-12)(`...`)<br>Add a mark for the given arguments. |
| `bool` | [`CanProtect`](#canprotect-14)(`...`)<br>Check whether the protection can protect the type. |

## Details
### Inheritance
 - [
`IMarkerService`
](../../models/services/IMarkerService.md)
 - [
`IService`
](../../models/IService.md)

### Constructors
#### MarkerService
[*Source code*](https://github.com///blob//ProwlynxNET.Core/Services/Marker/MarkerService.cs#L18)
```csharp
public MarkerService()
```

### Methods
#### AddMark [1/2]
[*Source code*](https://github.com///blob//ProwlynxNET.Core/Services/Marker/MarkerService.cs#L32)
```csharp
public virtual void AddMark(IMemberDefinition target, string protectionName, bool exclude, bool applyToMembers)
```
##### Arguments
| Type | Name | Description |
| --- | --- | --- |
| `IMemberDefinition` | target | The target definition. |
| `string` | protectionName | The protection name from the calling [IProtection](../../models/IProtection.md) . |
| `bool` | exclude | Whether to disallow protection. |
| `bool` | applyToMembers | Whether to apply the same mark to methods. |

##### Summary
Add a mark for the given arguments.

#### AddMark [2/2]
[*Source code*](https://github.com///blob//ProwlynxNET.Core/Services/Marker/MarkerService.cs#L44)
```csharp
public virtual void AddMark(ObfuscationInfo info)
```
##### Arguments
| Type | Name | Description |
| --- | --- | --- |
| [`ObfuscationInfo`](./ObfuscationInfo.md) | info | The obfuscation info. Cannot be null. |

##### Summary
Add an obfuscation info to the marker database.

#### CanProtect [1/4]
[*Source code*](https://github.com///blob//ProwlynxNET.Core/Services/Marker/MarkerService.cs#L16707566)
```csharp
public virtual bool CanProtect(IProtection currentProtection, TypeDefinition targetType, bool checkForPropagation)
```
##### Arguments
| Type | Name | Description |
| --- | --- | --- |
| [`IProtection`](../../models/IProtection.md) | currentProtection | The protection currently running. |
| `TypeDefinition` | targetType | The target type to protect. |
| `bool` | checkForPropagation | Used internally for recursion. Whether to check that the types apply to members. |

##### Summary
Check whether the protection can protect the type.

##### Returns
Whether the protection can protect the target type.

#### CanProtect [2/4]
[*Source code*](https://github.com///blob//ProwlynxNET.Core/Services/Marker/MarkerService.cs#L16707566)
```csharp
public virtual bool CanProtect(IProtection currentProtection, MethodDefinition targetMethod)
```
##### Arguments
| Type | Name | Description |
| --- | --- | --- |
| [`IProtection`](../../models/IProtection.md) | currentProtection | The protection currently running. |
| `MethodDefinition` | targetMethod | The method that is to be protected. |

##### Summary
Check whether the protection can protect a given method.

##### Returns
Whether the protection can protect the target method.

#### CanProtect [3/4]
[*Source code*](https://github.com///blob//ProwlynxNET.Core/Services/Marker/MarkerService.cs#L16707566)
```csharp
public virtual bool CanProtect(IProtection currentProtection, EventDefinition targetEvent)
```
##### Arguments
| Type | Name | Description |
| --- | --- | --- |
| [`IProtection`](../../models/IProtection.md) | currentProtection | The protection currently running. |
| `EventDefinition` | targetEvent | The event that is to be protected. |

##### Summary
Check whether the protection can protect a given event.

##### Returns
Whether the protection can protect the target event.

#### CanProtect [4/4]
[*Source code*](https://github.com///blob//ProwlynxNET.Core/Services/Marker/MarkerService.cs#L16707566)
```csharp
public virtual bool CanProtect(IProtection currentProtection, PropertyDefinition targetProperty)
```
##### Arguments
| Type | Name | Description |
| --- | --- | --- |
| [`IProtection`](../../models/IProtection.md) | currentProtection | The protection currently running. |
| `PropertyDefinition` | targetProperty | The property that is to be protected. |

##### Summary
Check whether the protection can protect a given property.

##### Returns
Whether the protection can protect the target property.

### Properties
#### Database
```csharp
public virtual MarkerInfo Database { get; }
```
##### Summary
The database of marker information for the marker service.

#### Name
```csharp
public virtual string Name { get; }
```
##### Summary
The unique name of the service.

#### Description
```csharp
public virtual string Description { get; }
```
##### Summary
Description of the service.

*Generated with* [*ModularDoc*](https://github.com/hailstorm75/ModularDoc)
