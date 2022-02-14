# Guard-duty #

Amazon GuardDuty is a continuous security monitoring service that analyzes and processes the following Data sources: VPC Flow Logs, AWS CloudTrail management event logs, CloudTrail S3 data event logs, and DNS logs. It uses threat intelligence feeds, such as lists of malicious IP addresses and domains, and machine learning to identify unexpected and potentially unauthorized and malicious activity within your AWS environment. This can include issues like escalations of privileges, uses of exposed credentials, or communication with malicious IP addresses, or domains.

## Structure

follwing are the resources that guardduty requires.

### Guardduty-detector

We are creating a `Guardduty-detector`,The `aws_guardduty_detector` resource specifies a new Amazon GuardDuty detector. A detector is an object that represents the Amazon GuardDuty service. A detector is required for Amazon GuardDuty to become operational

### S3 bucket

we are creating a `s3-bucket`,with the name `spanio-gaurdduty-information` the s3 bucket consists of a file name `spanio-guardduty-threat-list` this file will consist of known malicious IP addresses currently this list consists of the ip address `10.0.0.0/8` as we need to give aleast one ip address.This bucket is encrypted using default aws/s3 AWS KMS master key

### Guardduty

we are creating guardduty with the name `spanio-guardduty`.


