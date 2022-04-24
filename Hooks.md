## Actor
- `dnd5e.restCompleted`: Fires when the actor completes a short or long rest. Gets passed the actor instance a `RestResult` object containing information on the rest operation.
- `dnd5e.transformActor`: Fires just before a new actor is created during the transform process. Gets passed the original actor instance, the target actor instance, the data object that will be used to create the synthetic actor, and the options that were selected in the transform dialog.

## Advancement
- `dnd5e.preAdvancementManagerRender`: Fires when an `AdvancementManager` is about to be processed. Gets passed a single parameter containing the `AdvancementManager` instance.
- `dnd5e.advancementManagerComplete`: Fires when an `AdvancementManager` is done modifying an actor. Gets passed a single parameter containing the `AdvancementManager` instance.