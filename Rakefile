# From: https://github.com/ainc/awesomeinc2013/blob/master/Rakefile 

require "rubygems"
require "tmpdir"

require "bundler/setup"
require "jekyll"

# ENV["JEKYLL_ENV"] = "production"

# desc "Generate blog files"
# task :generate do
#   Jekyll::Site.new(Jekyll.configuration({
#     "source"      => ".",
#     "destination" => "_site"
#   })).process
# end


# desc "Generate and publish blog to gh-pages"
# task :publish => [:generate] do
#   Dir.mktmpdir do |tmp|
#     cp_r "_site/.", tmp

#     pwd = Dir.pwd
#     Dir.chdir tmp

#     system "git init"
#     system "git add ."
#     message = "Site updated at #{Time.now.utc}"
#     system "git commit -m #{message.inspect}"
#     system "git remote add origin git@github.com:AddisonHowe/addisonhowe.github.io.git"
#     system "git push origin main --force"

#     Dir.chdir pwd
#   end
# end


desc "Build and push to main branch"
task :publish do 
  system "git checkout main"
  system "JEKYLL_ENV=production bundle exec jekyll build"  
  system "git checkout deploy-branch"
  system "cp -r _site/* . && rm -rf _site/ && touch .nojekyll"
  system "git add ."
  message = "Site updated at #{Time.now.utc}"
  system "git commit -m #{message.inspect}"
  system "git push"
  system "git checkout main"
end


desc "Preview changes"
task :preview do 
  system "bundle exec jekyll serve"  
end


