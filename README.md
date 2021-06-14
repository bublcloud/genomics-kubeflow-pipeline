# genomics-kubeflow-pipeline
Example kubeflow pipeline of genome sequence preprocessing

## Based on

https://gitlab.oit.duke.edu/dcibioinformatics/soft/gatk-sigularity-pipeline/-/blob/master/pipeline/gatk4-preprocessing-eks/gatk-pre.workflow

## Modifications
Three modificatins are made to the orignal flow. 
1) set compression level of output to 1 (speeds up the flow with minimal effect on data size)
2) use spark version of BaseRecalibrator (beta), that allows for multi threading.
3) slightly adjusted the command to collect the RGID from the example fastq.gz files.
4) encryption is already done by node to node network. Using http for minio storage instead of https.
