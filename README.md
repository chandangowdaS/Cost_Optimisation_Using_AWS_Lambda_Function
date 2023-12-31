# Cost_Optimisation_Using_AWS_Lambda_Function

1. Create EC2 Instance

![Alt text](Created_EC2_Instance.png)

2. Check the Volume of Instance

![Alt text](Volume_OF_Instance.png)

3. Create a Snpashot for Volume of EC2 instance created

![Alt text](Created_Snpashot_of_volume_of_EBS.png)

4. Created Lambda Function

![Alt text](Created_Lambda_Function.png)

5. Timeout of test code increase to 5 seconds

![Alt text](Timeout_Increase_5_sec.png)

6. Created custom policy LIST_AND_DELETE_SNAPSHOT for giving access to lambda function to fetch the snapshot which is not associated to EC2 or EBS to delete it

![Alt text](Created_custom_policy_LIST_AND_DELETE_SNAPSHOT.png)

7. Attached two policies  to Lambda function which will fetch the snapshot and check whether it is associated to EC2 or EBS if it is not associated to EC2 or EBS it will delete the snapshot

![Alt text](Attached_policy_Lambda.png)

8. Test failed due to instance was running for that snapshot

![Alt text](Test_failed_due_to_instance_running.png)

9. Instance terminated which was created at 1 step

![Alt text](Instance_terminated.png)

10. Only snapshot remained and rest resources such as EC2 and volume deleted

![Alt text](Only_snapshot_remained_rest_deleted.png)

11. Test output that snapshot deleted because no EC2 nor any volume was attached to snapshot

![Alt text](Test_output_that_snapshot_deleted.png)

12. Output that Snapshot was deleted and can be seen that in dashboard

![Alt text](Snapshot_deleted_Dashboard.png)
