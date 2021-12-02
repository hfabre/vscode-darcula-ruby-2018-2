# Vscode Darcula 2018.2 for Ruby
Override rokoroku's Darcula theme to be closer to the one from RubyMine 2018.2.
This is the closest look I could get without making any PR to base plugins.
It is not meant to be used as a plugin since I don't want to maintain one. To use it simply install
plugins from base plugins sections and paste content of `settings.json` at the end of yours.

## Base plugins
This is based on the following plugins:

- [Darcula theme](https://marketplace.visualstudio.com/items?itemName=rokoroku.vscode-theme-darcula)
- [Ruby](https://marketplace.visualstudio.com/items?itemName=rebornix.Ruby)
- [JetBrains font (not a plugin)](https://www.jetbrains.com/lp/mono/)

## Notes

To be clear everything beyond this point is way beyond my understanding of vscode grammar / regexp,
so I would not be able to solve any of those in a near future. If you can (and do) please ping me so I can update this to be as close
as possible from the original theme.

### Known bugs

#### Probably fixable with a PR to ruby extension repo

- Methods calls are yellow (I was not able to override `entity.name.function.ruby` by `meta.function-call.ruby`)
- Local variables are white (Since the method call are only detected as local variables by the Ruby extension there was way to many blue so I kept it white, this could be put back if Rails special method are implemented in the ruby extension (or a new rails extension)

#### Not fixable by any of base extension at least with my understanding of vscode

- Unused parameters/variables should be grey

### Cool evolutions

- Handle Rails special method (such as model callbacks, validations, relations, and controller callbacks)
- Tag variables to see if they come from parameters or a local assignation (purple/blue in RubyMine)
