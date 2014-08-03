need this in your .bashrc (or so)

    /usr/sbin/anacron -t ${HOME}/okibin/.anacron/anacrontab -S ${HOME}/okibin/.anacron/timestamps &> ${HOME}/okibin/.anacron/anacron.log

then it will fire off anacron every time you log in 
