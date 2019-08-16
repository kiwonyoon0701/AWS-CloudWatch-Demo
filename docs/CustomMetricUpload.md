# Custom Metric Upload into CloudWatch

## Create Policy and Role
1. Services -> IAM -> Policies
2. "Create policy"
3. Service : CloudWatch
4. Actions
5. Access level
6. Write
7. Check PutMetricData
8. Click "Review Policy"
9. Review Policy 
10. Name : 
```bash
PutMetricRole20190815 
```