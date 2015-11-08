Start

\curl -L https://get.rvm.io | bash -s stable --ruby
rvm install ruby-2.2.3

gem install rails --version 4.2.4 --no-ri --no-rdoc

xcode-select --install
-- 
bundle install
screencast: http:rubyonrails.org/screencasts/rails3
http://gembundler.com
gem install bundler
--
run app:
	rails server or rails s

New App
    rails new <appName>
generators:
	rails generate [generator] or rails g

	generators:
		helper
		mailer
		migration
			to run migration files: rake db:migrate
		model
		scaffold
			rails g scaffold zombie name:string bio:text age:integer

console
	rails console: to debug our app
