# AutomoDerator config file

---

# Section 1 - Auto-remove posts that do not meet formatting guidelines / Title Control

---

### check for request type 
type: submission
~title (regex): ["help", "summon", "co-?op", "pvp"]
action: remove
action_reason: "missing request type in the title."
comment: |
    Hello there, your post has been automatically removed as it is missing [*request type*] in the title and so it does not meet our formatting guidelines:

    > You must include in the **title** the [*request type*] **and** your [*platform*].

    > e.g., [*Help*][*PS4*][DS3] Darkeater Midir

    ### Accepted values for [*request type*] and [*platform*], one of either:
    Request type | and | Platform
    :---:|:---:|:----:
    Help | - | PS5/PS4/PS3
    Summon | - | RPCS3/PC
    Co-op | - | XBX/Xbox/Xbone/Xbox360
    PvP | - | Switch

    Please re-submit with the correct formatting. Thanks!
comment_stickied: true

---

### check for platform 
type: submission
~title (regex): ["ps5", "ps4", "ps3", "rpcs3", "pc", "steam", "xbx", "xbs", "xbox(360)?", "xboxone", "xbone", "xb(ox)?1", "switch"]
action: remove
action_reason: "missing platform in the title."
comment: |
    Hello there, your post has been automatically removed as it is missing [*platform*] in the title and so it does not meet our formatting guidelines:

    > You must include in the **title** the [*request type*] **and** your [*platform*].

    > e.g., [*Help*][*PS4*][DS3] Darkeater Midir

    ### Accepted values for [*request type*] and [*platform*], one of either:
    Request type | and | Platform
    :---:|:---:|:----:
    Help | - | PS5/PS4/PS3
    Summon | - | RPCS3/PC
    Co-op | - | XBX/Xbox/Xbone/Xbox360
    PvP | - | Switch

    Please re-submit with the correct formatting. Thanks!
comment_stickied: true

---

### Redirect trading posts
type: submission
title (regex): ["dropping", "duping", "mule", "mulling", "transfer(s)?", "trade(s)?"]
action: remove
action_reason: "submission about trading items."
# modmail: |
#    The above {{kind}} by /u/{{author}} in /r/{{subreddit}} has been removed as it appears to be a trade post, please investigate.
comment: |
    Hello there, your post has been automatically removed as it does not meet this subreddit rules.

    It appears that this post is about trading items, please use the correct subreddit for trading items:

    * For Dark Souls and Dark Souls Remastered use r/snuggly

    * For Dark Souls 2 use r/wheelanddeal

    * For Dark Souls 3 use r/pumparum

    * For Demon Souls use r/twinkly

    Please re-submit in the correct subreddit. Thanks!

    ---
    If this action was mistakenly performed please [contact the moderators](https://www.reddit.com/message/compose?to=%2Fr%2FSummonSign&subject=&message=)
comment_stickied: true

---

### Possible trade, item begging alarm
type: submission
title (regex): ["item(s)?"]
# action: remove
# action_reason: "submission about trading items."
# modmail: |
#    The above {{kind}} by /u/{{author}} in /r/{{subreddit}} has been removed as it appears to be a trade post, please investigate.
modmail: |
    Full text: {{body}}

    /u/{{author}} posted a {{kind}} (containing the word **[{{match-1}}]**) in /r/{{subreddit}}.
    
    Verify this action.

---

# Section 2 - Set post flairs

---

### Change flair to Duty fulfilled based on comment
type: comment
body: ["+complete"]
is_top_level: true
author:
    is_submitter: true
parent_submission:
    set_flair:
        text: ":sunbro: Duty Fulfilled!"
        css_class: duty-fulfilled
        template_id: 25213842-1029-11e6-ba76-0ecc83f85b2b
    overwrite_flair: true
comment: |
    /u/{{author}} you have successfully changed your [submission's]({{permalink}}) flair to Duty Fulfilled!

---

### Warning message for user without apropriate permission
type: comment
body: ["+complete"]
is_top_level: true
author:
    is_submitter: false
comment: |
    /u/{{author}} is not in the sudoers file. This incident will be reported!! (´・＿・`)

---

### PLAYSTATION 5 TAGS
type: submission
title (regex): ["(ps5(.*)help|help(.*)ps5)"]
set_flair:
    text: ":psx: Help Me!"
    css_class: help-me-ps4
    template_id: 7e08ee68-10d4-11e6-b252-0e761361da27
overwrite_flair: true

---

type: submission
title (regex): ["(ps5(.*)summon|summon(.*)ps5)"]
set_flair:
    text: ":psx: Summon Me!"
    css_class: summon-me-ps4
    template_id: 9d8fb41a-10d4-11e6-bb10-0e5c663c2313
overwrite_flair: true
priority: -1

---

type: submission
title (regex): ["(ps5(.*)co-?op|co-?op(.*)ps5)"]
set_flair:
    text: ":psx: Co-op with Me!"
    css_class: coop-ps4
    template_id: ea1091aa-97f3-11e6-a160-0e7eefd57056
overwrite_flair: true

---

type: submission
title (regex): ["(ps5(.*)pvp|pvp(.*)ps5)"]
set_flair:
    text: ":psx: Fight Me!"
    css_class: arena-ps4
    template_id: 6cf67fac-d551-11e8-98f2-0edce2a7e600
overwrite_flair: true

---

### PLAYSTATION 4 TAGS
type: submission
title (regex): ["(ps4(.*)help|help(.*)ps4)"]
set_flair:
    text: ":psx: Help Me!"
    css_class: help-me-ps4
    template_id: 7e08ee68-10d4-11e6-b252-0e761361da27
overwrite_flair: true

---

type: submission
title (regex): ["(ps4(.*)summon|summon(.*)ps4)"]
set_flair:
    text: ":psx: Summon Me!"
    css_class: summon-me-ps4
    template_id: 9d8fb41a-10d4-11e6-bb10-0e5c663c2313
overwrite_flair: true
priority: -1

---

type: submission
title (regex): ["(ps4(.*)co-?op|co-?op(.*)ps4)"]
set_flair:
    text: ":psx: Co-op with Me!"
    css_class: coop-ps4
    template_id: ea1091aa-97f3-11e6-a160-0e7eefd57056
overwrite_flair: true

---

type: submission
title (regex): ["(ps4(.*)pvp|pvp(.*)ps4)"]
set_flair:
    text: ":psx: Fight Me!"
    css_class: arena-ps4
    template_id: 6cf67fac-d551-11e8-98f2-0edce2a7e600
overwrite_flair: true

---

### PLAYSTATION 3 TAGS
type: submission
title (regex): ["(ps3(.*)help|help(.*)ps3)"]
set_flair:
    text: ":psx: Help Me!"
    css_class: help-me-ps4
    template_id: 7e08ee68-10d4-11e6-b252-0e761361da27
overwrite_flair: true

---

type: submission
title (regex): ["(ps3(.*)summon|summon(.*)ps3)"]
set_flair:
    text: ":psx: Summon Me!"
    css_class: summon-me-ps4
    template_id: 9d8fb41a-10d4-11e6-bb10-0e5c663c2313
overwrite_flair: true
priority: -1

---

type: submission
title (regex): ["(ps3(.*)co-?op|co-?op(.*)ps3)"]
set_flair:
    text: ":psx: Co-op with Me!"
    css_class: coop-ps4
    template_id: ea1091aa-97f3-11e6-a160-0e7eefd57056
overwrite_flair: true

---

type: submission
title (regex): ["(ps3(.*)pvp|pvp(.*)ps3)"]
set_flair:
    text: ":psx: Fight Me!"
    css_class: arena-ps4
    template_id: 6cf67fac-d551-11e8-98f2-0edce2a7e600
overwrite_flair: true

---

### RPCS3 (PS3 emulation software)
type: submission
title (regex): ["(rpcs3(.*)help|help(.*)rpcs3)"]
set_flair:
    text: ":pc: Help Me!"
    css_class: help-me-steam
    template_id: 85941c70-10d4-11e6-9bed-0e1e1ee7abbb
overwrite_flair: true

---

type: submission
title (regex): ["(rpcs3(.*)summon|summon(.*)rpcs3)"]
set_flair:
    text: ":pc: Summon Me!"
    css_class: summon-me-steam
    template_id: a27cf4f6-10d4-11e6-a99e-0e3eeff20e29
overwrite_flair: true
priority: -1

---

type: submission
title (regex): ["(rpcs3(.*)co-?op|co-?op(.*)rpcs3)"]
set_flair:
    text: ":pc: Co-op with Me!"
    css_class: coop-steam
    template_id: f0a7871c-97f3-11e6-ae07-0e985c31f9b0
overwrite_flair: true

---

type: submission
title (regex): ["(rpcs3(.*)pvp|pvp(.*)rpcs3)"]
set_flair:
    text: ":pc: Fight Me!"
    css_class: arena-steam
    template_id: 77528950-d551-11e8-b954-0ea613d466fc
overwrite_flair: true

---

### PC STEAM TAGS
type: submission
title (regex): ["((pc|steam)(.*)help|help(.*)(pc|steam))"]
set_flair:
    text: ":pc: Help Me!"
    css_class: help-me-steam
    template_id: 85941c70-10d4-11e6-9bed-0e1e1ee7abbb
overwrite_flair: true

---

type: submission
title (regex): ["((pc|steam)(.*)summon|summon(.*)(pc|steam))"]
set_flair:
    text: ":pc: Summon Me!"
    css_class: summon-me-steam
    template_id: a27cf4f6-10d4-11e6-a99e-0e3eeff20e29
overwrite_flair: true
priority: -1

---

type: submission
title (regex): ["((pc|steam)(.*)co-?op|co-?op(.*)(pc|steam))"]
set_flair:
    text: ":pc: Co-op with Me!"
    css_class: coop-steam
    template_id: f0a7871c-97f3-11e6-ae07-0e985c31f9b0
overwrite_flair: true

---

type: submission
title (regex): ["((pc|steam)(.*)pvp|pvp(.*)(pc|steam))"]
set_flair:
    text: ":pc: Fight Me!"
    css_class: arena-steam
    template_id: 77528950-d551-11e8-b954-0ea613d466fc
overwrite_flair: true

---
### XBOX SERIES X/S TAGS
type: submission
title (regex): ["((xbx|xbs)(.*)help|help(.*)(xbx|xbs))"]
set_flair:
    text: ":xbox: Help Me!"
    css_class: help-me-xbox
    template_id: 8bda4208-10d4-11e6-8ffe-0ecc83f85b2b
overwrite_flair: true

---

type: submission
title (regex): ["((xbx|xbs)(.*)summon|summon(.*)(xbx|xbs))"]
set_flair:
    text: ":xbox: Summon Me!"
    css_class: summon-me-xbox
    template_id: a7aebc20-10d4-11e6-8151-0e462b3a24fb
overwrite_flair: true
priority: -1

---

type: submission
title (regex): ["((xbx|xbs)(.*)co-?op|co-?op(.*)(xbx|xbs))"]
set_flair:
    text: ":xbox: Co-op with Me!"
    css_class: coop-xbox
    template_id: 4668aaae-d551-11e8-b7b4-0e8d2f93592c
overwrite_flair: true

---

type: submission
title (regex): ["((xbx|xbs)(.*)pvp|pvp(.*)(xbx|xbs))"]
set_flair:
    text: ":xbox: Fight Me!"
    css_class: arena-xbox
    template_id: 7f9b42dc-d551-11e8-ad02-0eb636c8d21a
overwrite_flair: true

---

### XBOX ONE TAGS
type: submission
title (regex): ["((xbox|xb(ox)?1|xbone|xboxone)(.*)help|help(.*)(xbox|xb(ox)?1|xbone|xboxone))"]
set_flair:
    text: ":xbox: Help Me!"
    css_class: help-me-xbox
    template_id: 8bda4208-10d4-11e6-8ffe-0ecc83f85b2b
overwrite_flair: true

---

type: submission
title (regex): ["((xbox|xb(ox)?1|xbone|xboxone)(.*)summon|summon(.*)(xbox|xb(ox)?1|xbone|xboxone))"]
set_flair:
    text: ":xbox: Summon Me!"
    css_class: summon-me-xbox
    template_id: a7aebc20-10d4-11e6-8151-0e462b3a24fb
overwrite_flair: true
priority: -1

---

type: submission
title (regex): ["((xbox|xb(ox)?1|xbone|xboxone)(.*)co-?op|co-?op(.*)(xbox|xb(ox)?1|xbone|xboxone))"]
set_flair:
    text: ":xbox: Co-op with Me!"
    css_class: coop-xbox
    template_id: 4668aaae-d551-11e8-b7b4-0e8d2f93592c
overwrite_flair: true

---

type: submission
title (regex): ["((xbox|xb(ox)?1|xbone|xboxone)(.*)pvp|pvp(.*)(xbox|xb(ox)?1|xbone|xboxone))"]
set_flair:
    text: ":xbox: Fight Me!"
    css_class: arena-xbox
    template_id: 7f9b42dc-d551-11e8-ad02-0eb636c8d21a
overwrite_flair: true

---

### XBOX360 TAGS
type: submission
title (regex): ["((xbox(360)?)(.*)help|help(.*)(xbox(360)?))"]
set_flair:
    text: ":xbox: Help Me!"
    css_class: help-me-xbox
    template_id: 8bda4208-10d4-11e6-8ffe-0ecc83f85b2b
overwrite_flair: true

---

type: submission
title (regex): ["((xbox(360)?)(.*)summon|summon(.*)(xbox(360)?))"]
set_flair:
    text: ":xbox: Summon Me!"
    css_class: summon-me-xbox
    template_id: a7aebc20-10d4-11e6-8151-0e462b3a24fb
overwrite_flair: true
priority: -1

---

type: submission
title (regex): ["((xbox(360)?)(.*)co-?op|co-?op(.*)(xbox(360)?))"]
set_flair:
    text: ":xbox: Co-op with Me!"
    css_class: coop-xbox
    template_id: 4668aaae-d551-11e8-b7b4-0e8d2f93592c
overwrite_flair: true

---

type: submission
title (regex): ["((xbox(360)?)(.*)pvp|pvp(.*)(xbox(360)?))"]
set_flair:
    text: ":xbox: Fight Me!"
    css_class: arena-xbox
    template_id: 7f9b42dc-d551-11e8-ad02-0eb636c8d21a
overwrite_flair: true

---

### NINTENDO SWITCH TAGS
type: submission
title (regex): ["(switch(.*)help|help(.*)switch)"]
set_flair:
    text: ":switch: Help Me!"
    css_class: help-me-ps4
    template_id: 98377df4-10d4-11e6-b9d0-0eb66bc8b02f
overwrite_flair: true

---

type: submission
title (regex): ["(switch(.*)summon|summon(.*)switch)"]
set_flair:
    text: ":switch: Summon Me!"
    css_class: summon-me-switch
    template_id: d5689590-97f3-11e6-9f6a-0e985c31f9b0
overwrite_flair: true
priority: -1

---

type: submission
title (regex): ["(switch(.*)co-?op|co-?op(.*)switch)"]
set_flair:
    text: ":switch: Co-op with Me!"
    css_class: coop-switch
    template_id: 5a57d3e6-d551-11e8-8cde-0ed4b8f6e992
overwrite_flair: true

---

type: submission
title (regex): ["(switch(.*)pvp|pvp(.*)switch)"]
set_flair:
    text: ":switch: Fight Me!"
    css_class: arena-switch
    template_id: 8c07df9e-d551-11e8-990a-0e453627aeb0
overwrite_flair: true

---

# Section 3 - Security rules

---

# Moderator Alerts

---

### Report modmail
reports: 1
modmail: The above {{kind}} by /u/{{author}} has received 1 report. Please investigate.

---

### Remove reported users
reports: 3
action: remove
action_reason: "reported at least 3 times."
comment: The post was removed for being reported excessively, MODs will look into this matter.
comment_stickied: true
modmail: The above {{kind}} by /u/{{author}} was removed because it received 6 reports. Please investigate and ensure that this action was correct.

---

# Content Quality Control

---

### Hate Speech Filters
### Auto-remove offensive words or phrases - silently nuke them forever
title+body (regex): ["(f|ph)agg?[eio0]?t?s?(ry)?", "nigg(a|er)s?", "dykes?", "homos?", "autis[mt](ic)?", "retard(s|ed)", "na?zi?", "卐", "rape(d)?", "fgt", "dexfag", "kike?", "k[iy]kes?", "trann(y|ie)s?","cocks?([ -]?suck(ers?|ing)?)?","cum(ming|[ -]shots?)?","cunts?", "lesbo", "(fuck|lib|republi)tard(s|ed|(ed)?ness)?", "kill ?yoursel(f|ves?)", "I hope (you die|it dies?|she dies?|he dies?|they die|they all die|you get ebola|she gets ebola|he gets ebola|they get ebola|it gets? Ebola)", " deserve to (die|be shot)", "ging"]
action: remove
action_reason: "offensive content."
modmail: |
    Full text: {{body}}

    /u/{{author}} posted a {{kind}} (containing the word **[{{match-1}}]**) in /r/{{subreddit}}.
    
    That was removed. Verify this action.
message: |
    Your {{kind}} in /r/{{subreddit}} has been automatically removed due to offensive/banned content.
    The word was: {{match-1}} - [Link to your {{kind}}]({{permalink}})

    ---
    [SummonSign Rules](https://www.reddit.com/r/SummonSign/wiki/rules)
message_subject: Your {{kind}} in /r/{{subreddit}} was removed.

---

### Hate Speech Filters
### Remove comments that were reported and contain the following words
reports: 1
body+title (regex): [ "gay", "cuck", "cucks", "trap", "carpet muncher", "camel jockey", "wog", "coon", "heeb", "kraut", "jap(s)", "wop", "beaner", "boong", "chink", "kafir", "kaffir", "raghead", "pikey", "femi-?nazi", "shit[- ]?lord", "dogshit", "a(ss|rse|es)([ -]?holes?)?", "((mother|motha|mutha)[ -]?)?f(u?c?k?k|\\*ck|\\*{0,2}k|\\*{3})(er|ed|ing|s)?", "s(h(i|ar?|\\*)t|\\*{3}|h\\*{2})(s|ter|e|ting)?", "b(i|\\*)o?(tch|\\*{3})(y|es)?" ]
action: remove
action_reason: "Reported and contains offensive content."
modmail: |
    Full text: {{body}}

    /u/{{author}} posted a {{kind}} (containing the word **[{{match-1}}]**) in /r/{{subreddit}}.
    
    That was reported and removed. Verify this action.

---

### Remove posts from forbidden domains
domain: [redgifs.com, webmshare.com, erome.com, pornhub.com, xvideos.com, xhamster.com, youporn.com, redtube.com, tube8.com, porndig.com, imgbb.com, prnt.sc, prntscr.com, tinypic.com, onlyfans.com]
action: remove
action_reason: "not allowed domain."
comment: |
    Your submission was automatically removed because {{domain}} is not an approved site.
comment_stickied: true

---

### Filter out subreddit spam / Comments that are just /r links
title+body (regex): ["r/eyestone"]
action: filter
action_reason: "spam."

---

# User Control

---

### Account karma check
~author: ["aleksa736"]
author:
    combined_karma: "< -50"
action: remove
action_reason: "account karma below -50, possible troll."
comment: |
    Hello {{author}}, your post has been automatically removed as your account is flagged as a troll/bot account. If this was a mistake [contact the moderators](https://www.reddit.com/message/compose?to=%2Fr%2FSummonSign&subject=&message=).

    ---
    Thank you for your understanding and co-operation in creating an enjoyable gaming environment for all.
comment_stickied: true
modmail: The above {{kind}} by /u/{{author}} was removed because it appears to be a troll account. Please investigate and ensure that this action was correct.

---

### Silent remove post from the following users(shadowban):
author: [gaynibba9090, ChungusEater420, Gigi0505, SPambot67, slavknightgayl12, S0ur68w, BonfireFodder, Reb_Eye_Stone, Shweep80, mlugo808, datboy2006, KMACS4769, oldenspace, MinMaxxingGoon, Zelyyx, really_special_spam, datboi_216, Loud-Quarter, TheRightous335, Hypixelizdead, TobiasNH, Phypur, Timageness, Sk8orDie95, IttwasmeDIO, Dirty1forlyf, cumgobiln, AdPsychological1295]
action: remove
action_reason: "user is silenced."

---