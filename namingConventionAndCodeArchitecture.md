# Naming convention and code architecture

In this files are naming rules and structure rules.

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




