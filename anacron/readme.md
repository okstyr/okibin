need this in your .bashrc (or so)

mkdir -p ${HOME}/.anacron/timestamps
/usr/sbin/anacron -t ${HOME}/okibin/anacron/anacrontab -S ${HOME}/.anacron/timestamps &> ${HOME}/.anacron/anacron.log
then it will fire off anacron every time you log in

although all the files exist here, its nicer to write timestamps and logs
to $HOME/.anacron


