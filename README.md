# RegionTrigger for TShock

RegionTrigger is a **TShock-based** plugin aimed to trigger special events when players enter a region.

> 本插件有中文版本! 查看[中文教程][cn].. [下载链接][cndown]..

## Requirement:
- API Version: 2.0
- TShock Version: 4.3.22

## Commands:
- `/rt set-<property> <region> [--del] <value>` -- *Sets regions*
>  ### Available properties:
>  - Event: `event(e)`
>  - Bans: `projban(pb), itemban(ib), tileban(tb)`
>  - Messages: `entermsg(em), leavemsg(lm), messageinterval(msgitv/mi)`
>  - Group: `tempgroup(tg)`

  **e.g.** `/rt set-event main-region nopvp`
          ` /rt set-tempgroup main-region admin`
  
- `/rt show <region>` -- *Gets information about a specific region*
- `/rt reload` -- *Reloads data in database*
- `/rt --help [page]` -- *Gets helps*

You can also find this plugin in [TShock offical forum][tshockco].

## Permission
- `regiontrigger.manage` -- *Manages regions' events.*
- `regiontrigger.bypass.tileban` -- *Use banned tiles in regions.*
- `regiontrigger.bypass.projban` -- *Use banned projectiles in regions.*
- `regiontrigger.bypass.itemban` -- *Use banned items in regions.*
- `regiontrigger.bypass.tempgroup` -- *Player won't be switched to tempgroup.*
- `regiontrigger.bypass.pvp` -- *Players will be able to toggle their PvP status.*
- `regiontrigger.bypass.nopvp` -- *Players will be able to toggle their PvP status.*
- `regiontrigger.bypass.private` -- *Enters private regions.*
- `regiontrigger.bypass.tempperm` -- *Skip temp permissions in region.*

## Available events now:
- `EnterMsg` - *Sends player a specific message when entering regions.*
- `LeaveMsg` - *Sends player a specific message when leaving regions.*
- `Message` - *Sends player in regions a specific message.*
- `TempGroup` - *Alters players' tempgroups when they are in regions.*
- `Itemban` - *Disallows players in specific regions from using banned items.*
- `Projban` - *Disallows players in specific regions from using banned projectiles.*
- `Tileban` - *Disallows players in specific regions from using banned tiles.*
- `Kill` - *Kills players entering to region.*
- `Godmode` - *Turns players' godmode on when they are in regions.*
- `Pvp` - *Turns players' PvP status on when they are in regions.*
- `NoPvp` - *Disallows players from enabling their PvP mode.*
- `InvariantPvp` - *Disallows players from changing their pvp mode.*
- `Private` - *Disallows players without permission from entering region.*

   [tshockco]: <https://tshock.co/xf/index.php?resources/regiontrigger.157/>
   [cn]: <https://github.com/mistzzt/RegionTrigger/blob/cn/README.md>
   [cndown]: <https://github.com/mistzzt/RegionTrigger/releases>

## Overview
### Commands:
- /rt set-<property> <region> [--del] <value> -- Sets regions
- /rt show <region> -- Gets information about a specific region
- /rt reload -- Reloads data in database
- /rt --help [page] -- Gets helps
 
**Available properties:**
1. Event: event(e)
2. Bans: projban(pb), itemban(ib), tileban(tb)
3. Messages: entermsg(em), leavemsg(lm), messageinterval(msgitv/mi)
4. Group: tempgroup(tg)

**e.g.** 
- `/rt set-event main-region nopvp`
- `/rt set-tempgroup main-region vip`

 ### Example: How to add a message(5 seconds per sending) in region
1. Use `/region` to define a region. And here I defined a region named main.
2. Use `/rt set-event main message` , which adds event **message** to region **main**. Now, when players enter the region, they will receive a default message.
3. Use `/rt set-message main Welcome to our region!` , which sets the region's property **message** to **"Welcome to our region!"**. Now, players entering region main will receive the message.
4. Use `/rt set-mi(MessageInterval) message main 5` , which sets the **interval** to **5 seconds**. 
5. Now, players in this region will receive the message every five seconds.

**Available Events (New events will be added in upcoming versions):**
- EnterMsg - Sends player a specific message when entering regions.
- LeaveMsg - Sends player a specific message when leaving regions.
- Message - Sends player in regions a specific message.
- TempGroup - Alters players' tempgroups when they are in regions.
- Itemban - Disallows players in specific regions from using banned items.
- Projban - Disallows players in specific regions from using banned projectiles.
- Tileban - Disallows players in specific regions from using banned tiles.
- Kill - Kills players entering to region.
- Godmode - Turns players' godmode on when they are in regions.
- Pvp - Turns players' PvP status on when they are in regions.
- NoPvp - Disallows players from enabling their PvP mode.
- InvariantPvp - Disallows players from changing their pvp mode.
- Private - Disallows players without permission from entering region.

## Permissions
- regiontrigger.manage -- Manages regions' events.
- regiontrigger.bypass.tileban -- Use banned tiles in regions.
- regiontrigger.bypass.projban -- Use banned projectiles in regions.
- regiontrigger.bypass.itemban -- Use banned items in regions.
- regiontrigger.bypass.tempgroup -- Player won't be switched to tempgroup.
- regiontrigger.bypass.pvp -- Player will be able to toggle his PvP status.
- regiontrigger.bypass.nopvp -- Player will be able to toggle his PvP status.
- regiontrigger.bypass.private -- Enters private regions. 

## Installation Guide
1. Download RegionTrigger.dll to the ServerPlugins folder and restart TShock if running. 

## Source
[RegionTrigger | TShock for Terraria](https://tshock.co/xf/index.php?resources/regiontrigger.157/)
