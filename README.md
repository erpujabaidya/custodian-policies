         ___        ______     ____ _                 _  ___  
        / \ \      / / ___|   / ___| | ___  _   _  __| |/ _ \ 
       / _ \ \ /\ / /\___ \  | |   | |/ _ \| | | |/ _` | (_) |
      / ___ \ V  V /  ___) | | |___| | (_) | |_| | (_| |\__, |
     /_/   \_\_/\_/  |____/   \____|_|\___/ \__,_|\__,_|  /_/ 
 ----------------------------------------------------------------- 


Hi there! Welcome to AWS Cloud9!

To get started, create some files, play with the terminal,
or visit https://docs.aws.amazon.com/console/cloud9/ for our documentation.

Happy coding!
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Cloud Custodian is a tool that unifies the dozens of tools and scripts most organizations use for managing their public cloud accounts into one open source tool. It uses a stateless rules engine for policy definition and enforcement, with metrics, structured outputs and detailed reporting for clouds infrastructure. It integrates tightly with serverless runtimes to provide real time remediation/response with low operational overhead.

Organizations can use Custodian to manage their cloud environments by ensuring compliance to security policies, tag policies, garbage collection of unused resources, and cost management from a single tool.

Cloud Custodian can be bound to serverless event streams across multiple cloud providers that maps to security, operations, and governance use cases. Custodian adheres to a compliance as code principle, so you can validate, dry-run, and review changes to your policies.

Cloud Custodian policies are expressed in YAML and include the following:

1.The type of resource to run the policy against

2.Filters to narrow down the set of resources

3.Actions to take on the filtered set of resources
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Here AWS Cloud custodian package is installed
or, visit https://aws.amazon.com/blogs/opensource/compliance-as-code-and-auto-remediation-with-cloud-custodian/

Install Custodian in the aws cloud9 environment
1. python3 -m venv custodian
2. source custodian/bin/activate
3.  pip install c7n   # Install AWS package
4. custodian validate <yml_file> # We must validate Cloud Custodian policies against the JSON schema before processing
5. custodian run --dryrun <yml_file> -s out # Performming a dry-run command before running the command on infrastructure is usually preferred.
6. custodian run <yml_file> -s out # we use the report subcommand to summarize 
7. custodian report <yml_file> -s out --format grid # Everything looks as expected, so now we are going to run the policies

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


Use Cases:
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
1.Find all running EC2 instances that are using invalid AMIs and stop them  (check custodian_polices.yml)

2.Filter any security group that allows 0.0.0.0/0 or ::/0 (IPv6) ingress on port 22, remove the rule (check custodian_polices.yml)

3.Find all non-compliant tag instances to stop in 1 day (check custodian_polices.yml)

4.Cloud Service Limit (check cloudservicelimit.yml & servicelimit.yml)

5.Find all the old instances (check old-instances.yml)

6. Recommend Use - AWS Organizations , check if config is enabled or not (check aws-organization-check-config.yml)

7.Check MFA root aacess (check checkmfaroot.yml)

8.Cloud trail logging disabled (check cloudtrailloggingdisabled.yml)

9.Cloud trail for s3 access enabled (check cloudtrailloggingdisabled.yml )

10.Cloud trail logging enabled (check cloudtrailenabled.yml)

11.Delete old snapshot that exceeds particular days (check delete-old-snapshot.yml)

12.Delete resources without tags (check deleteresources-without-tags.yml)

13.Find resources without tags (check findresources-withouttags.yml)

14.Deregister old ami (check deregister-old-ami.yml)

15.Some use cases for ebs policies (check ebs-policies.yml)

16.IAM users doesn’t exist in groups (check empty-iam-group.yml)

17.Find idle instances (check findidleinstance.yml)

18.IAM user inactivity exceeds 10 days (check  iam-inactivity.yml)

19.Users with MFA disabled (check mfa-disabled.yml)

20.Modify CPU utilization (check modifycpuutilization.yml)

21.Old Instance generation  (check old-instances.yml)

22.RDS public access (check rds-public-access.yml)

23.S3 public access off (check  s3-publicaccessoff.yml  )

24.Block S3 public access(check s3-public-blockpolicy.yml)

25.Scheduled Resource scheduling (check schedulingresources.yml)

26.Unrestricted SG (check unrestrictedSG.yml)

27.Unused EC2 key pair (check unusedec2-keypair.yml)

28.Unused ELB (check unused-ebl.yml)

29.Creates a Weekly Cron Scheduled CWEvent to Snapshot single non-cluster RDS Instances weekly if tagged (check weeklysnapshot-rds.yml )



------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


One more interesting way to do is
Click on the AWS Security Hub --> Integrations --> Cloud Custodian --> Accept All findings --> It will find all the violated rules --> We can remediate also from the AWS console only.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------




