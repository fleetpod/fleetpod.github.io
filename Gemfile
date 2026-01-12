source "https://rubygems.org"

# Hello! This is where you manage which Jekyll version is used to run.
# When you want to use a different version, change it below!
# We use a specific version to avoid breaking changes.
gem "jekyll", "~> 4.3.0"

# This is the default theme for new Jekyll sites.
# You may want to change this to something like minima or another theme.
# gem "minima", "~> 2.5"

# If you want to use GitHub Pages, remove the "gem "jekyll"" above and
# uncomment the line below. To upgrade, run `bundle update github-pages`.
gem "github-pages", group: :jekyll_plugins

# Plugins
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
  gem "jekyll-seo-tag", "~> 2.6"
end

# Windows and JRuby compatibility
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
  gem "wdm", "~> 0.1.1", :install_if => Gem.win_platform?
end

# Performance booster for watching directories on Windows
gem "wdm", "~> 0.1.1", :install_if => Gem.win_platform?
