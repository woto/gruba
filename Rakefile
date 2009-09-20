require 'rubygems'
require 'rake'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "gruba"
    gem.summary = %Q{Best grabber DSL}
    gem.description = %Q{Best grabber DSL}
    gem.email = "ceo@prepor.ru"
    gem.authors = ["Andrew Rudenko"]
    gem.add_development_dependency "rspec"
    gem.add_development_dependency "yard"
    
    gem.add_dependency "nokogiri"
    gem.add_dependency "mechanize"
    gem.add_dependency "nokogiri"
    gem.add_dependency "xmpp4r-simple"
    
    # gem is a Gem::Specification... see http://www.rubygems.org/read/chapter/20 for additional settings
  end
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: sudo gem install jeweler"
end

require 'spec/rake/spectask'
Spec::Rake::SpecTask.new(:spec) do |spec|
  spec.libs << 'lib' << 'spec'
  spec.spec_files = FileList['spec/**/*_spec.rb']
end

Spec::Rake::SpecTask.new(:rcov) do |spec|
  spec.libs << 'lib' << 'spec'
  spec.pattern = 'spec/**/*_spec.rb'
  spec.rcov = true
end

task :spec => :check_dependencies

task :default => :spec

begin
  require 'yard'
  YARD::Rake::YardocTask.new
rescue LoadError
  task :yardoc do
    abort "YARD is not available. In order to run yardoc, you must: sudo gem install yard"
  end
end
