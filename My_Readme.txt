Ruby 2.5.* Rails 6.0.3.1

On Terminal:
To install  Ruby Version Manager (RVM)
https://github.com/rvm/ubuntu_rvm
sudo apt-get install software-properties-common
sudo apt-add-repository -y ppa:rael-gc/rvm
sudo apt-get update
sudo apt-get install rvm
CC: For verify the versio of RVM:
rvm --version
CC:To list all ruby avaliable for install:
rvm list known
Install Ruby with RVM and specif version:
rvm install 2.4
CC:afther install
ruby -v
CC: To use some version
rmv use 2.4 default
CC: To list all versions of Ruby installed with RVM:
rvm list

CC: To install RAILS
gem install rails
rails -v

CC: Install nodeJS
sudo apt-get install nodejs

CC: Install config Mysql

sudo apt-get install mysql-client mysql-server libmysqlclient-dev

sudo mysql -u root -p
alter user 'root'@'localhost' identified with mysql_native_password by 'L4st_0ff_D4t4';
flush privileges;
mysql -u root -p

CC: Install and configure PostgreSQL

sudo apt-get install postgresql postgresql-contrib libpq-dev
sudo -u postgres createuser -rds pippo
createdb pippo
quit;

CC: To creat a new app for the mysql DB:
rails new testapp-mysql -d mysql
cd testapp-mysql
modify de file /config/database.yml adding the pwd for DB

rails db:create db:migrate
rails s

CC: To creat a new app for the postgres DB

rails new testapp-postgres -d postgresql
modify de file /config/database.yml adding the pwd for DB
rails db:create db:migrate
rails s


CC: App wee will create an app for answers frequently questions.
rails new time_to_answer
rails g controller welcome index