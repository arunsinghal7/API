REQUEST
```xml
element REQUEST {
    element ACTION { "sendSavedMMSCampaign" } &
    element API_KEY { text } &
    element MMSID { text } &
    element TOCAMPAIGN { text }
}
```

RESPONSE
```xml
element RESPONSE {
    element STATUS { text } &
    element MMSID { text }? &
    element SCHEDULEDID { text }? &
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