# Dependencies List

A list of dependencies for each script in the project (WIP)
Dependency is when script A calls other scripts.
Reference is when other scripts call script A.

## Table of scripts

|                             |                             |                             |                             |                             |
|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|
| [Crafting](#crafting) 	  | [CraftingRecipe](#craftingrecipe) | [UpgradeRecipe](#upgraderecipe) | [CraftingUI](#craftingui) | [RequiredMaterialUI](#requiredmaterialui) |
| [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) |
| [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) |
| [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) |
| [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) |
| [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) |
| [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) |
| [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) |
| [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) | [script name](#script_name) |

## Crafting
<details>
  <summary> Click here </summary>
  
| Dependencies    | References |
|-----------------|------------|
| CraftingRecipe    | UpgradeRecipe |
| UpgradeRecipe     | CraftingSlime |
| PlayerInteraction | ---- |
| UIManager         | ----- |
</details>

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
