# Snap Share

Snap Share is a simple WordPress sharing plugin that offers a clean and modern way to share your posts to social media.

If you are not a developer, please use the [Snap Share WordPress Plugin Page](https://wordpress.org/plugins/snap-share/) on WordPress.org.

## Filters
Snap Share includes some helpful filters to extend Snap Share.

To add more post types to Snap Share, please use the following function:
```
function themeprefix_snapshare_post_types( $post_types ) {
  /**
   * Add all applicable post types to the
   * $post_types array
   */
  $post_types = array( 'post', 'page' );

  return $post_types;
}
add_filter( 'snapshare_post_types', 'themeprefix_snapshare_post_types' );
```

If you want to dequeue Font Awesome because you may already have it enqueued, you can do so with the following function:
```
function themeprefix_snapshare_remove_fontawesome( $enable_fontawesome ) {
  $enable_fontawesome = false;

  return $enable_fontawesome;
}
add_filter( 'snapshare_enable_fontawesome', 'themeprefix_snapshare_remove_fontawesome' );
```

## Versioning
Sanp Share is maintained under the [Semantic Versioning guidelines](http://semver.org/).

## Created By
Blake Wilson
* http://blakewilson.me
* https://twitter.com/blakewilsonme

## License
Snap Share code released under the GPLv2 or later.
