---
title: Storage DDF-Datei
description: Storage DDF-Datei
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/hardware
ms.assetid: 247062A3-4DFB-4B14-A3D1-68D02C27703C
ms.openlocfilehash: 352312eab2b072d9cd15b79c2420bcc221107bf1
ms.sourcegitcommit: d33e870dc4850bf0ea47fdae0d163b04c1c90f15
translationtype: MT
---
# <a name="storage-ddf-file"></a>Storage DDF-Datei


In diesem Thema wird das OMA DM Gerät Beschreibung Framework (DDF) für den **Speicher** Konfiguration-Dienstanbieter. DDF-Dateien werden nur mit OMA DM XML-Bereitstellung verwendet.

``` syntax
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE MgmtTree PUBLIC "-//OMA//DTD-DM-DDF 1.2//EN"
    "http://www.openmobilealliance.org/tech/DTD/DM_DDF-V1_2.dtd"
    [
  <?oma-dm-ddf-ver supported-versions="1.2"?>
]>
<MgmtTree>
  <VerDTD>1.2</VerDTD>
  <Node>
    <NodeName>Storage</NodeName>
    <Path>./Vendor/MSFT</Path>
    <DFProperties>
      <AccessType>
        <Get />
      </AccessType>
      <Description>Root node for Storage CSP.</Description>
      <DFFormat>
        <node />
      </DFFormat>
      <Occurrence>
        <One />
      </Occurrence>
      <Scope>
        <Permanent />
      </Scope>
      <DFType>
        <DDFName></DDFName>
      </DFType>
    </DFProperties>
    <Node>
      <NodeName>Disable</NodeName>
      <DFProperties>
        <AccessType>
          <Get />
          <Replace />
        </AccessType>
        <Description>Specifies whether to enable or disable a storage card. A Boolean value of true disables the storage card. The default value is False. The value is case sensitive.</Description>
        <DFFormat>
          <bool />
        </DFFormat>
        <Occurrence>
          <One />
        </Occurrence>
        <Scope>
          <Permanent />
        </Scope>
        <DFType>
          <MIME>text/plain</MIME>
        </DFType>
      </DFProperties>
    </Node>
  </Node>
</MgmtTree>
```

 

 






