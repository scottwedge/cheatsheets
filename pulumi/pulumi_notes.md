# Notes on using Pulumi
Manage all multi-cloud operations from Pulumi.
Pulumi manages allocating and teardown of infastructure.


## Questions
- How are stacks run when interfacing with underlying cloud products?
- How are those services paid for on Pulumi free?
- How are costs passed on the users?

- Where is the line between AWS and Pulumi?
    - What is up to Pulumi only?

- publicHostName changes in between pulumi updates, temp ip?

- Would I be able to use AWS EC2 with GCP Storage?



### Projects - YAML file holding metadata for current project.
`name` Req. 
`runtime` Req. Language of program.

### Stacks
Program running in Pulumi.  An isolated independent instance of Pulumi.  
Commonly used as different phases in development (SDLC).  Ex. DEV, STAGING, PROD

`pulumi stack init <stackname>` default set as active stack.



Each of these has a corresponding Pulumi.yaml file. 



`pulumi up` will activate the stack for the cloud environment.



## Under the hood

### State
Copy of hte current state.  Snapshots are stored at checkpoints.

### Backends
Pulumi supports mulitple backends either cloud or on-premesis.


![Architecture](https://www.pulumi.com/images/docs/reference/state_saas.png)


Networks are managed by Pulumi.
## Security
The backend is encrypted in transit and at rest.  

Role based access control.  


