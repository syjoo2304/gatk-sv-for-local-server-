# gatk-sv-for-local-server-
- It requires installation of human genome references, docker images, and cromwell.jar file.  For the download, please refer to https://github.com/broadinstitute/gatk-sv.  
- sample_format should be ~.bam and ~.bam.bai
- please edit 'GATKSVPipelineSingleSample.no_melt.json' json file to change the sample name , path to reference and docker images that you've built on your local server. 
- please edit 'cromwell.example.conf' file, for particularly changing the line starting with 'dockerRoot=' into any 'non-root' directory on your local server. example non-root directory: [directory-where-you-pull-the-git]/gatksv_run
- please run the command below in your local server.
java -Xmx128g -jar  -Dconfig.file=[directory-where-you-pull-the-git]/cromwell.example.conf [path-to-cromwell]/cromwell-57.jar run [directory-where-you-pull-the-git]/gatksv_run/wdl/GATKSVPipelineSingleSample.wdl --inputs [directory-where-you-pull-the-git]/GATKSVPipelineSingleSample.no_melt.json -p [directory-where-you-pull-the-git]/gatksv_run/wdl/dep.zip
