# Security Tools installation

# ClamAV

ClamAV is a free, open source antivirus program for the detection of trojans, viruses and malware on your VPS.

# Installation ClamAV

yum -y install epel-release

yum -y update

yum -y install clamav-server clamav-data clamav-update clamav-filesystem clamav clamav-scanner-systemd clamav-devel clamav-lib clamav-server-systemd

rpm -qa | grep -i clamav  // check the packagaes

freshclam  // update the databases


cat /etc/cron.d/clamav-update //check cron 




