require 'rake'

#------------------------------------------------------------------------------
#  
#  Config
#  
#------------------------------------------------------------------------------

# The directory of the target project's public assets
target = ENV["TARGET_DIR"] || "../../rails/public"

# The directory (under target) where stylesheets are stored
css_dir = ENV["CSS_DIR"] || "stylesheets"


#------------------------------------------------------------------------------
#  
#  Tasks
#  
#------------------------------------------------------------------------------

desc """Remove all compiled assets."""
task :clean do
  puts "CLEANING STYLESHEETS >>"
  system("rm -rf #{target}/#{css_dir}/silverforge/*")
  system("rm -rf #{target}/#{css_dir}/silverlib/*")
  puts "--"
end

desc """Builds HTML/CSS using Compass."""
task :default => [:silverlib, :silverforge]


desc """Builds Silverforge SASS using Compass."""
task :silverforge do
  puts "COMPILING SILVERFORGE SASS TO CSS >>"
  system("COMPASS_TARGET=\"#{target}\" compass compile silverforge")
  puts "--"
end
