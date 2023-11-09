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

# Lynis 

Lynis is a battle-tested security tool for systems running Linux, macOS, or Unix-based operating system.

Use cases of Lynis

1. Security auditing
2. Compliance testing
3. Penetration testing
4. Vulnerability detection
5. System hardening


# Download and Installation of Lynis

 git clone https://github.com/CISOfy/lynis 

 cd lynis 

 ./lynis audit system 