---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# gameTargetSearchQuery

## Description

Used by functions of \[TargetingSystem], to specify the parameters for searches of targets.

* \[this.testedSet] decides the shape of the area of the search (in the limits of \[this.maxDistance]). \[TargetingSet.Frustum] covers the whole cone of vision of the instigator. \[TargetingSet.Visible] and \[TargetingSet.ClearlyVisible] additionally require differing degrees of line-of-sight. \[TargetingSet.Complete] covers a sphere around the instigator.
* \[this.searchFilter] identifies the nature of the objects that will qualify for the search. See REDmod script resources for examples of currently used filters, like \[TSF\_NPC].
