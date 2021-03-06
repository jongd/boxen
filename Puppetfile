# This file manages Puppet module dependencies.
#
# It works a lot like Bundler. We provide some core modules by
# default. This ensures at least the ability to construct a basic
# environment.

def github(name, version, options = nil)
  options ||= {}
  options[:repo] ||= "boxen/puppet-#{name}"
  mod name, version, :github_tarball => options[:repo]
end
# Shortcut for a module from GitHub's boxen organization
def github(name, *args)
  options ||= if args.last.is_a? Hash
    args.last
  else
    {}
  end

  if path = options.delete(:path)
    mod name, :path => path
  else
    version = args.first
    options[:repo] ||= "boxen/puppet-#{name}"
    mod name, version, :github_tarball => options[:repo]
  end
end

# Core modules for a basic development environment. You can replace
# some/most of those if you want, but it's not recommended.

# Includes many of our custom types and providers, as well as global
# config. Required.

github "boxen", "3.0.2"

# Core modules for a basic development environment. You can replace
# some/most of these if you want, but it's not recommended.

github "dnsmasq",  "1.0.0"
github "gcc",      "1.0.0"
github "git",      "1.0.0"
github "homebrew", "1.9.0"
github "hub",      "1.0.0"
github "inifile",  "0.9.0", :repo => "cprice-puppet/puppetlabs-inifile"
github "nginx",    "1.0.0"
github "nodejs",   "2.0.0"
github "ruby",     "1.0.0"
github "stdlib",   "3.0.0", :repo => "puppetlabs/puppetlabs-stdlib"
github "sudo",     "1.0.0"

# Optional/custom modules. There are tons available at
# https://github.com/boxen.

github "imagemagick", "1.1.0"
github "xquartz", "1.0.0"
github "redis", "1.0.0"
github "notational_velocity",  "1.0.0"
github "dropbox",  "1.0.0"
github "onepassword",  "1.0.0"
github "chrome",  "1.0.0"
github "mongodb",  "1.0.0"
github "sublime_text_2",  "1.0.0"
github "spotify",  "1.0.0"
github "macvim",  "1.0.0"
github "iterm2",  "1.0.0"
github "heroku",  "1.0.0"
github "sysctl", "1.0.0"
github "rbenv",  "1.0.0"
github "zsh",  "1.0.0"
github "osx", "1.0.0"
github "divvy", "1.0.0"
github "repository", "2.0.2"
