FROM biocontainers/biocontainers:vdebian-buster-backports_cv1
MAINTAINER biocontainers <biodocker@gmail.com>
LABEL    software="rdp-readseq" \ 
    base_image="biocontainers/biocontainers:vdebian-buster-backports_cv1" \ 
    container="rdp-readseq" \ 
    about.summary="Ribosomal Database Project (RDP) sequence reading and writing" \ 
    about.home="https://github.com/rdpstaff/ReadSeq" \ 
    software.version="2.0.2-6-deb" \ 
    upstream.version="2.0.2" \ 
    version="1" \ 
    about.copyright="2006-2012 Michigan State University <rdpstaff@msu.edu>," \ 
    about.license="GPL-3+" \ 
    about.license_file="/usr/share/doc/rdp-readseq/copyright" \ 
    extra.binaries="/usr/bin/rdp-readseq" \ 
    about.tags=""

USER root
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update && (apt-get install -t buster-backports -y rdp-readseq || apt-get install -y rdp-readseq) && apt-get clean && apt-get purge && rm -rf /var/lib/apt/lists/* /tmp/*
USER biodocker
