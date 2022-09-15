 # Spark Memory Calculator

## Description
Excel workbook to calculate Spark memory settings. This is specifically for spark application avalable in an EMR.  
Used this [AWS bigdata blog post](https://aws.amazon.com/blogs/big-data/best-practices-for-successfully-managing-memory-for-apache-spark-applications-on-amazon-emr/) to create it.

Since creation of this workbook AWS EMR has introduced features that eliminate the need for calculating sizing for individual workloads.
See:
* [emr managed scaling](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-managed-scaling.html)
* [maximizeResourceAllocation](https://docs.aws.amazon.com/emr/latest/ReleaseGuide/emr-spark-configure.html)

I've tipicaly used this tool for legacy system that cannot upgrade to newer version of EMR.
And to remediate memory related issues for workloads where spark code optimization is not an option.

## Usage

Inputs for the workbook

### Vcpu :  
Number of vCPU available for the selected instance type. Eg. for m5.4xlarge it is 16  


### Memory(GiB) : 
Memory available for the selected instance type. Eg. for m5.4xlarge it is 64  


### #Nodes :  
Number of Cluster nodes  


### Cores per executor:  
Value set for spark.executor.cores  
