# URLs

## Name:

### URLs (WIP)

## Overall logic

- Home page `https://alpha.austin.gov/`
- Topic collection page `https://alpha.austin.gov/(THEME_SLUG)/(TOPIC_COLLECTION_SLUG)` or `https://alpha.austin.gov/(THEME_SLUG)/(TOPIC_COLLECTION_SLUG)/(TOPIC_COLLECTION_SLUG)` (our current (Joplin 2) data structure supports an unlimited chain of topic collections)
- Topic page `https://alpha.austin.gov/(THEME_SLUG)/(TOPIC_COLLECTION_SLUG)/(TOPIC_SLUG)` (see topic collections for how this gets more complicated)
- Department page `https://alpha.austin.gov/(DEPARTMENT_SLUG)/`
- Service/Info/Guide page `https://alpha.austin.gov/(THEME_SLUG)/(TOPIC_COLLECTION_SLUG)/(TOPIC_SLUG)/(PAGE_SLUG)` (see topic collections for how this gets more complicated) or `https://alpha.austin.gov/(DEPARTMENT_SLUG)/(PAGE_SLUG)`

## Resident facing implementation (Code):

Janis (js) - [static.config.js](https://github.com/cityofaustin/janis/blob/master/static.config.js)

### [Themes](themes.md)

![theme](themes/url.png)

### Topic collections

![theme](topic_collections/url.png)

### Topics (TODO)

### Page slug (TODO)
