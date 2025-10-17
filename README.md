# commands


DOS
 cd: moving between directories
 ls: list directory & files
 ls -a: list hidden files and directories
 ls -l: long listing of directories & files
 touch <name>: create file
 nano filename: create and open a file if not exists
 mkdir: create directory
 rm filename.ext: delete file
 rmdir: remove directory
 rm -r: remove directory with content
 mv <name> <new name>: move or rename directory & files
 cp -r <source> <destination> : copy directory & files recursively
 grep -r “error” <directory/file>: search for a pattern recursively in all files in a directory
 find <directory> -name "*.jpg”: search for all jpg files in given directory and its subdirectories
 find / -name “filename”: search for file/dir in all folders starting from root
 find . -iname “TODO”: search for file/dir case sensitively in current and sub folders
 find . -type d -name "my_project”: search for directory using type d can use f for file
 chmod -R 777 <directory>: full permission(4+2+1) to directory recursively
 pwd: print current path
 whoami: print current user

Git
git init
git add -a
git commit -m 'commit message'
git branch -a
git branch <branch name>
git checkout <branch name>
git checkout -b <branch name>
git pull
git fetch
git merge <parent branch> <branch for merge>
git stash
git stash pop
git push -d <remote_name> <branchname>
git branch -D <branch_name>
git branch -m <oldname> <newname>
git diff <file1><file2>
git pull origin main
git fetch upstream main
git rebase upstream/main ->git push -f origin branch-name
git cherry-pick <commit-hash-1> <commit-hash-2>
git grep -iF ‘deleted-class-name’
git fetch upstream pull/Pull-Id/head:BRANCH
git remote -v
git remote add upstream URL
git remote set-url origin URL
git bisect

PHP & Laravel
php -v
php filename.php
composer create-project laravel/laravel="7.0.*" laravel7
composer require laravel/ui
composer require brianium/paratest --dev
php artisan ui bootstrap --auth
php artisan key:generate
php artisan cache:clear 
php artisan route:clear
php artisan config:cache 
php artisan route:list
php artisan migrate
php artisan migrate:rollback --step=1
php artisan db:seed --class=ProductTableSeeder
php artisan make:model Settings --migration
php artisan make:controller UserController --resource
php artisan make:controller Api/UserController --api
php artisan make:provider MyCustomServiceProvider
php artisan make:resource UserResource/UserCollection
php artisan make:observer ProductObserver --model=Product
php artisan make:migration AddColumnIsMessageToDocumentsTable
php artisan make:seeder UserSeeder
php artisan make:notification InvoicePaid
php artisan make:command RegisteredUsers --command=registered:users
php artisan view:clear 
php artisan demo:command
php artisan db:seed --class=RolesAndPermissionsSeeder
php artisan test
php artisan test tests/Unit/OrderServiceTest.php


JS & TS & React & Vue
node -v
tsc filename.ts
npx create-react-project  PROJECT-NAME
npm create vite@latest
npm audit fix --force
npm cache clean --force
npm update
npm start
npm run serve
npm run dev
npm run lint -- --fix
npm install eslint eslint-plugin-react eslint-plugin-react-hooks --save-dev
npm test ; run test for all files in react
npm test -- src/components/Greeting.test.tsx # react test
npm test -- --coverage
npm run test ; run test for all files in vue
npm run test src/components/__tests__/HelloWorld.test.ts # vue test



Python & Django
python3 -V
python3 filename.py
python3.12 -m pip install django
python3 -m venv env
source env/bin/activate
pip3 install -r requirements.txt
pip install django psycopg2-binary: install custom packages
pip freeze > requirement.txt: generating requirement.txt
django-admin startproject myapp
python manage.py startapp api
python manage.py runserver
pytest api/tests/test_utils.py
python -m unittest tests/test_calculator.py
python manage.py createsuperuser
python manage.py makemigrations: creating migrations for changes
python manage.py migrate: rolling out changes to db
python manage.py migrate <app_name> <prev_migration_name>: rolling back to prev migration
python manage.py show_urls
python3 manage.py test catalog.tests.test_models.YourTestClass.test_one_plus_one_equals_two
deactivate

Dart & Flutter
dart --version
dart filename.dart
dart create -t package <PACKAGE_NAME>
flutter doctor
flutter create project-name
emulator -list-avds
emulator -avd Pixel_3a_API_34_extension_level_7_x86_64
flutter devices
flutter run 
flutter run -d Pixel_3a_API_34_extension_level_7_x86_64
flutter test path_your_test_file.dart

Go & Gin
go mod init github.com/manumuralivakkel/project 
go mod tidy
go run main.go
go get -u github.com/gin-gonic/gin

Docker
nano ~/.zshrc
export PATH="/Applications/Docker.app/Contents/Resources/bin:$PATH"
source ~/.zshrc
docker build -t <TAG-NAME> .
docker images
docker run -d TAGNAME :- run in detach mode
docker pull IMAGE_FROM_HUB
docker build -t django-docker:latest .
docker ps
docker image rm image-name
docker exec -it CONTAINER_NAME bash  :- will go to that container shell
docker volume ls :- list volumes
docker network ls  :- list networks
docker stats  :- show container status
docker-compose —version
docker compose up --build -d
docker compose down
docker compose log
docker stop $(docker ps -q) :- stop all containers
docker rm $(docker ps -aq) :- remove all containers
docker rmi $(docker images -q) :- remove all images
docker compose logs -f
docker compose exec app bash
docker run --rm -v $(pwd):/app -w /app composer install
docker compose exec app chown -R www-data:www-data /var/www/html/storage

Linux
whoami
echo $0
sudo apt-get update
sudo apt-get upgrade
sudo install package name
pwd

Mac
pwd: current path
echo $SHELL
nano ~/.zshrc or zsh
export ANDROID_SDK_ROOT=$HOME/Library/Android/sdk
source ~/.zshrc or zsh
sudo /Applications/XAMPP/xamppfiles/xampp restart
redis-cli -h 127.0.0.1 -p 6379
brew services list
brew services start mysql/postgresql/redis
brew services restart mysql/postgresql/redis
brew services stop mysql/postgresql/redis
brew services info mysql/postgresql/redis
redis-server # start redis in current console
redis-cli #open the Redis command-line interface
127.0.0.1:6379> PING
127.0.0.1:6379> SELECT 1
127.0.0.1:6379[1]> GET your_key_name
mysql -u root -p
