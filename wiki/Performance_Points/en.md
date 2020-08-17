<!-- TODO:
- add bonus pp section
- figure out what to do with FAQ
- re-cleanup this -->

# Performance points

**Performance points** ( or **pp** for short) is a ranking metric that aims to be more contextually relevant to a player's progression in osu!.

It aims to shift the focus of skill progression from the amount of time played to an actual representation of the player's skill. This is attained by the calculation of a unique score known that is based on the difficulty of a beatmap and a player's performance on that [beatmap](/wiki/Beatmaps).

## History

The first initial implementation of such a score was revealed to the public during April 2012 and was known only as the mysterious *'???'* project, the enigmatic system eventually received its full name later on in the month.

Known thereafter as "pp" (an abbreviation for "performance points"), this new system sought to change the previous standard of player performance from simply total [score](/wiki/Score) to something that accurately reflected skill. The new system was met to widespread acclaim among the player base at the time.

Several months after its reveal, the 20120722-24 osu! release officially implemented the system to fully replace the old [Ranked](/wiki/Beatmaps#ranked) score system, with new scores being calculated every 30 minutes. Later on in August of the same year, the system was improved to update in real-time.

*Note: ppv1, the original build of the Performance Points system also had a changelog, which you may view from its [forum topic](https://osu.ppy.sh/community/forums/topics/92185).*

It continued to exist in this capacity for more than a year of service, until [Tom94](https://osu.ppy.sh/users/1857058), the creator of the *osu!tp* scoring metric, joined the [osu! team](/wiki/People/The_Team) and implemented his design into the system. The resulting system was titled *ppv2*, and became live on the January 27, 2014. Therfore renaming the old system to *[ppv1](/wiki/Performance_Points/ppv1)*

ppv2 is currently in active service, with live updates published to its [changelog](https://osu.ppy.sh/p/changelog?category=pp).

## Calculation

Performance points are heavily based on calculated beatmap difficulty, which is determined by a unique algorithm constructed for each individual [game mode](/wiki/Game_Modes).

The difficulty of the beatmap a player is playing on determines the end pp value of their score. By design, the formula relies on four core values: **aim**, **speed**, **accuracy**, and **strain**.These core values are then combined in varying magnitudes to produce an overall score that relates to a beatmap's particular [difficulty](/wiki/Difficulties), and a player's individual performance in said beatmap.

Scores are then "weighted" against each other to ensure that only the best scores a user makes count the most towards their overall performance points ranking. Known as the [*weightage system*](#weightage-system), its goal is to prevent the rapid and repeated gaining of lower pp scores on easy beatmaps by reducing the amount of pp that is actually gained based on the player's other top scores.

*Note: A small amount of bonus pp is awarded based on the number of Ranked maps you have set a score on.*

### Weightage system

The weightage system is a simple formula used after the calculation of the full amount of performance points a play is worth. The formula is used to reduce the amount of pp that is gained based on said play's placing in the player's top scores. The aforementioned formula is as follows: 

`Total pp = p * 0.95^(n-1)` <!-- may want a graphic representation here? (instead of code block) -->

Regarding the formula above, *p* represents each score's full pp value (pre-weighting), and *n* is the placing in the player's `Best Performance` ranking. For example, if a players top 5 scores were 110pp, 100pp, 100pp, 90pp, and 80pp, then the weighted scores would be approximately 110pp, 95pp, 90pp, 77pp, and 65pp. <!-- n's description is pretty awkward here /shrug -->

### Aim

Aim is a core value that considers how difficult it is to consistently hit consecutive notes in a beatmap.

Elements like [approach rate (AR)](/wiki/Beatmapping/Approach_rate) and certain [mods](/wiki/Game_Modifiers) (namely [Flashlight](/wiki/Game_Modifiers#flashlight), [Hidden](/wiki/Game_Modifiers#hidden) and [Hard Rock](/wiki/Game_Modifiers#hard-rock)) make aiming significantly more difficult, and thus influence the amount of pp a score gives.

In the case of [osu!standard](/wiki/Game_Modes/osu!) beatmaps with very large jumps are considered to be "high-aim" maps, and are thus often given very high pp scores. Beatmaps with lots of hyperdashing in [osu!catch](/wiki/Game_Modes/osu!catch) will be considered similarly.

Aim is not considered in gamemodes like [osu!taiko](/wiki/Game_Modes/osu!taiko) and [osu!mania](/wiki/Game_Modes/osu!mania).

### Speed

**Speed is considered the rate at which a beatmap presents elements for a play.**

Beatmaps with high numbers of hit objects in a short period of time are considered to have very high speed values. In this aspect, the faster a beatmap's speed is, the more difficult said beatmap is. Thus granting larger gains of pp.

Mods like [Double Time](/wiki/Game_Modifiers/Half-Time) and [Half Time](/wiki/Game_Modifiers#Half-Time) significantly affect the speed of a beatmap as considered by the performance points algorithm. Likewise, they also significantly affect pp gains when used.

<!-- A "see also" or some other sort of hatnote for the--potential--pp farm stub -->

### Accuracy

*See also: [Accuracy](/wiki/Accuracy)

**Accuracy is considered as your individual performance and consistency in hitting objects within their designated timeframe.**

Highly accurate scores are considered to be very skillful and impressive by the performance points algorithm and will award very large scores compared to scores that are not as accurate. For example, a score set with 80% accuracy is sometimes worth 2/3 of a score set with 95% accuracy. 

Mods like Hidden, Hard Rock and Flashlight are considered to significantly increase how difficult it is to attain an accurate score on a beatmap.

### Strain

**Strain is considered as how many times and for how long a player is subjected to high intensity sections within a particular beatmap.**

Sections or bursts of extremely high speed or difficulty [patterning](/wiki/Beatmaps/Pattern) in a beatmap will massively increase its considered strain values.

Beatmaps with high strain values are considered to be extremely difficult, thus they award very large sums of performance points if surmounted by a player's skill.

### How aim, speed, accuracy and strain combine to produce a pp score

**All four elements are considered in concert to determine how difficult a map is overall and how a particular score compares to what is considered the "optimal" play for that beatmap.**

*Note: The algorithm for performance points varies significantly depending on game mode.*

While the exact numbers are well beyond the scope of this article, certain game modes place greater precedence on certain statistics due to their individual mechanics (e.g., accuracy in osu!taiko vs. accuracy in osu!catch). It is generally reccomended that players try to do their best on a certain beatmap; a play with really good values in one area, but really bad values in others will still not gain a favorable amount of pp. 

Many seasoned osu!standard players understand the pp system intuitively through the help of general experience, mods, and bots like [Tillerino](https://osu.ppy.sh/users/2070907). Experimenting with mods and different "types" of beatmap styles grants a level of understanding that plain text cannot.

## FAQ

### Where can I view the performance ranking?

**The performance points ranking for all players can be found on the [rankings page](https://osu.ppy.sh/p/pp).**

You can also navigate to the rankings by using the `ranking` dropdown panel at the top of the legacy web design, and choosing the `performance` option.

### How can I increase my rank and overall pp?

**Your performance is ranked predominately based on your scores on individual maps.**

The best way to improve is to work at getting good scores on difficult maps or playing a wide variety of beatmaps.

Consider the following tips:

- Play efficiently and figure out which play style works best for you.
- Focus on getting a handful of exceptional scores instead of "farming" hundreds of just okay scores. <!-- "farming" will need to be linked once a stub or section is created -->
- Aim to improve your accuracy. Even 1% makes a massive difference.
- Aim for higher combos. Full combos (FC) or [SS](/wiki/Glossary#grade) scores give tremendous amounts of score.

### Why didn't I gain the full amount of pp from a map I played?

**Performance points use a weighted system, which means that your highest score ever will give 100% of its total pp, and every score you make after that will give gradually less.**

You can learn more about the weightage system [above](#weightage-system)

### How much bonus pp is awarded for having lots of scores on ranked maps?

**Up to 416.6667 bonus pp is given for setting large numbers of scores. This is attained at approximately 25397 scores.**

You can calculate the exact amount of this bonus by following this formula, where `N` is the number of ranked maps with a score set:

`416.6667 * (1 - 0.9994 ^ N)`.

The median number of scores required to reach half of this bonus is roughly 1155 scores. As you can see, the amount of scores required spikes sharply towards the upper end of the spectrum.

#### Is weighting the reason behind why I don't get any pp from playing easy maps any more?

**As above, older scores will eventually be weighted for less than a single percent of their total value. This means they will eventually contribute almost nothing to your total score as you improve.**

At that point however, you would've set some comparatively more impressive scores, meaning that your pp will be higher overall as the higher scores you have set outweigh the older ones.

### Why did I lose pp for setting a new score?

**You might occasionally lose pp for setting a higher combo score with worse accuracy, or playing with mods with worse accuracy overall.**

Total score is still important to individual map rankings, and this may produce unusual circumstances where a higher overall score with lower accuracy or mod use factored in will produce a "better" result that still ultimately loses you pp.

### Some mods feel very overweighted/underweighted. Why is this?

**This is a matter of opinion more than anything else.**

No system is completely perfect, and performance point totals will certainly vary between mapsets and certain mod combinations, even when the subjective difficulty of those plays may be lower than a more difficult map.

Overall, the current performance points system has been engineered to be as fair as possible under the constraints of its model.
