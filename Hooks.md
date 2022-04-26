## Actor

### `dnd5e.restCompleted`

Fires when the actor completes a short or long rest.

| Name | Type | Description |
| ---- | ---- | ----------- |
| actor | Actor5e | The actor that just completed resting. |
| result | RestResult | Details on the completed rest. |

### `dnd5e.transformActor`

Fires just before a new actor is created during the transform process.

| Name | Type | Description |
| ---- | ---- | ----------- |
| actor | Actor5e | The original actor before transformation. |
| target | Actor5e | The target actor being transformed into. |
| data | object | The merged data that will be used to create the newly-transformed actor. |
| options | TransformationOptions | Options that determine how the transformation is performed. |

## Advancement

### `dnd5e.preAdvancementManagerRender`

Fires when an `AdvancementManager` is about to be processed. Returning `false` will prevent the normal rendering process.

| Name | Type | Description |
| ---- | ---- | ----------- |
| advancementManager | AdvancementManager | The advancement manager about to be rendered. |

### `dnd5e.advancementManagerComplete`

Fires when an `AdvancementManager` is done modifying an actor.

| Name | Type | Description |
| ---- | ---- | ----------- |
| advancementManager | AdvancementManager | The advancement manager that just completed. |