# version-numbering-standards

Semantic versioning standards are:

major.minor.patch.

This works fine for our code-only repositories.

However, for our respositories that include hardware and firmware, here is our proposed update for repository 1.2.3:

1. Major changes, including:
  * Board dimensions
  * Board layout
  * Fundamental board function
2. Minor changes but that nonetheless can break board/firmware/manufacture/mounting hardware compatibility, including:
  * Board component addition/removal
  * Component placement on board: even minor changes to this affect its ability to be manufactured, typically requiring new setup charges.
  * Firmware if committed as part of a single package that includes hardware updates; firmware updates not directly coupled to hardware updates go under the traditional "patch" number, below. (Indeed, this is a broader rule; see below this numbered/bulleted list)
3. Changes in documentation, firmware, or anciliary components
  * Board silkscreen. This can require new setup charges, but these updates aren't necessary, and the charges in this case may be less or waived.
  * Firmware updates without corresponding "minor" or "major" hardware updates
  * Improvements in housings and mounts that do not require a change to the physical board

Any changes in lower categories may be subsumed into changes in higher-level categories. (That is, there could be board silk changes in a transition from 1.3.12 to 2.0.0.)

For a repository X.Y.Z, Each board may then wear a number that is simply **X.Y**. This means that we can keep the same number regardless of firmware upgrades or changes to the housing, mounting, etc. One may include the third number if it relates to silkscreen updates, but this is not necessary; **X.Y** will by default refer to the *most recent* version of **X.Y** at the time of fabrication.
