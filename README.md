## Give your Application Auto-Deploy Superpowers

Implementing these stages of CI/CD pipline using CirclecCi tool :

- Build Phase for building both of front-end and back-end

- Test Phase providing Unit tests for both front-end and back-end

- Analyze Phase for scanning and checking known vulnerabilities in  the packages used in the application

- Create/Deploy Infrastructure Phase:
using cloudformation to provision back-end and front-end stacks, 

- Configure Infrastructure Phase:
setting up the back-end server using Ansible.

- Run DB Migrations:
to ensure that new changes are applied

- Deploy Front-End:
coping build files to the S3 bucket utilizing AWS CLI

- Deploy Back-End:
coping compiled bakend files to the EC2 instance using Ansible.

- Smoke Test Phase:
  doing curl on both front-end and back-end to make sure both of them are responding in an automated senario.

- Rollback Phase:

  Incase any smoke test fails destroy-environment and revert last migration to roll back any migrations that were successfully applied during this CI/CD
  workflow.

- Promotion Phase:

 as we approach Blue-Green Deployment Strategy, this job is to switch from blue to green, sothat cloudfront distribution's origin get changed to the new S3 bucket.

-  Cleanup Phase:
deleting the previous(blue) stacks/files.


![Diagram of this CI/CD Pipeline .](udapeople.png)



### Built With

- [Circle CI](www.circleci.com) - Cloud-based CI/CD service
- [Amazon AWS](https://aws.amazon.com/) - Cloud services
- [AWS CLI](https://aws.amazon.com/cli/) - Command-line tool for AWS
- [CloudFormation](https://aws.amazon.com/cloudformation/) - Infrastrcuture as code
- [Ansible](https://www.ansible.com/) - Configuration management tool
- [Prometheus](https://prometheus.io/) - Monitoring tool

### License

[License](LICENSE.md)
