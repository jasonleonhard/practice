<h1 align="center">Geminate!</h1>

<p align="center">
<!--   <img src="https://pixabay.com/static/uploads/photo/2016/03/29/22/08/love-1289532_1280.png" height="450x450"> -->

  <img src="https://pixabay.com/static/uploads/photo/2016/03/29/22/08/love-1289532_1280.png" height="350x350">
</p>

<h1>The gem I made to teach you how to build your own gems</h1>

    Geminate:

    verb (used with or without object), geminated, geminating.
    1. to make or become doubled or paired.

    adjective
    2. Also, geminated. combined or arranged in pairs; twin; coupled.

___

### Fork this repository by clicking 'fork' button

### Or clone with ssh

    git clone git@github.com:jasonleonhard/geminate.git

### Or clone with https

    git clone https://github.com/jasonleonhard/geminate.git


### Navigate into the repo

    cd geminate

### Create a new git branch and switch to it

    git checkout -b 0.0.0

___


## You will not want your gem to be named "geminate", that is mine, so do the following

1. Rename your repo and folder

2. Change all of the files named "geminate" to what your gem will be called

3. When you see the word "geminate" anywhere, for the rest of this guide, I will assume you have/will change the name to match your intented new gem name

___

### Look at the following files in the repo

#### lib/geminate.rb

    class geminate
      def self.how
        puts "Geminate: the gem I made to teach you how to build your own gems!"
        puts "Learn how at: https://github.com/jasonleonhard/geminate"
      end
    end

The above file holds the class methods you are creating for others to use, when they use your gem later, feel free to modify the method name and what it does before we continue

#### geminate.gemspec

    Gem::Specification.new do |s|
      s.name        = 'geminate'
      s.authors     = ["jasonleonhard"]
      s.email       = ['devbrights@gmail.com']
      s.files       = ["lib/geminate.rb"]
      s.summary     = "Geminate: 1. to double or repeat 2. to make or become doubled or paired."
      s.description = "Geminate the gem I made to teach you how to make your own gems!"
      s.homepage    = 'http://rubygems.org/gems/geminate'
      s.license     = 'MIT'
      s.version     = '0.0.0'
    end

#### Change all of the following:

1. name, authors, email, summary, description, homepage, files

2. Consider if you want to release your gem under an MIT or GPL licence

3. Make certain your version is 0.0.0 the first time you are creating a gem

___

#### When you are satisified with all of your changes....

    git add .
    git commit -am "version 0.0.0 ready"
    git push 0.0.0
    git checkout master
    git merge 0.0.0

#### Create an account at:

[https://rubygems.org/api/v1/api_key.yaml](https://rubygems.org/api/v1/api_key.yaml)

#### Sign in with your username and password

Save the yaml file into: ~/.gem/

#### On any Nix system (UNiX/LINUX):

    mv ~/Downloads/api_key.yaml ~/.gem/api_key.yaml

___

## To find your API key

[https://rubygems.org/profile/edit](https://rubygems.org/profile/edit)

#### Look for the words:

Your API key is

#### If you do not see a API key on that page

You will want to run the curl command they suggest to create a ~/.gem/credentials

___

## PUBLISH WITH:

    gem push geminate-0.0.0.gem

enter your username

enter your password

#### List your gem:

    gem list -r geminate

# Congratulations! You have just created and publicly pushed your first version of a ruby gem!

___

### Warning: To change any gem you own, after it has been uploaded to rubygems, you must version it

#### geminate.gemspec

    Gem::Specification.new do |s|
      s.name        = 'geminate'
      s.authors     = ["jasonleonhard"]
      s.email       = ['devbrights@gmail.com']
      s.files       = ["lib/geminate.rb"]
      s.summary     = "geminate!"
      s.description = "Geminate the gem I made to teach you how to make your own gems!"
      s.homepage    = 'http://rubygems.org/gems/geminate'
      s.license     = 'MIT'
      s.version     = '0.0.1' # notice this version increased from 0.0.0
    end

#### Every new version must increase, to create what you will be giving to rubygems:

    gem build geminate.gemspec

[//]: # (Successfully built RubyGem)
[//]: # (Name: geminate)
[//]: # ( `Version: 0.0.1`)
[//]: # ( File: geminate-0.0.1.gem)

#### View this new file with

    ls -G -latrh

#### You should now see something like this

[//]: # (geminate-0.0.1.gem)

#### You have only created the file, you need to give it to rubygems now

    gem push geminate-0.0.1.gem

#### Cool, now you have, go to your url that should be similar to this

[https://rubygems.org/gems/geminate](https://rubygems.org/gems/geminate)

#### Your new version of the gem should be listed and if so you have sucessfully updated you gem

___

# What about using the gem?

#### First install it by the version you want

    gem install ./geminate-0.0.1.gem

#### Or install the latest version

    gem install geminate

#### Verify you have it installed now

    gem list -r geminate

#### Start pry or irb

    pry

#### or

    irb

#### Require your new gem library

    require 'geminate'

## And now for the moment we have all been waiting for, you can use your gems class method

    Geminate.how

[//]: # (Geminate: the gem I made to teach you how to build your own gems!)
[//]: # (Learn how at: https://github.com/un5t0ppab13/geminate)

#### List all method you defined in your Class (aka gem)

    Geminate.methods(false)

___

### If you need further help view the guides here

[http://guides.rubygems.org/rubygems-org-api/](http://guides.rubygems.org/rubygems-org-api/)

___

## If you've enjoyed building your own gem why not give us a star!?!?
# Thank you.
