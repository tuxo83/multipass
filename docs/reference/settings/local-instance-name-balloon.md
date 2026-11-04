(reference-settings-local-instance-name-balloon)=
# local.\<instance-name\>.balloon

> See also: [`get`](/reference/command-line-interface/get), [`set`](/reference/command-line-interface/set), [`local.driver`](/reference/settings/local-driver).

## Key

`local.<instance-name>.balloon`

where `<instance-name>` is the name of a Multipass instance.

## Description

Whether the instance has a memory balloon device with free page reporting. With it, the guest reports the memory it has freed and the host takes it back, so an idle instance holds less host memory.

The change takes effect the next time the instance starts. Resuming a suspended instance keeps the devices it was suspended with.

This setting is only available with the `qemu` driver. The guest kernel needs free page reporting support (Linux 5.7 or later, e.g. Ubuntu 22.04 and later).

## Possible values

A boolean value (`true` or `false`).

## Examples

`multipass set local.handsome-ling.balloon=true`

## Default value

`false`
