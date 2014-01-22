# apt-fast #

    sudo apt-get install axel aria2
    sudo add-apt-repository ppa:apt-fast/stable
    sudo apt-get update
    sudo apt-get install apt-fast  
    
    sudo echo "alias apt-get='apt-fast'" >> ~/.bashrc
    // 新配置apt-fast选项
    sudo dpkg-reconfigure apt-fast
    
# 校验和#
    
    sudo mv /var/lib/apt/lists /var/lib/apt/lists.bak
    sudo mkdir /var/lib/apt/lists

    // 修改/etc/apt/apt.conf.d/00aptitude
    // 最后加一行: Acquire::CompressionTypes::Order "gz";
    sudo echo "" >> "Acquire::CompressionTypes::Order 'gz';" /etc/apt/apt.conf.d/00aptitude
    
