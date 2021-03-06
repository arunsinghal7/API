REQUEST
```xml
element REQUEST {
    element ACTION { ”sendPassInMMS” } &
    element API_KEY { text } &
    element MMSID { text } &
    element TO { text } &
    element FROM { text } &
    element CAMPAIGNREF { text }? &
    element DDMTITLE { text }? &
    element DDMTEXT { text }? &
    element DDMTIMEOUT { xsd:nonNegativeInteger }? &
    element CUSTOMTEXT {
        element VALUE { text } &
        element SLIDE { xsd:nonNegativeInteger }
    }? &
    element CUSTOMSUBJECT { text }? &
    element DATA {
        element FIRST_NAME { text }? &
        element LAST_NAME { text }? &
        element GENDER { text }?
        ...
    }? &
    element PASSDATA {
        element CUSTOMPASSID { text }? &
        element THUMBNAILURL { text }? &
        element BARCODEVALUE { text } &    # if "Barcode = Allowed" && "Barcode Type = Dynamic" && "Barcode Value Source = Dynamic Value" for Pass Template otherwise IGNORED
        element BARCODETEXT { text }? &    # if "Barcode = Allowed" && "Barcode Alternate Text = Dynamic Text" for Pass Template otherwise IGNORED
        element HEADERLABEL1 { text }? &
        element HEADERVALUE1 { text }? &
        element PRIMARYLABEL1 { text }? &
        element PRIMARYVALUE1  { text }? &
        element PRIMARYLABEL2 { text }? &    # if "Pass Template Type = Boarding Pass" otherwise IGNORED
        element PRIMARYVALUE2  { text }? &    # if "Pass Template Type = Boarding Pass" otherwise IGNORED
        element SECLABEL1 { text }? &
        element SECVALUE1 { text }? &
        element SECLABEL2 { text }? &
        element SECVALUE2 { text }? &
        element SECLABEL3 { text }? &
        element SECVALUE3 { text }? &
        element SECLABEL4 { text }? &
        element SECVALUE4 { text }? &
        element AUXLABEL1 { text }? &
        element AUXVALUE1 { text }? &
        element AUXLABEL2 { text }? &
        element AUXVALUE2 { text }? &
        element AUXLABEL3 { text }? &
        element AUXVALUE3 { text }? &
        element AUXLABEL4 { text }? &
        element AUXVALUE4 { text }? &
        element BACKLABEL1 { text }? &
        element BACKVALUE1 { text }? &
        element BACKLABEL2 { text }? &
        element BACKVALUE2 { text }? &
        element BACKLABEL3 { text }? &
        element BACKVALUE3 { text }? &
        element BACKLABEL4 { text }? &
        element BACKVALUE4 { text }? &
        element RELLATITUDE1 { text }? &
        element RELLONGITUDE1 { text }? &
        element RELTEXT1 { text }? &
        element RELLATITUDE2 { text }? &
        element RELLONGITUDE2 { text }? &
        element RELTEXT2 { text }? &
        element RELLATITUDE3 { text }? &
        element RELLONGITUDE3 { text }? &
        element RELTEXT3 { text }? &
        element RELLATITUDE4 { text }? &
        element RELLONGITUDE4 { text }? &
        element RELTEXT4 { text }? &
        element RELLATITUDE5 { text }? &
        element RELLONGITUDE5 { text }? &
        element RELTEXT5 { text }? &
        element RELLATITUDE6 { text }? &
        element RELLONGITUDE6 { text }? &
        element RELTEXT6 { text }? &
        element RELLATITUDE7 { text }? &
        element RELLONGITUDE7 { text }? &
        element RELTEXT7 { text }? &
        element RELLATITUDE8 { text }? &
        element RELLONGITUDE8 { text }? &
        element RELTEXT8 { text }? &
        element RELLATITUDE9 { text }? &
        element RELLONGITUDE9 { text }? &
        element RELTEXT9 { text }? &
        element RELLATITUDE10 { text }? &
        element RELLONGITUDE10 { text }? &
        element RELTEXT10 { text }?
    }
}
```

RESPONSE
```xml
element RESPONSE {
    element STATUS { text } &
    element TO { text }? &
    element FROM { text }? &
    element MMSID { text }? &
    element TRACKINGID { text }? &
    element ERRORCODE { text }? &
    element ERRORINFO { text }?
}
```

POSTBACK

N101
```xml
element POSTBACK {
    element ORIGIN { "MMS_MT" } &
    element CODE { "N101" } &
    element SENTAS { text } &
    element STATUS { text } &
    element MMSID { text } &
    element TO { text } &
    element TRACKINGID { text } &
    element SPID { text } &
    element TIMESTAMP { text }
}
```

N102
```xml
element POSTBACK {
    element ORIGIN { "MMS_MT" } &
    element CODE { "N102" } &
    element SENTAS { text } &
    element STATUS { text } &
    element MMSID { text } &
    element TO { text } &
    element TRACKINGID { text } &
    element SPID { text } &
    element TIMESTAMP { text } &
    element HANDSET { text } &
    element AGGREGATORID { text }
}
```