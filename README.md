# TermuxSetup
Setup Termux Terminal Mobile 

# Install ssh
  pkg update && pkg upgrade -y
   pkg install openssh -y
   passwd
   ifconfig
   echo "sshd" >> ~/.bashrc
   nano $PREFIX/etc/ssh/sshd_config
   Port 8022
   pkill sshd
   sshd
 
# Install mariadb
  pkg install mariadb
   mysqld_safe -u root
   mysql -u root

# Install Ubuntu no desktop
  pkg update && pkg upgrade
  pkg install proot-distro git wget curl neofetch -y
  proot-distro install ubuntu
  proot-distro login ubuntu
  apt update && apt upgrade -y
