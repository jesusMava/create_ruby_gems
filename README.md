# How to create a Gem in Ruby
## Getting Started
first all, we'll do it in linux OS and use us bundle. 

you should install [rbenv](https://github.com/rbenv/rbenv) for to work with ruby, for this example use the ruby version 2.6.3 
open your console and type 

> $ **ruby -v**  
    # => 2.6.3

next, we need to install bundle
> $ **gem install bundle** 

we check that it is install with 
> $ **bundle -v**  
    #=> Bundler version 2.0.2

## Create your gem
next step, we need to select a name for our gem, you can follow the [basic recomendations](https://guides.rubygems.org/patterns/#consistent-naming) to do it, and for create the gem is very easy, just type.

> $ **bundle gem name-your-gem **


there is some thing that you should answer before to create your gem, 

> $ Do you want to generate tests with your gem? rspec   
  $ Do you want to license your code permissively under the MIT license? y   
  $ Do you want to include a code of conduct in gems you generate? y

## Setting up .Gemspec  
and it is all. you have a gem but you need to configure the file **.gemspec**

>  spec.name          = "name-your-gem"  
   spec.authors       = ["your name"]  
   spec.email         = ["your email example@gmail.com"]         
   spec.summary       = "Summary"   
   spec.description   = "description"   
   spec.homepage      = "your repo in github"     
   spec.license       = "MIT"        
   spec.metadata["source_code_uri"] = "your github"   
   spec.metadata["changelog_uri"] = "your github"  

## Finally

you principal code you should put in *lib/name-your-gem.rb*

and you proof *TDD* should put it in spec/name-your-gem.spec

finally you can do your gem exec with

> $ **gem build name-your-gem.gemspec**

## RubyGems
to post your gem in [RubyGems](https://rubygems.org/) 

> $ **gem push name-your-gem.gem**


