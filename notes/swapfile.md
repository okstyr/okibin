# to create a swapfile

    free -h
    sudo fallocate -l 4G /swapfile
    sudo chmod 600 /swapfile
    ls -lh /swapfile

# to activate it by hand

    sudo mkswap /swapfile
    sudo swapon /swapfile
    sudo swapon --show
    free -h

# do it in fstab instead

    echo '/swapfile none swap sw 0 0' | sudo tee -a /etc/fstab
