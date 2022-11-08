Savvy is a powerful but lightweight object-oriented template system for PHP.

Unlike other template systems, Savvy by default does not compile your
templates into PHP; instead, it uses PHP itself as its template language so you
don't need to learn a new markup system.


## Note 2022
For php 8.1 we swapped using Brett's packge to this repo. We did this so we can more easily update and maintain the package. 

### Update to composer.json
- First we added the repo to the "repositories" section in the json file 
```{
			"type":"package",
			"package": {
				"name": "tommyneu/savvy",
				"version": "master",
				"source": {
					"url": "https://github.com/tommyneu/Savvy.git",
					"type": "git",
					"reference": "master"
				}
			}
		}
 ```
 - We then changed `"saltybeagle/savvy": "#.#",` to `"tommyneu/savvy": "dev-master",` so we always pull from the master branch
 - We also need to add `"Savvy": "vendor/tommyneu/savvy/src"` in the psr-0 section of the the autoload so that Savvy's namespace is used correctly
 - After all the changes are made we may need to clear the cache and re-install `composer clear-cache && composer install`

[Brett's Package](https://packagist.org/packages/saltybeagle/savvy)
