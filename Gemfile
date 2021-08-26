# Managed by modulesync - DO NOT EDIT
# https://voxpupuli.org/docs/updating-files-managed-with-modulesync/

source ENV['GEM_SOURCE'] || "https://rubygems.org"

# as a test, pull in gettext-setup from master
# it allows newer fast_gettext versions
gem 'gettext-setup', git: 'https://github.com/puppetlabs/gettext-setup-gem', branch: 'master', require: false

group :test do
  gem 'voxpupuli-test', '~> 2.5',   :require => false
  gem 'coveralls',                  :require => false
  gem 'simplecov-console',          :require => false
  gem 'puppet_metadata', '~> 1.0',  :require => false
  gem 'puppet-lint-param-docs',     :require => false
end

group :development do
  gem 'guard-rake',               :require => false
  gem 'overcommit', '>= 0.39.1',  :require => false
end

group :system_tests do
  gem 'voxpupuli-acceptance', '~> 1.0',  :require => false
end

group :release do
  gem 'github_changelog_generator', '>= 1.16.1',  :require => false if RUBY_VERSION >= '2.5'
  gem 'voxpupuli-release', '>= 1.0.2',            :require => false
  gem 'puppet-strings', '>= 2.2',                 :require => false
end

gem 'rake', :require => false
gem 'facter', ENV['FACTER_GEM_VERSION'], :require => false, :groups => [:test]

puppetversion = ENV['PUPPET_VERSION'] || '>= 6.0'
gem 'puppet', puppetversion, :require => false, :groups => [:test]

# vim: syntax=ruby
