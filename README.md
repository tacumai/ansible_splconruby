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
$ rails s
# or
$ rake unicorn:start
```
