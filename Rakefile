# pre-flight
require 'bundler/setup'

require 'rspec/core/rake_task'
require 'rubocop/rake_task'
require 'yard'

RSpec::Core::RakeTask.new(:spec)
RuboCop::RakeTask.new(:rubocop)
YARD::Rake::YardocTask.new(:yard)

task default: [:test]

desc 'Run all build/tests commands (CI entry point)'
task test: [:rubocop, :spec, :yard]

desc 'Generate all documentations'
task doc: [:yard]
