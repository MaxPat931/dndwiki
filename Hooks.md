![Up to date as of 2.0.0](https://img.shields.io/static/v1?label=dnd5e&message=2.0.0&color=informational)

## Actor

### `dnd5e.preRollAbilityTest`

Fires before an ability test is rolled. Returning `false` will prevent the normal rolling process.

| Name | Type | Description |
| ---- | ---- | ----------- |
| actor | Actor5e | Actor for which the ability test is being rolled. |
| config | D20RollConfiguration | Configuration data for the pending roll. |
| abilityId | string | ID of the ability being rolled as defined in `DND5E.abilities`. |

### `dnd5e.rollAbilityTest`

Fires after an ability test has been rolled.

| Name | Type | Description |
| ---- | ---- | ----------- |
| actor | Actor5e | Actor for which the ability test has been rolled. |
| roll | D20Roll | The resulting roll. |
| abilityId | string | ID of the ability being rolled as defined in `DND5E.abilities`. |

### `dnd5e.preRollAbilitySave`

Fires before an ability save is rolled. Returning `false` will prevent the normal rolling process.

| Name | Type | Description |
| ---- | ---- | ----------- |
| actor | Actor5e | Actor for which the ability save is being rolled. |
| config | D20RollConfiguration | Configuration data for the pending roll. |
| abilityId | string | ID of the ability being rolled as defined in `DND5E.abilities`. |

### `dnd5e.rollAbilitySave`

Fires after an ability save has been rolled.

| Name | Type | Description |
| ---- | ---- | ----------- |
| actor | Actor5e | Actor for which the ability save has been rolled. |
| roll | D20Roll | The resulting roll. |
| abilityId | string | ID of the ability that was rolled as defined in `DND5E.abilities`. |

### `dnd5e.preRollDeathSave`

Fires before a death saving throw is rolled. Returning `false` will prevent the normal rolling process.

| Name | Type | Description |
| ---- | ---- | ----------- |
| actor | Actor5e | Actor for which the death saving throw is being rolled. |
| config | D20RollConfiguration | Configuration data for the pending roll. |

### `dnd5e.rollDeathSave`

Fires after a death saving throw has been rolled, but before updates have been performed.  Returning `false` will prevent updates from being performed.

| Name | Type | Description |
| ---- | ---- | ----------- |
| actor | Actor5e | Actor for which the death saving throw has been rolled. |
| roll | D20Roll | The resulting roll. |
| details | object |  |
| details.updates | object | Updates that will be applied to the actor as a result of this save. |
| details.chatString | string | Localizable string displayed in the create chat message. If not set, then no chat message will be displayed. |

### `dnd5e.preRollSkill`

Fires before a skill check is rolled. Returning `false` will prevent the normal rolling process.

| Name | Type | Description |
| ---- | ---- | ----------- |
| actor | Actor5e | Actor for which the skill check is being rolled. |
| config | D20RollConfiguration | Configuration data for the pending roll. |
| skillId | string | ID of the skill being rolled as defined in `DND5E.skills`. |

### `dnd5e.rollSkill`

Fires after a skill check has been rolled.

| Name | Type | Description |
| ---- | ---- | ----------- |
| actor | Actor5e | Actor for which the skill check has been rolled. |
| roll | D20Roll | The resulting roll. |
| skillId | string | ID of the skill that was rolled as defined in `DND5E.skills`. |

### `dnd5e.preRollHitDie`

Fires before a hit die is rolled. Returning `false` will prevent the normal rolling process.

| Name | Type | Description |
| ---- | ---- | ----------- |
| actor | Actor5e | Actor for which the hit die is to be rolled. |
| config | D20RollConfiguration | Configuration data for the pending roll. |
| denomination | string | Size of hit die to be rolled. |

### `dnd5e.rollHitDie`

Fires after a hit die has been rolled, but before updates have been applied. Returning `false` will prevent updates from being performed.

| Name | Type | Description |
| ---- | ---- | ----------- |
| actor | Actor5e | Actor for which the hit die has been rolled. |
| roll | D20Roll | The resulting roll. |
| updates | object |  |
| updates.actor | object | Updates that will be applied to the actor. |
| updates.class | object | Updates that will be applied to the class. |

### `dnd5e.preRollClassHitPoints`

Fires before hit points are rolled for a character's class.

| Name | Type | Description |
| ---- | ---- | ----------- |
| actor | Actor5e | Actor for which the hit points are being rolled. |
| item | Item5e | The class item whose hit dice will be rolled. |
| rollData | object |  |
| rollData.formula | string | The string formula to parse. |
| rollData.data | object | The data object against which to parse attributes within the formula. |
| messageData | object | The data object to use when creating the message. |

### `dnd5e.preShortRest`

Fires before a short rest is started. Returning `false` will prevent the rest from being performed.

| Name | Type | Description |
| ---- | ---- | ----------- |
| actor | Actor5e | The actor that is being rested. |
| config | RestConfiguration | Configuration options for the rest. |

### `dnd5e.preLongRest`

Fires before a long rest is started. Returning `false` will prevent the rest from being performed.

| Name | Type | Description |
| ---- | ---- | ----------- |
| actor | Actor5e | The actor that is being rested. |
| config | RestConfiguration | Configuration options for the rest. |

### `dnd5e.preRestCompleted`

Fires after rest result is calculated, but before any updates are performed. Returning `false` will prevent updates from being performed.

| Name | Type | Description |
| ---- | ---- | ----------- |
| actor | Actor5e | The actor that is being rested. |
| result | RestResult | Details on the rest to be completed. |

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

### `dnd5e.preAdvancementManagerComplete`

| Name | Type | Description |
| ---- | ---- | ----------- |
| advancementManager | AdvancementManager | The advancement manager. |
| actorUpdates | object | Updates to the actor. |
| toCreate | object[] | Items that will be created on the actor. |
| toUpdate | object[] | Items that will be updated on the actor. |
| toDelete | string[] | IDs of items that will be deleted on the actor. |

### `dnd5e.advancementManagerComplete`

Fires when an `AdvancementManager` is done modifying an actor.

| Name | Type | Description |
| ---- | ---- | ----------- |
| advancementManager | AdvancementManager | The advancement manager that just completed. |

### Document Modification Context

All of the normal 'pre' and 'post' hook events for document modification when an advancement manager flow finishes (Actor Update, Item Creation, Item Update, and Item Deletion) have a custom flag on them: `isAdvancement`. This allows a hook listener to react differently to advancement-created hook events vs normal ones.

```js
Hooks.on('updateActor', (actor, change, options) => {
  if ( options.isAdvancement ) {
    // do something special
  }
})
```