## Actor

### `dnd5e.restCompleted`

| Name | Type | Description |
| ---- | ---- | ----------- |
| actor | Actor5e | The actor that just completed resting. |
| result | RestResult | Details on the completed rest. |

### `dnd5e.transformActor`

| Name | Type | Description |
| ---- | ---- | ----------- |
| actor | Actor5e | The original actor before transformation. |
| target | Actor5e | The target actor being transformed into. |
| data | object | The merged data that will be used to create the newly-transformed actor. |
| options | TransformationOptions | Options that determine how the transformation is performed. |

## Advancement

### `dnd5e.preAdvancementManagerRender`

| Name | Type | Description |
| ---- | ---- | ----------- |
| advancementManager | AdvancementManager | The advancement manager about to be rendered. |

### `dnd5e.advancementManagerComplete`

| Name | Type | Description |
| ---- | ---- | ----------- |
| advancementManager | AdvancementManager | The advancement manager that just completed. |