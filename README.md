This repository shows you how to setup crontab in Linux OS such as RHEL 7.x/8.x and CentOS
# CronJobs:
Cron job is a time-based job scheduler in Unix-like computer operating systems.
# Crontab:
The crontab is a list of commands that you want to run on a regular schedule, and also the name of the command used to manage that list.

Please note:
Prior to setup cronjobs in CentOS/RHEL, we need to take a look at the OS whether the cron package has installed or not.If not, we need to install first and begin the process,

$ yum list updates        --> Display a list of updated software and security fix
$ yum check-update        --> Updates exist for packages that are already installed on my system
$ yum update              --> Patch up system by applying all updates
$ sudo yum update --security --> It will only apply security-related package updates
$ rpm -qa                 --> List all installed packages  (OR)
$ yum list installed      --> List all installed packages
$ rpm -qa | grep httpd*   --> Find out if httpd related package installed or not on the system
$ yum list installed httpd  --> Find out if httpd package installed or not on the system

# cron package is not installed on the system
***********************************************************************************************************************************************
$ sudo yum install yum-cron -->  Install yum-cron on a CentOS/RHEL 6.x/7.x OS

# Turn on service using systemctl command on CentOS/RHEL 7.x:
************************************************************************************************************************************************
$ sudo systemctl enable yum-cron.service
$ sudo systemctl start yum-cron.service
$ sudo systemctl status yum-cron.service

$ sudo chkconfig yum-cron on
$ sudo service yum-cron start

Happy Learning...!!

