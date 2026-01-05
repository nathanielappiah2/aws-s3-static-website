## UC2: EC2 Instance Type Modification

### Objective
Optimize EC2 costs by right-sizing an overprovisioned instance.

### Business Context
Monitoring showed the EC2 instance was consistently underutilized,

using ~10% CPU and ~300MB of 1GB RAM. The instance was larger than required
for the workload.

By resizing from `t2.micro` to `t2.nano`, costs were reduced while maintaining
adequate performance.

### Action Taken
- Stopped the EC2 instance (required for instance type changes)
- Modified instance type via AWS Console
- Restarted the instance
- Verified functionality and instance health

### Outcome
- Instance successfully running as `t2.nano`
- Lower ongoing cost
- No functional impact to the workload

### Key Learning
EC2 instance type changes require planned downtime. In production
environments, changes should be scheduled during maintenance windows.

## Evidence

### Instance type changed to t2.nano
![Instance type changed to t2.nano](./screenshots/uc2/IMG_5509.png)

### Instance running successfully
![Instance running successfully](./screenshots/uc2/IMG_5512.png)
