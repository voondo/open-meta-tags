require 'rake'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "open-meta-tags"
    gem.summary = %Q{A}
    gem.description = %Q{something}
    gem.email = "jonathan@intridea.com"
    gem.homepage = "http://github.com/jonathannelson/open-meta"
    gem.authors = ["Intridea"]
    gem.add_development_dependency "thoughtbot-shoulda", ">= 0"
    # gem is a Gem::Specification... see http://www.rubygems.org/read/chapter/20 for additional settings
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: gem install jeweler"
end

begin
  require 'spec/rake/spectask'

  desc 'Default: run specs'
  task :default => :spec

  desc 'Test the sphinx plugin'
  Spec::Rake::SpecTask.new do |t|
    t.libs << 'lib'
    t.pattern = 'spec/*_spec.rb'
    t.verbose = true
    t.spec_opts = ['-cfs']
  end
rescue LoadError
  puts 'RSpec not available. Install it with: sudo gem install rspec'
end

begin
  require 'yard'
  YARD::Rake::YardocTask.new(:yard) do |t|
    t.options = ['--title', 'MetaTags Documentation']
    if ENV['PRIVATE']
      t.options.concat ['--protected', '--private']
    else
      t.options.concat ['--protected', '--no-private']
    end
  end
rescue LoadError
  puts 'Yard not available. Install it with: sudo gem install yard'
end