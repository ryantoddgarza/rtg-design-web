# rtg-design-web

Web design system for my personal digital properties.

Additional design systems:

- [rtg-design](https://github.com/ryantoddgarza/rtg-design.git): Core design system

## Using SASS in your project

Compile your project's CSS from the rtg-design-web source SASS.

```scss
@use 'rtg-design-web';
```

## Using design tokens

### Font family

Font family tokens make it possible to set font family based on type or role.

#### Available fonts

The following font stacks are available.

| Token       | Value                                                                                                          |
| ----------- | -------------------------------------------------------------------------------------------------------------- |
| `helvetica` | `Helvetica Neue, Helvetica, Roboto, Arial, sans-serif`                                                         |
| `monospace` | `ui-monospace, SFMono-Regular, SF Mono, Menlo, Consolas, Liberation Mono, monospace`                           |
| `system`    | `-apple-system, BlinkMacSystemFont, Segoe UI, Helvetica, Arial, sans-serif, Apple Color Emoji, Segoe UI Emoji` |

#### Type-based tokens

| Token   | Value       |
| ------- | ----------- |
| `mono`  | `monospace` |
| `sans`  | `helvetica` |
| `serif` | `false`     |

#### Role-based tokens

| Token     | Value       |
| --------- | ----------- |
| `alt`     | `false`     |
| `body`    | `helvetica` |
| `code`    | `monospace` |
| `heading` | `helvetica` |
| `ui`      | `helvetica` |

#### Using font family tokens

| Context  | Usage           | Example                       |
| -------- | --------------- | ----------------------------- |
| function | `family(token)` | `font-family: family('body')` |

### Spacing units

Spacing unit tokens are based on multiples of 8px.

#### Spacing unit tokens

**Any** numeric token is supported.

#### Using spacing unit tokens

| Context  | Usage          | Example             |
| -------- | -------------- | ------------------- |
| function | `units(token)` | `padding: units(2)` |

### Breakpoints

#### Breakpoint tokens

| Token        | Value    |
| ------------ | -------- |
| `phone`      | `320px`  |
| `phone-lg`   | `480px`  |
| `tablet`     | `640px`  |
| `tablet-lg`  | `880px`  |
| `desktop`    | `1024px` |
| `desktop-lg` | `1200px` |
| `widescreen` | `1400px` |

#### Using breakpoint tokens

| Context  | Usage               | Example                           |
| -------- | ------------------- | --------------------------------- |
| function | `breakpoint(token)` | `max-width: breakpoint('tablet')` |
| mixin    | `at-media(token)`   | `@include at-media('desktop')`    |

## Contributing

### Versioning

This design system uses [SemVer](https://semver.org/)—Semantic Versioning. The three types of versions are:

- **Major** versions contain breaking changes.
- **Minor** versions add new features or deprecate existing features without breaking changes.
- **Patch** versions fix defects or optimize existing features without breaking changes.
