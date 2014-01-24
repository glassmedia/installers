#Create rpm for zpphp

<code>yum -y install bzip2-devel gmp-devel --downloadonly --downloaddir=$HOME/rpmbuild/RPMS/$(uname -m)</code>

<code>yum -y install bzip2-devel gmp-devel apr-util-ldap</code>

<code>cd $HOME/rpmbuild/SOURCES</code>

<code>git clone https://github.com/php/php-src.git zpphp-5.4.24</code>

<code>cd zpphp-5.4.24</code>

<code>git checkout php-5.4.24</code>

<code>cd ..</code>

<code>tar -cvf zpphp-5.4.24.tar.bz2 zpphp-5.4.24</code>

<code>rm -rf zpphp-5.4.24</code>

<code>wget https://github.com/zpanel/installers/raw/master/install/CentOS-6_4/compile/zpphp/php-$(uname -m).spec \ </code>

<code>-P $HOME/rpmbuild/SPECS</code>

<code>rpmbuild -ba $HOME/rpmbuild/SPECS/php-$(uname -m).spec</code>