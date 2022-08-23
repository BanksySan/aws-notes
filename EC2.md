# EC2

## Glossary

| Term   | Definition        | Notes        |
|--------|-------------------|--------------|
| Volume | Data/file storage | Could be EBS |
|        |                   |              |

## Encryption

Encryption isn't required.  When it is enabled:

* Uses KMS keys.

* AES-256

* Happens on the EC2 instance attached.
  * Secures
    * Data at rest
    * Data in transit

## Key Pairs

Credentials to authenticate when connecting to EC2.  When an instance initially boots, the contents of its public key is places in `~/.ssh/authorized_keys`.  When you log into a Linux instance you need to specify the private key that corresponds to the public key that the instance has stored.
In order to share a volume the instances *must* be in the same availability zone.
The volumes being shares *must* be IOPS Provisioned.

## Managing Instances

### Security

* Least permissive rule set.
* Apply patches to keep the instances up-to-date.

#### Storage

* Separate OS and data onto separate (EBS) volumes.
* Don't use ephemeral volumes for critical data.
* Perform EBS snapshots to allow disaster recovery.
