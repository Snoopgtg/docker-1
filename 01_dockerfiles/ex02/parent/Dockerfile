FROM ruby:2.5
EXPOSE 3000

#Install library dependencies
RUN gem install sqlite3 rails \
	&& curl -sL https://deb.nodesource.com/setup_11.x | bash - && apt-get install -y nodejs

ONBUILD WORKDIR ./opt/app/
#folder with app will be in root where child Dockerfile 
ONBUILD COPY app .
ONBUILD RUN bundle install
ONBUILD RUN rake db:migrate
ONBUILD RUN rake db:setup

#docker build -t ft-rails:on-build ./pathToParentDockerfile/
#docker build -t child ./pathToChildDockerfile/
#docker run -d --name myrails -p 3000:3000 child:latest
#http://192.168.99.100:3000/ - index page
#http://192.168.99.100:3000/articles/new - form for creating article
#http://192.168.99.100:3000/articles - list of all created articles