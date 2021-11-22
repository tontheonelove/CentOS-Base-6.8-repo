# CentOS-Base-6.8-repo


# CentOS-Base.repo
#
# The mirror system uses the connecting IP address of the client and the
# update status of each mirror to pick mirrors that are updated to and
# geographically close to the client.  You should use this for CentOS updates
# unless you are manually picking other mirrors.
#
# If the mirrorlist= does not work for you, as a fall back you can try the 
# remarked out baseurl= line instead.
#
#

[C6.8-base]
name=CentOS-6.8 - Base
baseurl=http://vault.centos.org/6.8/os/$basearch/
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6
enabled=1
metadata_expire=never

[C6.8-updates]
name=CentOS-6.8 - Updates
baseurl=http://vault.centos.org/6.8/updates/$basearch/
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6
enabled=1
metadata_expire=never

[C6.8-extras]
name=CentOS-6.8 - Extras
baseurl=http://vault.centos.org/6.8/extras/$basearch/
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6
enabled=1
metadata_expire=never

[C6.8-contrib]
name=CentOS-6.8 - Contrib
baseurl=http://vault.centos.org/6.8/contrib/$basearch/
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6
enabled=0
metadata_expire=never

[C6.8-centosplus]
name=CentOS-6.8 - CentOSPlus
baseurl=http://vault.centos.org/6.8/centosplus/$basearch/
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6
enabled=0
metadata_expire=never


##################################################################################

#add this
vi /etc/yum.conf

sslverify=false

#################

yum clean all
