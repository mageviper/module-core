# magento2-dpd
![shipping-config](img/dpd-logo-transparent.png "Config Shipping Dpd")

This module add DPD shipping method

### Version

1.0.0

### Compatibility

- Magento Open Source 2.2.*

### Installation

1. To enable this extension run the setup:upgrade command from Magento console

### Basic use

#### API CONFIG

`Stores -> Configuration -> Fwc Modules → Shipping Integration → Dpd`

![config](img/config_dpd.png "Config Dpd")


| NAME       | DESCRIPTION          |DEFAULT        |
|:---------  |:---------------------|:--------------|
| Test mode  | Use test api         | Enabled       |
| login      | DPD account login    | test          |
| password   | DPD account password | thetu4Ee      |
| MasterFid  | DPD MasterFid        | 1495          |
| AddressFid | DPD AddressFid       | 1495          |
| WSDL       | url to your wsdl     | [DEMO_WSDL][1]|

#### SHIPPING CONFIG

`Stores -> Configuration -> Sales -> Shipping Methods`

![shipping-config](img/config_shipping_dpd.png "Config Shipping Dpd")

|NAME             |DESCRIPTION                 |
|:----------------|:---------------------------|
| Enabled         | On/off shipping method     |
| Title           | Title on checkout          |
| Confgiuration   | [Owebia Config ][2]        |
| Max weight      | Max parcel weight          |
|Required Fields  | Owebia fileds validation   |
|Order Status     | Collect orders to manifest |

#### GENERATE MAIFEST

1. Prepare data `Sales -> Order -> [Prepare DPD data]`

![dpd-manifest-grid](img/dpd_manifest_grid.png "Dpd Manifest Grid")

| NAME               | DATA                                          |
|:-------------------|:----------------------------------------------|
| Create Date        | Open manifetst collect data                   |
| Last Update Date   | Date last collection modification             |
| Shipped Date       | Close manifest and send to DPD date           |
| Order              | Comma separated orders increment Id's         |
| Parcels            | Comma separeted parcel numbers form DPD Api   |
| Status             | Apply/Waiting for Apply                       |


[1]: https://dpdservicesdemo.dpd.com.pl/DPDPackageObjServicesService/DPDPackageObjServices?WSDL
[2]: http://htmlpreview.github.io/?https://github.com/owebia/magento2-module-advanced-shipping-setting/blob/master/view/doc_en_US.html