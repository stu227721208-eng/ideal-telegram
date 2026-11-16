# HarvestPlus — One-page GUI and durability update

Minecraft Java 1.21.11 Fabric source project.

## Changes
- One-page options screen with a single toggle per setting; green right = ON, red left = OFF.
- Toggle switches animate smoothly when clicked. Open settings with H.
- Leaves and mushroom/nether caps now use world.breakBlock(...), not the axe, so they consume no axe durability.
- Logs continue to use vanilla tryBreakBlock; ordinarily each log costs one durability before Unbreaking, including the first log you manually break. Axe protection retains the last durability point for automatic harvesting.
- Existing tree, ore, crop, and replant features retained.

## Build
Open the directory containing build.gradle in IntelliJ and run Gradle > Tasks > build > build.

## Caveats
This is an uncompiled, untested source update. The original project's server commands still lack permission checks, and client/server settings are not synchronized for multiplayer. Do not publish as production-ready until tested and secured. Leaf ownership checks are conservative, and touching canopies can leave ambiguous leaves behind. Normal Minecraft Unbreaking enchantments can reduce durability consumed.
