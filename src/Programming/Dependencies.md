# Dependencies List

A list of dependencies for each script in the project (WIP)
Dependency is when script A calls other scripts.
Reference is when other scripts call script A.

## Table of scripts

|                             |                             |                             |                             |                             |
|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|
| [Crafting](#crafting) 	  | [CraftingRecipe](#craftingrecipe) | [UpgradeRecipe](#upgraderecipe) | [CraftingUI](#craftingui) | [RequiredMaterialUI](#requiredmaterialui) |
| [CloudsUISettings](#cloudsuisettings) | [CloudGeneration](#cloudgeneration) | [GrabSlime](#grabslime) | [PlayerMovementControl](#playermovementcontrol) | [PlayerGrabSlime](#playergrabslime) |
| [playerblockinteraction](#playerplockinteraction) | [SleepingSlime](#sleepingslime) | [TimeManager](#timemanager) | [SlimeStatus](#slimestatus) | [Slime](#slime) |
| [SleepingSlime](#sleepingslime) | [PlayerMovementController](#playermovementcontroller) | [SlimeLevelUpInfo](#slimelevelupinfo) | [IslandHeart](#islandheart) | [script name](#script_name) |
| [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) |
| [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) |
| [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) |
| [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) |
| [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) |



## CraftingRecipe
<details>
  <summary> Click here </summary>
  
| Dependencies    | References |
|-----------------|------------|
| ItemBase  	   | UpgradeRecipe |
| RequiredMaterial | CraftingUI |
| PlayerInventory  | CraftingRecipeUI |
| ItemStack  	   | UIManager |
| -------------    | Crafting |
</details>

## UpgradeRecipe
<details>
  <summary> Click here </summary>
  
| Dependencies    | References |
|-----------------|------------|
| CraftingRecipe   | Crafting |
| Crafting 		   | CraftingUI |
| PlayerInventory  | CraftingRecipe |
| ItemStack  	   | ----- |
| UIManager        | ----- |
</details>

## CraftingUI
<details>
  <summary> Click here </summary>
  
| Dependencies    | References |
|-----------------|------------|
| CraftingRecipe     | UIManager  |
| PlayerInventory    | CraftingUI |
| CraftingRecipeUI   | ----- |
| RequiredMaterial   | ----- |
| RequiredMaterialUI | ----- |
| UIManager 		 | ----- | 
</details>

## RequiredMaterialUI
<details>
  <summary> Click here </summary>
  
| Dependencies    | References |
|-----------------|------------|
| RequiredMaterial | CraftingUI |
</details>

## CloudsUISettings
<details>
  <summary> Click here </summary>

| Dependencies    | References |
|-----------------|------------|
| CloudGeneration | ---------- |

</details>

## CloudGeneration
<details>
  <summary> Click here </summary>

| Dependencies    | References |
|-----------------|------------|
| ---             | CloudsUISettings |

</details>

## GrabSlime
<details>
  <summary> Click Here </summary>

| Dependencies    | References |
|-----------------|------------|
| Slime | Interactable |
| Interactable| ----- |
| Interaction| ----- |
| AkSoundEngine | ----- |
| PlayerMovementController | ----- |

</details>

## PlayerMovementControl
<details>
  <summary> Click Here </summary>

| Dependencies    | References |
|-----------------|------------|
| UIManager | FootstepsAnimationSound |
| TimeManager | DroppedItem |
| StarterAssetsInputs | InteractionsViaUI |
| PlayerGrabSlime | PlayerDataManager |
| TrainersManager | PlayerCamController |
| AkSoundEngine | FeedSlime |
| PlayerInputActions | GrabSlime |
| GameEvents | PetSlime |
| InputManager | DroneActionSequence |
| StarterAssetsInputs | DestroyObject |
| SerializationManager | PhotoModeUIController |
| RespawnPlayerCurrentIsland | PlayerTooltipPickup |
| PlayerDataManager | PlayerEnergyController |

</details>

## Slime
<details>
  <summary> Click Here </summary>

| Dependencies    | References |
|-----------------|------------|
| IFeedable | SlimeManager |
| SlimeSaveData | UIManager |
| SlimeName | SlimeAgent |
| SlimeManager | PlayerGrabSlime |
| DialogManager | PlayerNameSlime |
| PetSlime | CraftingSlime |
| SlimeAgent | ColdWarmSystemSlime |
| AkSoundEngine | FeedSlime |
| DialogData | GrabSlime |
| SlimeLevelUpInfo | PetSlime |
| Player | SleepingSlime |
| PlayerBlockInteraction | SlimeUIInteract |
| Outline | RenameSlimeUI |
| ----- | UIController |
| ----- | SlimeTransportHandler |
|-----  | SlimeStatus|

</details>

## PlayerGrabSlime
<details>
  <summary> Click Here </summary>

| Dependencies    | References |
|-----------------|------------|
| PlayerBlockInteraction | PlayerMovementController |
| Slime | ----- |
| AkSoundEngine | ----- |

</details>

## PlayerBlockinteraction
<details>
  <summary> Click Here </summary>

| Dependencies    | References |
|-----------------|------------|
| ItemStack | PlayerTooltipPickup |
| Island1BuildBlocker | Bridge |
| BuildAreaManager | Table |
| AkSoundEngine | CreativeItem |
| Island1BuildBlocker | PlaceableItem |
| PlayerToolAnimation | ToolItem |
| PlayerInventory | PlayerGrabSlime |
| ToolController | ToolController |
| ----- | CraftingRecipe |
| ----- | UpgradeRecipe |
| ----- | Slime |
| ----- | DestroyObject |
| ----- | GetBlock |

</details>

## SlimeAgent
<details>
  <summary> Click Here </summary>

| Dependencies    | References |
|-----------------|------------|
| ColdWarmSystemSlime | Slime |
| FeedSlime | SlimeUIInteract |
| Slime | ----- |
| SleepingSlime | ----- |
| ItemBase | ----- |
| PlayerInventory | ----- |
| Bed | ----- |


</details>

## SleepingSlime
<details>
  <summary> Click Here </summary>

| Dependencies    | References |
|-----------------|------------|
| Interaction | SlimeAgent |
| Bed | Bed |
| DialogData | ----- |
| SlimeManager | ----- |
| Slime | ----- |
| Interactable | ----- |

</details>

## TimeManager
<details>
  <summary> Click Here </summary>

| Dependencies    | References |
|-----------------|------------|
| GameEvents | StarFade |
| Time | SerializationManager |
| PlayerDataManager | WwiseManager |
| ----- | PlayerMovementController |
| ----- | LightingManager |
| ----- | LowerPlaneManager |
| ----- | MoonOrbit |
| ----- | SkyboxManager |
| ----- | PostMod |
| ----- | PhotoModeUIController |
| ----- | TimechangeInScene |
| ----- | TimeEvents|

</details>

## SlimeStatus

<details>
  <summary> Click here </summary>

| Dependencies        | References |
|---------------------|------------|
| Slime               | -          |
| SleepingSlime       | -          |
| ColdWarmSlimeSystem | -          |

</details>

## SleepingSlime

<details>
  <summary> Click Here </summary>

|Dependencies        | References |
|--------------------|------------|
|Interaction        |   SlimeAgent|
|Bed                 |  Bed|
|DialogData       |     SlimeStatus|
|SlimeManager     |     -----|
|Slime             |    -----|
|Interactable       |   -----|

</details>

## PlayerMovementController

<details>
  <summary> Click Here </summary>

| Dependencies    | References |
|-----------------|------------|
| CharacterController | FootstepsAnimationSound |
| PlayerInput | DroppedItem |
| Animator | InteractionsViaUI |
| StarterAssetsInputs | PlayerDataManager |
| PlayerGrabSlime | PlayerCamController|
| TrainersManager | FeedSlime |
| PlayerInputActions | GrabSlime |
| AkSoundEngine | PetSlime |
| GameEvents | DroneActionSequence |
| InputManager | DestroyObject |
| SerializationManager | null |
| RespawnPlayerCurrentIsland | null |
| PlayerDataManager | null |
| TimeManager | null |
| UIManager | null|

</details>


## SlimeLevelUpInfo

<details>
  <summary> Click Here </summary>

| Dependencies    | References |
|-----------------|------------|
| null | FeedSlime|
| null | Slime|

</details>


## IslandHeart

<details>
  <summary> Click Here </summary>

| Dependencies    | References |
|-----------------|------------|
| IslandHeartInfo| IslandHeartRangeFX |
| IslandHeartBuildReach| null |
| AK.Wwise.Event| null |
| ItemStack| null |
| PlayerGrabSlime| null |
| Slime| null |
| WaitForSeconds| null |

</details>