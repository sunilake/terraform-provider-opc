---
layout: "opc"
page_title: "Oracle: opc_compute_storage_volume_snapshot"
sidebar_current: "docs-opc-datasource-storage-volume-snapshot"
description: |-
  Gets information about the configuration of a storage volume snapshot
---

# opc\_compute\_storage\_volume\_snapshot

Use this data source to access the configuration of a storage volume snapshot.

## Example Usage

```hcl
data "opc_compute_storage_volume_snapshot" "foo" {
  name = "my-storage-volume/my-storage-volume-snapshot-name"
}
```

## Argument Reference
* `name` is the name of the storage volume snapshot.

## Attributes Reference

* `account` - Account of the snapshot.
* `collocated` - Boolean specifying whether the snapshot is collocated or remote.
* `description` - The description of the storage volume snapshot.
* `machine_image_name` - The name of the machine image that's used in the boot volume from which this snapshot is taken.
* `parent_volume_bootable` - Boolean specifying whether or not the snapshot's parent volume was bootable.
* `property` - Where the snapshot is stored, whether collocated, or in the Oracle Storage Cloud Service instance.
* `platform` - The OS platform this snapshot is compatible with
* `size` - The size of the snapshot in GB.
* `snapshot_timestamp` - Timestamp of the storage snapshot, generated by storage server. The snapshot will contain data written to the original volume before this time.
* `snapshot_id` - The Oracle ID of the snapshot.
* `start_timestamp` - Timestamp when the snapshot was started.
* `status` - Status of the snapshot.
* `status_detail` - Details about the latest state of the storage volume snapshot.
* `status_timestamp` - Indicates the time that the current view of the storage volume snapshot was generated.
* `tags` - Comma-separated strings that tag the storage volume.
* `uri` - Uniform Resource Identifier
* `volume_name` - The name of the storage volume that the snapshot was created from
