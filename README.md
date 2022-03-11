# Site Attributes + Site Stream Demo

### Links:
* [Site Entity in Knowledge Graph](https://www.yext.com/s/3521131/entity/edit3?entityIds=27957663)
* [Deploys Page](https://www.yext.com/s/3521131/yextsites/26614/branch/806/deploys/recent)

## Implementation
This branch leverages the new **site stream** feature. Refer to [sites-config/site-stream.json](https://github.com/lymarrie/sites-products-starter/blob/site-attributes/sites-config/site-stream.json), in which my site stream is defined. This stream requests for the following fields from my [site entity](https://www.yext.com/s/3521131/entity/edit3?entityIds=27957663):
* name
* c_header
* c_footer
* c_enableConversionTracking
* c_googleAnalytics

The site entity data is then nested under a **__site_** object, and appended to all other Stream documents. This can be observed by inspecting any sample document in your **_localData_/** directory.

From there, I can reference this data like I would any other field reference.
* Refer to the [navigation bar partial](https://github.com/lymarrie/sites-products-starter/blob/site-attributes/partials/nav.hbs#L11) to see how the header links are listed out.
* Here's an example of the site entity name reference on my [index page](https://github.com/lymarrie/sites-products-starter/blob/site-attributes/templates/home.hbs#L21)

The finished result [can be observed here](https://m6a74lmzm3-26614-d.preview.pagescdn.com/) - all information highlighted in _yellow_ is powered by the site-stream!

![](https://media.giphy.com/media/b8RfbQFaOs1rO10ren/giphy.gif)
