# Requiem-Experience

This is an auto-patcher which is meant to create patch for Experience mod, to be used along with Requiem. It takes care of 2 things:
* Adjusts quest types for various mods to reduce/increase XP - would only affect quests which present in your load order:
  * Vanilla Skyrim: reduces XP from Helgen & Whiterun main quests;
  * Requiem: removes XP from Requiem install/init quest;
  * Live Another Life: removes XP from Chargen and new life selection;
  * SunHelm: removes XP from SunHelm install/init quest;
  * Missives: here is the place where most of changes takes place, all the missives are being assigned with different quest types depending on their estimated difficulty. Also due to usage of regular expressions (masks), it's able to apply this changes to almost any additional regions (e.g. you have Wyrmstooth and Wyrmstooth Missives? they'll get auto-adjusted as well)
* Creates/overwrites DefaultRaces.csv to assign appropriate values for kill XP, also highly dependant on your load order. General idea is to base of average level of enemy to calculate reward, with some edge cases covered with overrides.
