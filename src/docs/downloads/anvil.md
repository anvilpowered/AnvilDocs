---
title: Anvil Downloads
---

|Version|Link|
|-------|----|
|0.3|[download]()|
|0.2.1|[download]()|
|0.2|[download]()|
|0.1.3|[download]()|
|0.1.2|[download]()|
|0.1.1|[download]()|
|0.1|[download]()|

## Changelog

### 0.3

### 0.2.1
Squashed bugs

- Command suggestions work properly now
- Fixed an NPE
- Small code cleanups

### 0.2
This release has breaking API changes.

New in this version:

- **Important!** Registering a listener to a registry now requires you to add .register(); at the end of the call. Plugins will fail silently if this is not done. This was done to make it simpler to specify the scope and order for a listener.
- Added ordering to registry listeners.
- Added @RegistryScoped annotation.
- Keys now require a namespace to register, this is to make inter-plugin data access easier and pave the way for future placeholder stuff.
- TimeFormatService now uses FormatResult for some return types. Use toString() to capture the current state of the FormatResult as a String.
- Updated MongoDB drivers
- Started using checker framework

Removed in this version:

- Nuked the Plugin interface. This interface added unnecessary weight to the API and wasn't being used anywhere.
- The PermissionService no longer has a generic type. This service only has one boolean method to check a permission for the provided subject. Checking the type of this parameter is now done at runtime.

### 0.1.3
Fixed a critical bug preventing banning and muting with Xodus.

### 0.1.2
Fixed bug in BaseManager causing silent failure during DB access.

### 0.1.1
This release fixes an issue where Anvil would sometimes load after plugins that depend on it.

### 0.1
This is the first release for Anvil. While stable, please note that Anvil is still under heavy development.
