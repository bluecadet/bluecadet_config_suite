


 *  Need to attach media library to new view, and disable the `media_entity_browser` view.

```
/**
 * Implements hook_preprocess_views_view().
 */
function HOOK_preprocess_views_view(&$variables) {
  if ($variables['view']->id() === 'media_entity_browser_custom') {
    $variables['view_array']['#attached']['library'][] = 'media_entity_browser/view';
  }
}
```