# Carnalitas EK2 Compatibility

This is a [Carnalitas](https://www.loverslab.com/files/file/14207-carnalitas-unified-sex-mod-framework-for-ck3/) compatibility patch for [Elder Kings 2](https://steamcommunity.com/sharedfiles/filedetails/?id=2887120253). It reconciles changes to the character window and other game files made by these two mods. It also adds Elder Scrolls lore-based slavery doctrines, similar to the *Carnalitas Historical Slavery Doctrines* mod. It has been tested with CK3 1.8.1, EK2 0.11.2a, and Carnalitas 1.7.

Note that since Carnalitas itself has issues with CK3 1.8.*, it is strongly recommended to use the [GUK Fix Carnalitas](https://www.loverslab.com/files/file/24787-guk_fix_carnzip/) compatibility patch as well.

Load order:

* Elder Kinds 2
* Carnalitas
* GUK Fix Carnalitas
* Carnalitas EK2 Compatibility
* (other mods based on Carnalitas)

Load order with [Carnalitas Slavery Reimagined](https://www.loverslab.com/topic/204734-mod-carnalitas-slavery-reimagined/):

* Elder Kinds 2
* Carnalitas
* GUK Fix Carnalitas
* Carnalitas EK2 Compatibility
* Carnalitas Slavery Reimagined
* CSR EK2 Compatibility

## Compatibility Fixes

### Character Window

All changes to the character window made by Carnalitas and EK2 have been reconciled, so that all additional interface elements introduced by both are present. Additional EK2 interface elements such as arcana, magicka, etc., as well as Carnalitas changes such as slaves at the bottom of the *Relations* tab, are all properly shown.

### Interactions and Events

All changes to courtier and guest management, as well as birth and pregnancy events made by Carnalitas and EK2 have been reconciled. The EK2 files have been taken as base, and Carnalitas changes have been applied on them. The main effects are the following (assuming Carnalitas was previously later than EK2 in the load order):

* The EK2 cultural parameter `foreign_guest_hostility` of Xenophobic cultures is properly taken into account when scoring guests.
* EK2 Argonian hatchlings and Birthsigns are properly handled or added on birth.
* EK2 Argonians laying eggs is properly handled during pregnancy.
* References to vanilla faiths present in the original Carnalitas no longer fill the logs with error messages.

## Lore-based Slavery Doctrines

This mod introduces a *Elder Scrolls Lore* game rules setting for Carnalitas slavery doctrines, and makes it the default. If this setting is active, all faiths have accurate doctrines for *Righteous Faith Slavery* and *Hostile Faith Slavery* based on Elder Scrolls lore research. The effect is similar to using the *Carnalitas Historical Slavery Doctrines* mod (available as a separate [Carnalitas](https://www.loverslab.com/files/file/14207-carnalitas-unified-sex-mod-framework-for-ck3/) download) in vanilla.

Although there is already [Elder Kings Slavery Doctrines](https://steamcommunity.com/sharedfiles/filedetails/?id=2887372040), I don't recommend using it, since it's mostly (badly) copy-pasted from *Carnalitas Historical Slavery Doctrines*, no sources are cited, comments don't correspond to the code, and some of the decisions taken are dubious. Still, if you would like to use it, just place it after this mod in the load order.

### Overview

The timeline of the EK2 mod starts in 2E 440 or 2E 450. This is well after slavery was initially abolished by the [Alessian Slave Rebellion](https://elderscrolls.fandom.com/wiki/Alessian_Slave_Rebellion), but before it was finally outlawed in all imperial lands, which took place after the seventh century of the Second Era (see [Outlawing of slavery]((https://elderscrolls.fandom.com/wiki/Slavery#Outlawing_of_slavery))). I take this to mean that slavery is sufficiently widespread for Aedric religions to frown upon it, but not fully criminalize it, and for Aurbic and especially Daedric religions to be even more lenient, especially towards *Hostile Faith Slavery*.

### Righteous Faith Slavery

The baseline for *Righteous Faith Slavery* depending on religious family is as follows:

* *Aedric*: criminal
* *Aurbic*: shunned
* *Daedric*: shunned

This is modified by the special doctrine *Worship of Molag Bal*, since [Molag Bal](https://elderscrolls.fandom.com/wiki/Molag_Bal) is the Daedric Prince of enslavement. If it's allowed or pantheon, *Righteous Faith Slavery* is accepted, and if it's shunned or criminal *Righteous Faith Slavery* is shunned or criminal as well. The following religions or faiths are affected by this:

* *Thousand Cults*, *Vinedusk Exemptions*: shunned (although *Aedric*)
* *Necromantic*: accepted (although *Aurbic*)
* *Khajiiti*, *Dwemeri*, *Stone*, *Vampiric*: criminal (although *Aurbic*)
* *Molag Bal*, *Reach*, *Azurite*: accepted (although *Daedric*)
* *Velothi*, *Meridia*: criminal (although *Daedric*)

### Hostile Faith Slavery

The baseline for *Hostile Faith Slavery* depending on religious family is as follows:

* *Aedric*: shunned
* *Aurbic*: shunned
* *Daedric*: accepted

There are the following exceptions to the above:

* *Hostile Faith Slavery* is accepted in *Aldmeri*, *Trinimac*, and *Yoku* religions (although *Aedric*):
  - > Altmer were still said to have humanoid slaves during the seventh century of the Second Era
  ([Altmer Society](https://elderscrolls.fandom.com/wiki/Altmer#Society))
  - [Tinimac]( https://elderscrolls.fandom.com/wiki/Trinimac) is the Daedric Prince Malacath, so similar attitude to slavery
  - > Slavery was widespread in Yokuda, and continues today in some places in Hammerfell.
  ([reddit](https://www.reddit.com/r/teslore/comments/j58xuf/what_other_races_practiced_slavery/))

* *Hostile Faith Slavery* is criminal in *Nedic-Nordic* and *Marukhati* religions (although *Aedric*). These religions descend from the one founded by Alessia in which slavery was outlawed ([Alessia's_Reign](https://elderscrolls.fandom.com/wiki/Alessian_Empire#Alessia's_Reign))

* *Hostile Faith Slavery* is accepted in *Hist*, *Khajiiti*, and *Dwemeri* religions (although *Aurbic*):
  - > However, under the effects of the Mad Hist, the Xit-Xaht tribe enslaved many of their own species to rebuild the Ruins of Mazzatun. Argonian mothers would sometimes sell their own children into slavery. ([Slavery in Black Marsh](https://elderscrolls.fandom.com/wiki/Slavery#Black_Marsh))
  - > Khajits, have it since ancient times and still have, sell their own kind to other races. ([reddit](https://www.reddit.com/r/teslore/comments/j58xuf/what_other_races_practiced_slavery/))
  - > Those who agreed became the savage Falmer, soon becoming slaves to the Dwemer. ([Slavery in Skyrim](https://elderscrolls.fandom.com/wiki/Slavery#Skyrim))

In addition, *Hostile Faith Slavery* is never less accepted than *Righteous Faith Slavery*, so if the latter is accepted due to the special doctrine *Worship of Molag Bal*, the former is accepted as well.
