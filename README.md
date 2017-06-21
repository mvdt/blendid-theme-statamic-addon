# blendid-theme-statamic-addon
[Statamic v2](https://statamic.com/) addon for configuring `rev-manifest.json` name/location. Ideal when using [Blendid](https://github.com/vigetlabs/blendid)

Blendid is super fast at compiling ES6 and SASS. It's also super easy to set up. However, Blendid's default location for outputting it's `rev-manifest.json` is not compatible with [Statamic's `theme` tag](https://docs.statamic.com/tags/theme-js). Statamic looks for a `rev-manifest.json` in `/site/themes/[mytheme]/build/` where [our Blendid setup](https://github.com/classyllama/blendid-theme-statamic-addon/wiki/Our-Blendid-setup-for-a-Statamic-project) puts the rev-manifest in the theme folder. 

## It's configurable

This Statamic addon allows you to configure the filepath (relative the the statamic theme) and the filename of your generated `rev-manifest.json`. So, in theory, this can be used without needing to use Blendid at all—if you just need to edit the name and/or location of your manifest file. 

### Defaults made for [Blendid](https://github.com/vigetlabs/blendid)

The default settings are set for Blendid, so that's why it's a "Blendid theme" addon. But you're more than welcome to use it for _any_ setup you need to configure a manifest file location/name!

## How to install

1. Download the source
2. Rename the folder you downloaded `BlendidTheme`
3. Add it to your Statamic addon directory at `/site/addons/`
4. Update addons by running `php please update:addons`
5. Done!

## How to use

`{{ blendid_theme }}` has all the exact same functionality as Statamic's `{{ theme }}` tag, except it will use the settings you set in **Control Panel > Addons > Blendid Theme > Settings** to look for a manifest file when you use the `version` param like this: `<script src="{{ blendid_theme:js version="true" }}"></script>`.

Check out [how we set up Blendid](https://github.com/classyllama/blendid-theme-statamic-addon/wiki/Our-Blendid-setup-for-a-Statamic-project) for a Statamic project.

## License

See the [LICENSE](https://github.com/classyllama/blendid-theme-statamic-addon/blob/master/LICENSE) file for license rights and limitations (MIT).
