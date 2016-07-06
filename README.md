# Rails app for Scraping
会員連携用スクレイピングApp向け vagrant-box

## vagrant

### required

* vagrant
* virtualbox

```sh
# mountするためにplugin必須
$ vagrant plugin install vagrant-vbguest
# up
$ vagrant up
```
## app(rails本体)
以下の作業は `vagrant ssh` 後行う

### Rails

```sh
$ rails new app
$ rails s -b 0.0.0.0
```

なお、railsが正常に立ち上がらず

```sh
There was an error while trying to load the gem 'uglifier'.
````

とでる場合は、Gemfile内の

```sh
gem 'therubyracer', platforms: :ruby`
```

のコメントアウトを外して`bundle install掛け直してみてください。
