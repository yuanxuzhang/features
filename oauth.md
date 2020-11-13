1. 为什么要client_id和client_secret分两步（或者说，要是用授权码）？  
授权页面是重定向的，重定向只支持GET方式[redirect works: it sends the URL to the browser, and the browser then resubmits it to the destination site.](https://stackoverflow.com/questions/7028730/redirect-to-another-site-using-post-method-with-parameters-in-stripes)
为避免client_secret暴露  
