# AWSCLI-Commands

Display all the ec2 instance id, instance state, volumes attached devicename and Tag key as Name
----------------------------

aws ec2 describe-instances --query "Reservations[*].Instances[*].[InstanceId, State.Name,BlockDeviceMappings[*].DeviceName,BlockDeviceMappings[*].Ebs,BlockDeviceMappings[*].VolumeId,Tags[?Key=='Name'].Value]" --profile=profile-name --output json

