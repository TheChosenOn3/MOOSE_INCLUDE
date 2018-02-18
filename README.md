# MOOSE framework

MOOSE is a **M**ission **O**bject **O**riented **S**cripting **E**nvironment, and is meant for mission designers and mission hosters.
It allows to quickly setup complex missions using pre-scripted scenarios using the available classes within the MOOSE Framework.
MOOSE works with DCS world 2.5.
  
  
## MOOSE Framework Goal

The goal of MOOSE is to allow mission designers to **enhance the mission designs** by using **mission orchestration objects**, 
which can be _instantiated_ from defined classes within the framework. 
This will allow to write exciting missions and multi player cooperative operation scenarios. 

Of course, the richness of the framework will determine the richness of the misson scenarios. 
The MOOSE is a service that is produced while being consumed ... , 
it will evolve further as more classes are developed for the framework, and as more users are using it.  

MOOSE is NOT meant to be a one-man show, it is meant to evolve within a growing community around the framework.  

Within the community, key users will support, document, explain and even create new classes for the framework.
It is the ambition to grow this framework as a de-facto standard for mission designers to use within the DCS World community.
  
  
## MOOSE Loading

Moose.lua is the include file to be used within your DCS World missions, containing all the MOOSE code.
There are two ways how you can load your missions. Dynamically or Statically.


### Static Loading

See the folder **Moose_Include_Static**

**Moose Static Loading** is what the "normal" mission designer uses.  
Simply put, you would include all the code of MOOSE by including **just one Moose.lua file**.  
So by executing a DO SCRIPT FILE within your mission, you would load the complete MOOSE code within your mission.
This process is very useful **when you are using a stable Release** of Moose which don't change often, 
because it is really easy to set up for the mission designer.  
It also allows him to **release missions** which are contained in their entirety in the .miz file.  
But in a context in wich Moose changes often, static loading would require the generation of a new Moose.lua 
**for every change within the MOOSE framework** and you would need to replace the old Moose.lua in the .miz file you are using to test the changes. 
Add to this cumbersome process the fact that the Mission Editor doesn't like changes to the .miz file while it is open, 
which means you would need to close and reopen the Mission Editor for every change, 
and this process becomes unworkable for both the tester and the contributor.

### Dynamic Loading

See the folder **Moose_Include_Dynamic**

So, beyond the Static Loading, there is the Dynamic Loading, which allows a much more smooth proces while testing your missions.

Enter **Moose Dynamic loading**. In this process, the **Moose.lua** you insert in your .miz file **looks for every .lua** 
which constitute Moose in `DCSWorld\Scripts`, **and asks DCS to load them** during the mission startup.  
This way, the latest changes to the MOOSE .lua files in `DCSWorld\Scripts` are automatically taken into account when you restart the mission, 
no need to fiddle around with the .miz file or to close the mission editor!
Now, there is still a problem left : you wouldn't want to have to copy the MOOSE .lua files from your local repository to `DCSWorld\Scripts`, 
everytime you retrieve a new version of Moose. The solution to this problem is a dynamic link!  
Simply put, it makes sure that the folder `DCSWorld\Scripts\Moose` is always in sync with your local MOOSE repository on your disk.  
That way, **everytime you want to update to the next Moose, you simply sync your local repository** with the remote with GitHub, **and restart your mission** !
Note that if you want to **release your missions to end users**, you will need to make it **use the static loading process**. There is a tool to automate this task, read below.
  
  
  
## MOOSE Main Site

[Click on this link to browse to the MOOSE main web page.](http://flightcontrol-master.github.io/MOOSE_DOCS)
Documentation on the MOOSE class hierarchy, usage guides and background information can be found here for normal users, beta testers and contributors.
  
  
  
## MOOSE Missions

MOOSE comes with [demonstration missions](https://github.com/FlightControl-Master/MOOSE_MISSIONS) that you can use to understand the mechanisms how to use the classes within MOOSE.
  
  
  
## MOOSE Youtube Channel

MOOSE has a [broadcast and training channel on YouTube](https://www.youtube.com/channel/UCjrA9j5LQoWsG4SpS8i79Qg) with various channels that you can watch.
  
  
  
## MOOSE on [Discord](https://discord.gg/yBPfxC6)

MOOSE has a living (chat and video) community of users, beta testers and contributors. The gathering point is a service provided by discord.com. If you want to join this community, just click Discord and you'll be on board in no time.
  
  
  
## Please Donate ...

If you appreciate this development, please support to extend the framework. The development of this framework takes a lot of time.
A small gift would help me to buy a new small laptop that I can use to extend this framework while commuting to and from work ...
Also, your donations will be saved and spent wisely to the advantage of the community! 

If everyone helps with a small amount, it would be really great!

<a class="dbox-donation-button" href="https://donorbox.org/fund-github-subscriptionfor-moose" style="background:#2d81c5 url(https://d1iczxrky3cnb2.cloudfront.net/red_logo.png) no-repeat 37px center; color: #fff;text-decoration: none;font-family: Verdana,sans-serif;display: inline-block;font-size: 16px;padding: 15px 38px 15px 75px; -webkit-border-radius: 2px; -moz-border-radius: 2px; border-radius: 2px; box-shadow: 0 1px 0 0 #1f5a89; text-shadow: 0 1px rgba(0, 0, 0, 0.3);" >Donate</a>

kind regards,
FC
  
  
