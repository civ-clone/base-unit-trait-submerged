# base-unit-trait-submerged

The `Submerged` unit trait: a unit type with it travels submerged.

A unit type with this trait cannot attack land, and the game's rules may hide it or weaken its defence.

For example: Civ1: Submarine (no attack on land). Civ2: flag 3 (Submarine).

A game declares which of its unit classes have the trait with `UnitTraits` rules from `@civ-clone/core-unit`, and its
rules ask `unit.hasTrait(Submerged)`:

```ts
import Submerged from '@civ-clone/base-unit-trait-submerged/Submerged';
import { unitTraits } from '@civ-clone/core-unit/Rules/UnitTraits';

ruleRegistry.register(...unitTraits('my-game:unit/trait', MyUnit, Submerged));
```

Part of the unit traits design (civ-clone/web-renderer#1008).
