# .bashrc

# Source global definitions
if [ -f /etc/bashrc ]; then
	. /etc/bashrc
fi

# Uncomment the following line if you don't like systemctl's auto-paging feature:
# export SYSTEMD_PAGER=
# User specific aliases and functions
alias afastart="~/bin/afastart"
alias afastop="~/bin/afastop"
alias log-1="cd ~/log/app/$(date -d '1 day ago' +%Y%m%d)/upbs/"
alias log-2="cd ~/log/app/$(date -d '2 day ago' +%Y%m%d)/upbs/"
alias log="cd ~/log/app/$(date +%Y%m%d)/upbs/"

export PS1='$PWD >'
alias l="ls -lrt"
alias anyang="cd ~/user/anyang/"

#rm to mv begin
mkdir -p ~/.trash
alias rm=trash
alias r=trash
alias rl='ls ~/.trash'
alias ur=undelfile
alias clear=cleartrash
undelfile(){
	mv -i ~/.trash/$@./
}

trash(){
	mv $@ ~/.trash/
}

cleartrash(){
	 /usr/bin/rm -rf ~/.trash/*
}

#rm to mv end
export JAVA_HOME=/lib/jvm/java-1.8.0-openjdk-1.8.0.131-11.b12.el7.x86_64
export ORACLE_SID=GENDB2
export ORACLE_HOME=/home/afa4sj/oracle/product/10.2.0/db_1
export TNS_ADMIN=$ORACLE_HOME/network/admin 
export NLS_LANG="AMERICAN_AMERICA.ZHS16GBK"
export LD_LIBRARY_PATH=$ORACLE_HOME/lib
export PATH=$ORACLE_HOME/lib:$PATH
