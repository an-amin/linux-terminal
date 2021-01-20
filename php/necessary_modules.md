## Install Python dependency

Not needed in Ubuntu 16.04 
````
sudo apt install python-software-properties
````
or, 

Not needed in Ubuntu 18.04 
````
sudo apt install software-properties-common
````


## Add repo 
````
sudo add-apt-repository ppa:ondrej/php
````

# Update apt 
````
sudo apt update && apt upgrade -y
````


## Necessary PHP Modules

### to install latest PHP version

````
apt install php php-fpm php-common php-cli php-curl php-zip php-intl php-mbstring php-json php-xml php-gd  php-bcmath php-tokenizer php-mysql
````


### to install PHP 7.2 

````
apt install php7.2 php7.2-fpm php7.2-common php7.2-cli php7.2-curl php7.2-zip php7.2-intl php7.2-mbstring php7.2-json php7.2-xml php7.2-gd  php7.2-bcmath php7.2-tokenizer php7.2-mysql
````


### to install PHP 5.6 

````
apt install php5.6 php5.6-fpm php5.6-common php5.6-cli php5.6-curl php5.6-zip php5.6-intl php5.6-mbstring php5.6-json php5.6-xml php5.6-gd  php5.6-bcmath php5.6-tokenizer php5.6-mysql
````

