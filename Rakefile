# frozen_string_literal: true

require 'bundler/gem_tasks'
require 'os'
require 'rspec/core/rake_task'
require 'rubocop/rake_task'
require 'yard'

task default: OS.linux? ? %i[rubocop spec] : %i[spec]

RuboCop::RakeTask.new(:rubocop) do |task|
  task.patterns = ['lib/**/*.rb', 'spec/**/*.rb']
end

RSpec::Core::RakeTask.new(:spec)

YARD::Rake::YardocTask.new(:doc) do |t|
  t.files = ['lib/**/*.rb']
  t.stats_options = ['--list-undoc']
end
