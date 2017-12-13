# Supported Parameters

## Direct stream / Structured stream

The following parameters are supported for both the Direct stream and Structured stream use cases.

| Parameter | Meaning | Required |
| --------- | ------- | -------- |
| `policyname` | EventHub connection policy name. Can be created on a namespace or individual EventHub level. It needs to have `Listen` permissions. | Yes |
| `policykey` | Key associated with the above policy. | Yes |
| `namespace` | EventHub namespace to connect to. | Yes |
| `name` | EventHub name within the namespace. | Yes |
| `partition.count` | Number of partitions available in the EventHub. | Yes |
| `consumergroup` | Consumer group to use when connecting. **Note:** Only one connection can be active per consumer group at a time. | Yes |
| `progressTrackingDir` | Directory to use to store progress files in. This is so your progress in the event stream won't be lost in case of job restarts. | Yes |
| `maxRate` | Maximum number of events to consume **per partition** per batch. | No, defaults to 10000 |

## Structured stream

The following parameters are only relevant for the Structured stream use cases, in addition to the ones above.

| Parameter | Meaning | Required |
| --------- | ------- | -------- |
| `sql.containsProperties` | Set to `true` if you want to extract custom properties from the Event properties | No |
| `sql.userDefinedKeys` | Comma-separated names of properties to extract from Event properties. | No |
