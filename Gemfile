source "https://rubygems.org"
# こんにちは！ここでJekyllのバージョンを管理します。
# 別のバージョンを使いたい場合は、以下のように変更してファイルを保存し、 `bundle install` を実行してください。

# これで適切なバージョンのJekyllが動作していることを確認できます。
# Happy Jekylling!
# gem "jekyll", "~> 4.3.3"

# これは新しいJekyllサイトのデフォルトテーマです。お好きなものに変更してください。
gem "minima", "~> 2.5"
# GitHub Pagesを使いたい場合は、上の「gem "jekyll"」を削除し、下の行のコメントを外します。アップグレードするには、`bundle update github-pages` を実行してください。
gem "github-pages", "~> 231", group: :jekyll_plugins
# If you have any plugins, put them here!
group :jekyll_plugins do
  gem 'jekyll-sitemap'
  gem 'jekyll-feed'
  gem 'jekyll-seo-tag'
end

# WindowsとJRubyはzoneinfoファイルを含まないので、tzinfo-data gemと関連ライブラリをバンドルする。
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]

# Lock `http_parser.rb` gem to `v0.6.x` on JRuby builds since newer versions of the gem do not have a Java counterpart.
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]

gem "webrick", "~> 1.8"
