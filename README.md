# gatk-sv-for-local-server-
# - It requires installation of human genome references, docker images, and cromwell.jar file.  For the download, please refer to https://github.com/broadinstitute/gatk-sv.  
# - sample_format should be ~.bam and ~.bam.bai
# - please edit 'GATKSVPipelineSingleSample.no_melt.json' json file to change the sample name , path to reference and docker images that you've built on your local server. 
# - please edit 'cromwell.example.conf' file, for particularly changing the line starting with 'dockerRoot=' into any 'non-root' directory on your local server. example non-root directory: [directory-where-you-pull-the-git]/gatksv_run
# - please run the command below, after all of the works.
  
