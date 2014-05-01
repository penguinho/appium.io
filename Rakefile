require_relative 'rake_lib/helper.rb'

# clone from forks for now
desc 'Update appium docs, readme, and intro'
task :appium do
  h = AppiumIo::Helper.new
  h.update_docs
  h.update_readme
  h.update_intro
end

desc 'Publish changes to github'
task :publish => :appium do
  sh 'git add --all .'
  sh 'git commit -am "Update appium.io"'
  sh 'git push origin gh-pages'
end

task :default => :appium

# jekyll serve -- run local gh pages server