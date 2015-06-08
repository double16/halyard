# This file manages Puppet module dependencies.

# Shortcut for a module from halyard organization
def github(name, *args)
  options ||= args.last.is_a?(Hash) ? args.last : {}

  if path = options.delete(:path)
    mod name, :path => path
  else
    version = args.first
    options[:repo] ||= "halyard/puppet-#{name}"
    mod name, version, :github_tarball => options[:repo]
  end
end

github 'stdlib', '4.3.2', :repo => 'puppetlabs/puppetlabs-stdlib'
github 'boxen', '3.11.0.akerl27'
github 'homebrew', '1.13.0'
github 'repository', '2.4.1'
#github 'git', '2.7.9.akerl1'
mod 'git', :path => '/Users/akerl/boxen-tmp/puppet-git'
github 'sudoers', '0.1.1.akerl8'
github 'hostname', '0.0.4'
#github 'dotfiles', '0.0.11'
mod 'dotfiles', :path => '/Users/akerl/boxen-tmp/puppet-dotfiles'

