# Notes on using Pulumi
Manage all multi-cloud operations from Pulumi.
Pulumi manages allocating and teardown of infastructure.


## Questions
- How are stacks run when interfacing with underlying cloud products?
- How are those services paid for on Pulumi free?
- How are costs passed on the users?



### Projects - YAML file holding metadata for current project.
`name` Req. 
`runtime` Req. Language of program.

### Stacks
Program running in Pulumi.  An isolated independent instance of Pulumi.  
Commonly used as different phases in development (SDLC).  Ex. DEV, STAGING, PROD

`pulumi stack init <stackname>` default set as active stack.



Each of these has a corresponding Pulumi.yaml file. 



`pulumi up` will activate the stack for the cloud environment.


