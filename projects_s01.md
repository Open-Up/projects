# Projects semester 1

## 1 : Event supervision

Whatching out a server is something important. As a system administrator, you want to be able to detect attackers. In order to do so :
 
 - You will log every time some change is detected on /etc/passw on /etc/sudoers. In case change is detected, log it in live.
 - On each boot you will check the SHA-1 hash of both file. In case changes is detected, send a mail to the administrator.
 - You will log every TCP connection opened.
 - Send a mail to the administrator upon somebody login
 - Install and set up tripwire

You will provide a GitHub GIST detailing how to do the different steps.

Keywords : Security, detection, incon, bash scripts, update-rc

## 2 : James supervision (deploying James + setting up JMX)

James is a Java Apache Mail Enterprise Server. It's one openSource project Linagora is heavily contributing to. As part of a client request, we recently introduced the metric feature. Such metrics are exposed via JMX.

You will :
 - Start a James server inside docker
 - Add documentation in James README on how to read such metrics from the command line. You will make your pull request on https://github.com/apache/james-project .

Keyword : OpenSource contribution, JMX, docker, James


## 3 : Merging github into SVN

As part of the James project, we have SVN repository backed on Github. Some people propose us pull requests on Github. We then need to apply them on SVN. Today we do it manually, which takes time. We would like to have some script to do it automatically.

You will provide a Github repository holding the script and describing how to use it.

Keywords : Script, svn, github

## 4 : Install archlinux in VM with encrypted disks

Your company is willing to invest on security, and wants to set up server disk encryption.

You will provide a Github GIST on how to install an Archlinux server with encrypted LVM volumes.

Keywords : installation, archlinux, lvm, encryption, security

## 5 : Firewall project

As part of OpenUp, we want to protect the computers from the class from being freely accessed on the network. You will propose a firewall script enabling protection. This firewall will act as a gateway. Here are the rules : 
 - No peer to peer protocols
 - Disable hosts from China
 - Allow outgoing TCP/UDP connections
 - Allow incoming connections only above port 1024
 - Drop non conventionnal TCP opening
 - Do not check if the connection is already established
 - Have some checks on ICMP
 - Protect against some known malware ports
 - Not relay 10.0.0.0/8
 - Do not allow external VMs to spoof internal IPs
 - Do not allow internal VMs to spoof exteral IPs
 - You will provide a simple mechanism for blackList. You will blacklist Facebook.com
 - You will provide protection over DoS by providing a limit of opened connection per seconds.

Your internal virtual machines will use internal virtualbox network intern_net_1. You will create VMs connected to intern_net_2. Your firewall will be the gateway between intern_net_1 and intern_net_2. intern_net_1 holds "openup computers" (internal). internet_net_2 is external.

You will provide : 
 - A script designating these rules
 - A init script
 - A README explaining the choices you made for each rule
 - The README will contain indications on how to enable the firewall on boot.

Keywords : IPtables, init.rc, security

## 6 : SVG ZFS

As a system administrator, you are willing to invest wether it is valuable to use the ZFS technology. ZFS is some advanced filesystem looking like BTRfs.

 - You will install ZFS on openSolaris
 - You will create snapshots
 - You will send these snapshots to an other ZFS server every hour
 - You will create a script for cleaning snapshots. We one to keep one snapshot per day after 1 day. 1 snapshot per week after one week. 1 snapshot per month after one month.

You will provide a github repository with : 
  - A README with the steps to follow to install this backup solution
  - The script for cleaning SNAPSHOTs

Keywords : ZFS, scripting, cron

## 7 :  Create Debian mirrors

Your organisation want to save bandwith and makes debian upgrades faster.

You will provide a GIST detailling how to install Debian mirror. You will show with a virtual machine how to use your mirror.

Keywords : APT, debian, mirror

## 8 : Home backup 

You will write a script to back up your home folder. It will produce an archive of your home folder.

Here are the features :

1) accepting different compression algorithms as arguments
2) checking for the presence of different compression programs and using the "best" one it finds
3) comparing the size of today's archive to yesterdays and sending the user an email if it changed significantly

You will also enable it every day at 5pm.

You will provide a Github repository with the script, and a README detailling how to use it.

Keywords : Scripting, cron
