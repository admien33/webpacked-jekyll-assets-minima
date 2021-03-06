## introduction :

- Exploratory works on Webpack with Jekyll-assets

- see intro jeykll-webpack [https://github.com/allizad/jekyll-webpack](https://github.com/allizad/jekyll-webpack)

- Why ? Jekyll-assets is great! But when enabling the options to compress css/js, with added gems as uglifier, autoprefixer, build time is multiplied by 2/3, depending configuration. Webpack can do the job. Then end-users just edit the content, with faster build time.

- Next step, with React components and custom page assets, project [webpacked-jekyll-assets-react](https://github.com/admien33/webpacked-jekyll-assets-react)


### Webpack_assets put on Jekyll src

first step : generate _site_assets_config repo with config_assets json files (export info from data/templates)

```bash
bundle exec jekyll build --config _config_assets.yml
```

second step : build with webpack. Optimized assets are placed on : src/_assets/css_wp and /src/assets/dist (js, fonts, images)

```bash
npm install
npm run build-wp /serve-wp
```

todo : 
	
	- add hash on assets js + list hashed filenames used during jekyll build



### Then, build jekyll site with plugin jekyll-assets and no compress options

```bash
bundle exec jekyll build / serve
```


### demo :

- [webpacked-jekyll-assets-minima](https://d2m.tech/webpacked-jekyll-assets-minima/)





#### Note  :

- see Gemfile, config temp :  plugin Jekyll-assets from master, fixed with jekyll 3.5,20170721

- font-awesome asset, adapt @font-face src url : '../font/fontawesome-webfont.eot?v=4.7.0' -> 'fontawesome-webfont.eot?v=4.7.0'



