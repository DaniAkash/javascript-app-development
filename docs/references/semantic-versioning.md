---
id: semantic-versioning
title: What is Semantic Versioning
sidebar_label: Semantic Versioning
---

Almost all software that are developed have some kind of dependency over other software. For example, you might have encountered software stating their minimum requirements that needs to be met in order for the software to work fine. One application may say, it needs Windows 10, version 1507. In this case, the version follows YYMM format and microsoft has good reasons to have it that way.

So now that we understand versioning, we can see how softwares are generally versioned. This type of versioning unlike the former is more widespread and more commonly understood across the industry.

## General Structure

### 0 — Pre-MVP/Alpha
This is used when your project is a proof of concept / minimum viable product. There is no need of versioning at this stage as the product is not usable yet.

### Major.Minor.Patch — Alpha/Beta
When you are ready with the release of the first version of the product, its adviced to start a versioning system.
Consider this example, Your software is now at version 1.0.0 after the first release.

### Major
If you find that you need to add a new feature / set of new features and in doing so, you would break at least one existing functionality and you want the people using your existing version to exercise caution in upgrading to this version, in such cases, you may increase the `Major component` making it `2.0.0`

### Minor
If you add a new feature and you have tested that the new feature does not make any breaking changes, then we would increase the middle component called `Minor component`. In other words, all parts of your existing release works and you are just adding more features, then use this. So here it would become `1.1.0`

### Patch
You find a bug that needs to be fixed immediately. In this case you would increment the `Patch component` and make the version as `1.0.1`
