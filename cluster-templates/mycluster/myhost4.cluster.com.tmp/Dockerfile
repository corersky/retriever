FROM centos
RUN yum install git -y
RUN rm -rf /tmp/setup
RUN mkdir /tmp/setup
WORKDIR /tmp/setup
RUN git clone http://github.com/satzkumr/MapRRepoFiles.git
RUN yum clean all
RUN yum install java-1.7.0-openjdk.x86_64 -y 
RUN yum install *jdk-devel* -y
WORKDIR /tmp/setup/MapRRepoFiles
RUN cp /tmp/setup/MapRRepoFiles/startscript /usr/sbin
RUN chmod +x /usr/sbin/startscript
RUN cp /tmp/setup/MapRRepoFiles/5.1/* /etc/yum.repos.d/
RUN mkdir /tmp/nfsmount
RUN yum install nfs-utils -y
RUN yum install mapr-core mapr-fileserver -y
RUN yum install mapr-nodemanager -y
