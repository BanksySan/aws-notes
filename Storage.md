# Storage

| Term | Definition              | Notes                 |
|------|-------------------------|-----------------------|
| EBS  | Elastic Block Storage   | Block-level storage.  |
| S3   | Simple Storage Solution | Object-level storage. |
|      |                         |                       |

### EBS

Use EBS for data that requires frequent updating.

#### EBS types

| Code        | Description              | Typical Usage                                     |
|-------------|--------------------------|---------------------------------------------------|
| `gp2` `gp3` | General Purpose SSD      |                                                   |
| `io1` `io2` | Provisioned IOPS SSD     | Mission critical.  High throughput.  Low latency. |
| `st1`       | Throughput Optimised HDD | Lower cost than `io*`.  High throughput.          |
| `sc1`       | Cold HDD                 | Lowest cost HDD.  Low throughput.                 |
|             | Magnetic (standard)      | Infrequently accessed data.                       |

* * 
