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
Cloud Custodian is a tool that unifies the dozens of tools and scripts most organizations use for managing their public cloud accounts into one open source tool. It uses a stateless rules engine for policy definition and enforcement, with metrics, structured outputs and detailed reporting for clouds infrastructure. It integrates tightly with serverless runtimes to provide real time remediation/response with low operational overhead.

Organizations can use Custodian to manage their cloud environments by ensuring compliance to security policies, tag policies, garbage collection of unused resources, and cost management from a single tool.

Cloud Custodian can be bound to serverless event streams across multiple cloud providers that maps to security, operations, and governance use cases. Custodian adheres to a compliance as code principle, so you can validate, dry-run, and review changes to your policies.

Cloud Custodian policies are expressed in YAML and include the following:

The type of resource to run the policy against

Filters to narrow down the set of resources

Actions to take on the filtered set of resources

Here AWS Cloud custodian package is installed
or, visit https://aws.amazon.com/blogs/opensource/compliance-as-code-and-auto-remediation-with-cloud-custodian/


Here i have run some use cases for cloud custodian
Use Cases:
1.Find all running EC2 instances that are using invalid AMIs and stop them  (check custodian_polices.yml)

2.Filter any security group that allows 0.0.0.0/0 or ::/0 (IPv6) ingress on port 22, remove the rule (check custodian_polices.yml)

3.Find all non-compliant tag instances to stop in 1 day (check custodian_polices.yml)

4.Cloud Service Limit (check  cloudservicelimit.yml & servicelimitt.yml)

5.Find all the instances (check old-instances.yml)

6.

7.

8.

9.

10.

11.

12.

13.

14.

15.

16.

17.

18.

19.

20.
