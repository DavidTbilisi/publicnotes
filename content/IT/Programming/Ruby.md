## Resources

https://rubyrush.ru/steps
https://www.geeksforgeeks.org/ruby/ruby-programming-language/
https://www.theodinproject.com/paths/full-stack-ruby-on-rails/courses/ruby
https://ruby-for-beginners.rubymonstas.org/
https://thoughtbot.com/upcase/rails


## Rake 
Artisan commands (Laravel’s `php artisan migrate`)

Think of **Rake** as Ruby’s version of `make` — a _task runner_.  
You define little scripts (called “tasks”) inside a `Rakefile`.  
Example:

`task :hello do   puts "Hello, world!" end`

Then run it with `rake hello`.  
Rails itself uses Rake under the hood for many commands — like `rake db:migrate`.

---
## Bundler
Composer

**Bundler** is Ruby’s dependency manager — same idea as `composer` for PHP or `pip` + `requirements.txt` for Python.  
It reads your `Gemfile` and installs all gems (libraries) with compatible versions, then locks them in `Gemfile.lock`.  
You usually run it as:

`bundle install bundle exec rails server`

`bundle exec` ensures you’re using the gems from _this project’s environment_, not globally installed ones.


---
## Rails
