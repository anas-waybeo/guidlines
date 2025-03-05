### CDR data (Missed)

```bash
{
  "callId": "f4de9019-6b4a-479e-8370-760c4e7b07c9-10",
  "uniqueId": "f4de9019-6b4a-479e-8370-760c4e7b07c9",
  "dateTime": "1740735753505",
  "dateTimeIso": "2025-02-28T09:42:33.505Z",
  "date": "2025-02-28",
  "callType": "INBOUND",
  "totalDuration": 12,
  "conversationDuration": 0,
  "virtualNumber": "+919535976902",
  "status": "Missed",
  "hangupLeg": "Caller",
  "busyCallees": [
    "+919372022300"
  ],
  "callRecordUrl": null,
  "dtmfKeys": [],
  "gateway": "Airtel",
  "callerRingDuration": 0,
  "ringDuration": 2,
  "callerStatus": "Answered",
  "calleeStatus": "Missed",
  "ivrDuration": 10,
  "busyCalleesStr": "+919372022300",
  "correlationId": "Xchangef4de9019-6b4a-479e-8370-760c4e7b07c9",
  "callerNumber": "+919822371632"
}
```

### CDR data (Answered)
```bash
{
    "callId": "82a7eea0-e786-43aa-a1a6-aea58c53bc2f",
    "uniqueId": "82a7eea0-e786-43aa-a1a6-aea58c53bc2f",
    "dateTime": "1741056836655",
    "dateTimeIso": "2025-03-04T02:53:56.655Z",
    "date": "2025-03-04",
    "callType": "INBOUND",
    "totalDuration": 35,
    "conversationDuration": 1,
    "virtualNumber": "+919535935699",
    "status": "Answered",
    "hangupLeg": "Caller",
    "busyCallees": [],
    "callRecordUrl": "https://waybeo-airtel-callrecordings.s3.ap-south-1.amazonaws.com/82a7eea0-e786-43aa-a1a6-aea58c53bc2f.mp3",
    "dtmfKeys": [],
    "gateway": "Airtel",
    "callerRingDuration": 0,
    "ringDuration": 24,
    "callerStatus": "Answered",
    "calleeStatus": "Answered",
    "ivrDuration": 10,
    "busyCalleesStr": "",
    "correlationId": "Xchange82a7eea0-e786-43aa-a1a6-aea58c53bc2f",
    "callerNumber": "+917061649946",
    "answeredBy": "+919888412404"
  }
  ```

### CDR data params definition

| Parameter    | Definition | Type     | Available values | Remarks |  Datatype |
| ------------ | ---------- | -------- | ---------------- | ------- | ------- |
| callId    | generated from telecom side | Both | Unique string | xxxx | string |
| uniqueId    | generated from telecom side | Both | Unique string | xxxx | string |
| dateTime    | datetime | Both | xxxx | xxxx | string |
| dateTimeIso    | call date in ISO | Both | xxxx | xxxx | string |
| date    | call date | Both | xxxx | xxxx | string |
| callType    | call type | Both | INBOUND/OUTBOUND | xxxx | string |
| totalDuration    | endtime-start time | Both | xxxx | in seconds (ivr dur + conversation dur) | integer |
| conversationDuration    | conversation duration | Both | xxxx | in seconds | integer |
| virtualNumber    | virtual number | Both | Unique no | xxxx | string |
| status    | call status | Both | Missed/Answered/IVR drop/Offline | xxxx | Based on requirement |
| hangupLeg    | who end the call | Both | Caller/Callee | xxxx | string |
| busyCallees    | the priority list whose missed the calls | Both | xxxx | xxxx | array |
| callRecordUrl    | call record url | Both | xxxx | xxxx | string |
| dtmfKeys    | Multilevel ivr keys | Both | xxxx | 1-sales, 2-service | array |
| gateway    | network | Both | Airtel/Tata/Vodafone | xxxx | string |
| callerRingDuration    | customer ring duration | Both | xxxx | xxxx | integer |
| ringDuration    | total ring duration | Both | xxxx | xxxx | integer |
| callerStatus    | agent status | Both | Answered/Missed | xxxx | string |
| calleeStatus    | customer status | Both | Answered/Missed | xxxx | Alwasy _Answered_ in inbound |
| ivrDuration    | ivr duration | Both | xxxx | xxxx | integer |
| busyCalleesStr    | busyCallees type cast to string | Both | xxxx | xxxx | string |
| correlationId    | generated from telecom side | Both | xxxx | unique string | string |
| callerNumber    | custome number | Both | xxxx | xxxx | string |
| answeredBy    | agent number | Answered | xxxx | xxxx | string |