# Custom Metric Upload into CloudWatch

## Create Policy and Role
   1. Services -> IAM -> Policies
   2. "Create policy"
      1. Service : CloudWatch
      2. Actions
         1. Access level
            1. Write
               1. Check PutMetricData
      3. Click "Review Policy"
      4. Review Policy 
         1. Name : 
```bash
         1.  PutMetricRole20190815 
         2.  ```