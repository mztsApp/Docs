# Naming convention and code architecture

In this files are naming rules and structure rules. 

***use only names in english language !**

## Naming branches and commits

Naming commits is very important, becouse on this basis package version will be updated.

- ```fix``` - bug fix for the user, not a fix to a build script,
- ```feat``` - new feature for the user, not a new feature for build script,
- ```chore``` - updating grunt tasks etc; no production code change,
- ```test```- adding missing tests, refactoring tests; no production code change

 ```<fix/feat/chore/test>(scope)/<chenging-description>``` **- branches**,
 ```<fix/feat/chore/test>(scope): <chenging description>``` **- commits**

 
**scope** is not essencial, but if you can, try use it. *In **UI repository** using scope is required! 
 
 ### exemples:
 - branches
```git
git branch fix(switch)/improving-switch-component-displaying
```
 - commits
```git
git commit -m 'fix(switch): improving switch component displaying'
```
## Structure 

**Convention:**
- PascalCase exemple: ```TypeOfButtonProps.tsx```,
- camelCase exemple: ```getBigestValue.tsx```

1. components - use PacalCase, exemples:
  - components
    - ComponentName
      - ComponentName.tsx
      - ComponentName.styled.ts
      - ComponentName.types.ts
      - ComponentName.consts.ts
      - ComponentName.pages.ts
      - ComponentName.utils.ts
2. consts - use camelCase, exemples: 
   - consts
     - getFirstColorOfArray.ts
     - getAddedNumbers.ts

## Function naming

It is very important to create properly name of functions to make other developer's works easier. Reading code should be like readig books, function name should describe, what function do.

Therefore folow this rules:
 - function always should began from verbs; exemples: ```get```SomeValue, ```set```SomeValues, ```handle```SomeEvent
 - use normaly used verbs by developers: 
   - if function return value should began from ```get```; exemple: ```getFirstElementOfArray = (array) => array(0)```
   - if function handle evet should began from ```handle```
   - if function return void and set value should began from ```set```
 - use CamelCase; exempes: ```getBigestValueOfArray```, ```getObjectFromArray```
 - never use shortened name; exemple: ```(e) => return e.type``` or ``` array.map((c, i, a) => ... )```instead use this ```(event) => event.type``` or ```array.map((current, index, array) => ... )```
