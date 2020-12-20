# Custom Metric Upload into CloudWatch

## Create Policy and Role
1. Services -> IAM -> Policies
2. "Create policy"
3. Service : CloudWatch
4. Actions
   1. Access level
   2. Write
      1. Check PutMetricData
5. Click "Review Policy"
6. Review Policy 
7.  Name : 
```bash
PutMetricRole20190815 
```
8. Click "Create policy"