# qc.CacheAsBitmap

## Description
Enhance rendering efficiency, especially in the canvas mode. This component will cache the node to a picture, then each time take the picture for rendering directly.
This logical component can only cache a single self node, and it can also cache all child nodes.

Note that when the content changes, you need to set the dirty property to flush the cache.

## Variables
| Variable Name     |   Type     |  Description        |
| ------------- |-------------|-------------|
| cacheType | int | The cache type, there are two possible values: CacheAsBitmap.CACHE_FOR_SCREEN, CacheAsBitmap.CACHE_FOR_SELF |
| boundsType | int | The bound type, there are two possible values: CacheAsBitmap.BOUNDS_SELF(only cache self)、CacheAsBitmap.BOUNDS_ALL(cache self and child) |
| boundsInScreen | boolean | Whether to limit the size of the cache, false by default |
| dirty | boolean | Whether need to refresh cache |

## Manual
[CacheAsBitmap](http://docs.qiciengine.com/manual/BuildinComponents/CacheAsBitmap.html)