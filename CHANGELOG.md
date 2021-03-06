## 1.2.5 (Unreleased)
## 1.2.4 (May 31, 2018)

BUG FIXES:

- `r/packet_ip_attachment` - handling IP attachments being deleted outside of Terraform ([#68](https://github.com/terraform-providers/terraform-provider-packet/issues/68))

## 1.2.3 (April 27, 2018)

- [#61](https://github.com/terraform-providers/terraform-provider-packet/issues/61), fix volume resource update
- [#63](https://https://github.com/terraform-providers/terraform-provider-packet/pull/63), add Organization resource, add org attirbute to project resource

## 1.2.2 (April 17, 2018)

IMPROVEMENTS:

- [#58](https://github.com/terraform-providers/terraform-provider-packet/issues/58), properly fix resource updates

## 1.2.1 (April 16, 2018)

IMPROVEMENTS:

- [#57](https://github.com/terraform-providers/terraform-provider-packet/issues/57), fix for update of PXE attributes of device resource
- [#52](https://github.com/terraform-providers/terraform-provider-packet/issues/52) fix for project resource update
- [#49](https://github.com/terraform-providers/terraform-provider-packet/issues/49) fix for crash on SSH key update
- [#50](https://github.com/terraform-providers/terraform-provider-packet/issues/50) fix for device update, adds `description` attribute


## 1.2.0 (January 23, 2018)

BACKWARDS INCOMPATIBILITIES / NOTES:

* [#37](https://github.com/terraform-providers/terraform-provider-packet/issues/37), changes computation of packet_reserved_ip_block.cidr_notation. In case you use that attribute down the chain, you will need to refresh and recreate the resource in which you use it.

IMPROVEMENTS:

* datasource/packet_precreated_ip_block: Add Datasource for precreated IP blocks, so that users can assign subnets from those ([#36](https://github.com/terraform-providers/terraform-provider-packet/issues/36))
* mark device userdata as ForceNew, fixing ([#42](https://github.com/terraform-providers/terraform-provider-packet/issues/42))
* Add support for CPR (custom partitioning and RAID)([#35](https://github.com/terraform-providers/terraform-provider-packet/pull/35))

## 1.1.0 (October 09, 2017)

INTERNAL:

* Capture breaking change in the Packet API ((https://github.com/packethost/packngo/pull/47))

## 1.0.0 (September 28, 2017)

INTERNAL:

* provider: Add logging transport for HTTP client (`DEBUG` log now contains all HTTP requests & responses) ([#25](https://github.com/terraform-providers/terraform-provider-packet/issues/25))

IMPROVEMENTS:

* resource/packet_device: Add `public_ipv4_subnet_size` field ([#7](https://github.com/terraform-providers/terraform-provider-packet/issues/7))
* resource/packet_device: Add `hardware_reservation_id` field ([#14](https://github.com/terraform-providers/terraform-provider-packet/issues/14))
* resource/packet_device: Add `root_password` attribute ([#15](https://github.com/terraform-providers/terraform-provider-packet/issues/15))
* resource/packet_volume_attachment: Add resource for attaching volumes ([#9](https://github.com/terraform-providers/terraform-provider-packet/issues/9))
* resource/packet_reserved_ip_block: Add resource for reserving blocks of IP addresses ([#21](https://github.com/terraform-providers/terraform-provider-packet/issues/21))
* resource/packet_ip_attachment: Add resource for attaching floating IP addresses to devices ([#21](https://github.com/terraform-providers/terraform-provider-packet/issues/21))
* resource/packet_devce: Allow to use next-available hardware reservation ([#26](https://github.com/terraform-providers/terraform-provider-packet/issues/26))
* resource/packet_reserved_ip_block: Make reserved IP block resource importable ([#29](https://github.com/terraform-providers/terraform-provider-packet/issues/29))


## 0.1.0 (June 21, 2017)

NOTES:

* Same functionality as that of Terraform 0.9.8. Repacked as part of [Provider Splitout](https://www.hashicorp.com/blog/upcoming-provider-changes-in-terraform-0-10/)
