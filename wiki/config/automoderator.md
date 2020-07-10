## Auto-remove posts that do not meet formatting guidelines

# check for request type 
type: submission
~title (regex): ["help", "summon", "co-?op", "pvp"]
action: remove
#modmail: |
#    The above {{kind}} by /u/{{author}} in /r/{{subreddit}} has been removed as it does not contain a type.
comment: |
    Hi, Your post has been automatically removed as it does not meet our formatting guidelines

    > You must include the type of submission, one of either Help, Summon, Co-op or PvP

    > e.g., [*Help*][PS4][100] Abyss Watchers

    Please re-submit with the correct formatting. Thanks!

---

# check for platform 
type: submission
~title (regex): ["ps4", "xbox", "xbone", "xb(ox)?1", "pc", "steam", "ps3", 'switch']
action: remove
#modmail: |
#    The above {{kind}} by /u/{{author}} in /r/{{subreddit}} has been removed as it does not contain a platform.
comment: |
    Hi, Your post has been automatically removed as it does not meet our formatting guidelines

    > You must include your platform, one of either PS4, PC/Steam, switch, or Xbox/Xbone/Xbox1

    > e.g., [Help][*PS4*][100] Abyss Watchers

    Please re-submit with the correct formatting. Thanks!

---

# tag submissions
type: submission
title (regex): ["(ps4(.*)help|help(.*)ps4)"]
set_flair: ["Help Me!", "help-me-ps4"]

---

type: submission
title (regex): ["((pc|steam)(.*)help|help(.*)(pc|steam))"]
set_flair: ["Help Me!", "help-me-steam"]

---

type: submission
title (regex): ["((xbox|xbox1|xbone)(.*)help|help(.*)(xbox|xb(ox)?1|xbone))"]
set_flair: ["Help Me!", "help-me-xbox"]

---

type: submission
title (regex): ["(ps3(.*)help|help(.*)ps3)"]
set_flair: ["Help Me!", "help-me-ps3"]

---

type: submission
title (regex): ["(switch(.*)help|help(.*)switch)"]
set_flair: ["Help Me!", "help-me-ps4"]

---

type: submission
title (regex): ["(ps4(.*)summon|summon(.*)ps4)"]
set_flair: ["Summon Me!", "summon-me-ps4"]

---

type: submission
title (regex): ["((pc|steam)(.*)summon|summon(.*)(pc|steam))"]
set_flair: ["Summon Me!", "summon-me-steam"]

---

type: submission
title (regex): ["((xbox|xbox1|xbone)(.*)summon|summon(.*)(xbox|xb(ox)?1|xbone))"]
set_flair: ["Summon Me!", "summon-me-xbox"]

---

type: submission
title (regex): ["(ps3(.*)summon|summon(.*)ps3)"]
set_flair: ["Summon Me!", "summon-me-ps4"]

---

type: submission
title (regex): ["(switch(.*)summon|summon(.*)switch)"]
set_flair: ["Summon Me!", "summon-me-switch"]

---

type: submission
title (regex): ["(ps4(.*)co-?op|co-?op(.*)ps4)"]
set_flair: ["Co-op with Me!", "coop-ps4"]

---

type: submission
title (regex): ["((pc|steam)(.*)co-?op|co-?op(.*)(pc|steam))"]
set_flair: ["Co-op with Me!", "coop-steam"]

---

type: submission
title (regex): ["((xbox|xbox1|xbone)(.*)co-?op|co-?op(.*)(xbox|xb(ox)?1|xbone))"]
set_flair: ["Co-op with Me!", "coop-xbox"]

---

type: submission
title (regex): ["(ps3(.*)co-?op|co-?op(.*)ps3)"]
set_flair: ["Co-op with Me!", "coop-ps3"]

---

type: submission
title (regex): ["(switch(.*)co-?op|co-?op(.*)switch)"]
set_flair: ["Co-op with Me!", "coop-switch"]

---

type: submission
title (regex): ["(ps4(.*)pvp|pvp(.*)ps4)"]
set_flair: ["Fight Me!", "arena-ps4"]

---

type: submission
title (regex): ["((pc|steam)(.*)pvp|pvp(.*)(pc|steam))"]
set_flair: ["Fight Me!", "arena-steam"]

---

type: submission
title (regex): ["((xbox|xbox1|xbone)(.*)pvp|pvp(.*)(xbox|xb(ox)?1|xbone))"]
set_flair: ["Fight Me!", "arena-xbox"]

---

type: submission
title (regex): ["(ps3(.*)pvp|pvp(.*)ps3)"]
set_flair: ["Fight Me!", "arena-ps3"]

---

type: submission
title (regex): ["(switch(.*)pvp|pvp(.*)switch)"]
set_flair: ["Fight Me!", "arena-switch"]

---

    author: [gaynibba9090, ChungusEater420, Gigi0505, SPambot67, slavknightgayl12, S0ur68w, BonfireFodder, Reb_Eye_Stone, Shweep80, mlugo808, datboy2006, KMACS4769, oldenspace, MinMaxxingGoon, Zelyyx, really_special_spam, datboi_216, Loud-Quarter, TheRightous335, Hypixelizdead, Abyssal_Paladin, TobiasNH, Phypur, Timageness]
    action: remove
    
---
   
   # Auto-remove offensive words or phrases - silently nuke them forever
    title+body (regex): ["(f|ph)agg?[eio0]?t?s?(ry)?", "nigg(a|er)s?", "dykes?", "homos?", "autis[mt](ic)?", "retard(s|ed)", "na?zi?", "卐", "rape(d)?", "fgt", "dexfag", "kike?"]
    action: remove
    modmail: |
        The above {{kind}} by /u/{{author}} in /r/{{subreddit}} has been removed due to banned words or phrases. The word was: {{match-1}}
