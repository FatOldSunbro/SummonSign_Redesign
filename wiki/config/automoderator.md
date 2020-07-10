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
~title (regex): ["ps4", "xbox", "xbone", "xb(ox)?1", "pc", "steam", "ps3", "switch"]
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
set_flair:
    text: Help Me!
    css_class: help-me-ps4
    template_id: 7e08ee68-10d4-11e6-b252-0e761361da27

---

type: submission
title (regex): ["((pc|steam)(.*)help|help(.*)(pc|steam))"]
set_flair:
    text: Help Me!
    css_class: help-me-steam
    template_id: 85941c70-10d4-11e6-9bed-0e1e1ee7abbb

---

type: submission
title (regex): ["((xbox|xbox1|xbone)(.*)help|help(.*)(xbox|xb(ox)?1|xbone))"]
set_flair:
    text: Help Me!
    css_class: help-me-xbox
    template_id: 8bda4208-10d4-11e6-8ffe-0ecc83f85b2b

---

type: submission
title (regex): ["(ps3(.*)help|help(.*)ps3)"]
set_flair:
    text: Help Me!
    css_class: help-me-ps3
    template_id: 910d3708-10d4-11e6-9bed-0e1e1ee7abbb

---

type: submission
title (regex): ["(switch(.*)help|help(.*)switch)"]
set_flair:
    text: Help Me!
    css_class: help-me-ps4
    template_id: 98377df4-10d4-11e6-b9d0-0eb66bc8b02f

---

type: submission
title (regex): ["(ps4(.*)summon|summon(.*)ps4)"]
set_flair:
    text: Summon Me!
    css_class: summon-me-ps4
    template_id: 9d8fb41a-10d4-11e6-bb10-0e5c663c2313

---

type: submission
title (regex): ["((pc|steam)(.*)summon|summon(.*)(pc|steam))"]
set_flair:
    text: Summon Me!
    css_class: summon-me-steam
    template_id: a27cf4f6-10d4-11e6-a99e-0e3eeff20e29

---

type: submission
title (regex): ["((xbox|xbox1|xbone)(.*)summon|summon(.*)(xbox|xb(ox)?1|xbone))"]
set_flair:
    text: Summon Me!
    css_class: summon-me-xbox
    template_id: a7aebc20-10d4-11e6-8151-0e462b3a24fb

---

type: submission
title (regex): ["(ps3(.*)summon|summon(.*)ps3)"]
set_flair:
    text: Summon Me!
    css_class: summon-me-ps4
    template_id: af1ae466-10d4-11e6-8cbd-0e1e1ee7abbb

---

type: submission
title (regex): ["(switch(.*)summon|summon(.*)switch)"]
set_flair:
    text: Summon Me!
    css_class: summon-me-switch
    template_id: d5689590-97f3-11e6-9f6a-0e985c31f9b0

---

type: submission
title (regex): ["(ps4(.*)co-?op|co-?op(.*)ps4)"]
set_flair:
    text: Co-op with Me!
    css_class: coop-ps4
    template_id: ea1091aa-97f3-11e6-a160-0e7eefd57056

---

type: submission
title (regex): ["((pc|steam)(.*)co-?op|co-?op(.*)(pc|steam))"]
set_flair:
    text: Co-op with Me!
    css_class: coop-steam
    template_id: f0a7871c-97f3-11e6-ae07-0e985c31f9b0

---

type: submission
title (regex): ["((xbox|xbox1|xbone)(.*)co-?op|co-?op(.*)(xbox|xb(ox)?1|xbone))"]
set_flair:
    text: Co-op with Me!
    css_class: coop-xbox
    template_id: 4668aaae-d551-11e8-b7b4-0e8d2f93592c

---

type: submission
title (regex): ["(ps3(.*)co-?op|co-?op(.*)ps3)"]
set_flair:
    text: Co-op with Me!
    css_class: coop-ps3
    template_id: 51729266-d551-11e8-89be-0e856c2f8d14

---

type: submission
title (regex): ["(switch(.*)co-?op|co-?op(.*)switch)"]
set_flair:
    text: Co-op with Me!
    css_class: coop-switch
    template_id: 5a57d3e6-d551-11e8-8cde-0ed4b8f6e992

---

type: submission
title (regex): ["(ps4(.*)pvp|pvp(.*)ps4)"]
set_flair:
    text: Fight Me!
    css_class: arena-ps4
    template_id: 6cf67fac-d551-11e8-98f2-0edce2a7e600

---

type: submission
title (regex): ["((pc|steam)(.*)pvp|pvp(.*)(pc|steam))"]
set_flair:
    text: Fight Me!
    css_class: arena-steam
    template_id: 77528950-d551-11e8-b954-0ea613d466fc

---

type: submission
title (regex): ["((xbox|xbox1|xbone)(.*)pvp|pvp(.*)(xbox|xb(ox)?1|xbone))"]
set_flair:
    text: Fight Me!
    css_class: arena-xbox
    template_id: 7f9b42dc-d551-11e8-ad02-0eb636c8d21a

---

type: submission
title (regex): ["(ps3(.*)pvp|pvp(.*)ps3)"]
set_flair:
    text: Fight Me!
    css_class: arena-ps3
    template_id: 885a2992-d551-11e8-8dc0-0e1a71db19ac

---

type: submission
title (regex): ["(switch(.*)pvp|pvp(.*)switch)"]
set_flair:
    text: Fight Me!
    css_class: arena-switch
    template_id: 8c07df9e-d551-11e8-990a-0e453627aeb0

---

    author: [gaynibba9090, ChungusEater420, Gigi0505, SPambot67, slavknightgayl12, S0ur68w, BonfireFodder, Reb_Eye_Stone, Shweep80, mlugo808, datboy2006, KMACS4769, oldenspace, MinMaxxingGoon, Zelyyx, really_special_spam, datboi_216, Loud-Quarter, TheRightous335, Hypixelizdead, Abyssal_Paladin, TobiasNH, Phypur, Timageness]
    action: remove
    
---
   
   # Auto-remove offensive words or phrases - silently nuke them forever
    title+body (regex): ["(f|ph)agg?[eio0]?t?s?(ry)?", "nigg(a|er)s?", "dykes?", "homos?", "autis[mt](ic)?", "retard(s|ed)", "na?zi?", "卐", "rape(d)?", "fgt", "dexfag", "kike?"]
    action: remove
    modmail: |
        The above {{kind}} by /u/{{author}} in /r/{{subreddit}} has been removed due to banned words or phrases. The word was: {{match-1}}
