https://github.com/perilouswithadollarsign/cstrike15_src/blob/master/engine/baseserver.cpp

Info: 

I made a discord server for a support n help https://discord.gg/8VQNx5wM7f

If anyone is interested to fix it, I released the source code (I dont take credit for it) of CS:GO fake server redirect extensions for everyone.  To stop "business opportunity"   to make money from  server owners who are willing to pay to get their server spoofed as well  duo spammed server browser because it has went out of control. It needs gamedata update for sure its from 2021 + some fixes to properly show fake players on the internet tab.  

Please submit PR I will update repo btw would be nice if someone added windows support as well :)

## Note By Gamemann
This forked repository's goal is to fix outdated gamedata that requires reverse engineering knowledge to update. I am not an expert in reverse engineering, but it is an area I've been very interested in and I do have experience with. Therefore, I'm hoping to use this project as a way to dig deeper into it. 

With that said, sadly, CS:GO/CS2's community server browser is in a bad state and filled with many thousands of spoofed redirect servers. Valve, unfortunately, hasn't done anything to combat these issues for years (the last [meaningful server browser update in CS:GO](https://blog.counter-strike.net/index.php/2014/12/11079/) that I remember was from 2014). I plan to address these issues to Valve due to the Source 2 launch and create my own open-source server browser (Best Servers) that combats against spoofing of any kind (including A2S_INFO caching).

In the meantime, I'd rather exploits/spoofing software/tools be made public so that there aren't only a handful of communities/companies utilizing them and Valve can see exactly how they're doing it.

### Signatures Updated
* `CBaseServer::UpdateMasterServer` - **NT**
* `Update CBaseServer::ProcessConnectionlessPacket` - **NT**
* `NET_SendPacket` - **NT**
* `CheckConnectionLessRateLimits` - **NT**
* `CNetChan::ProcessPacket` - **NT**
* `CNetChan::ProcessPacketHeader` - **NT**
* `CNetChan::ProcessMessages` - **NT**
* `CSteam3Server::SendUpdatedServerDetails` - **NT**
* `CBaseServer::RejectConnection` - **NT**

**T** - Tested  
**NT** - Not Tested

### Signatures Needing Updated
* `CBaseServer::GetNumFakeClients`
* `CBaseServer::GetNumHumanPlayers`
* `CBaseServer::GetMasterServerPlayerCounts`
* `CBaseServer::GetNumClients`
* `CBaseServer::ForwardPacketsFromMasterServerUpdater`
* `CBaseServer::GetNumPlayers`
* `CBaseServer::GetNumProxies`
* `CBaseServer::FillServerInfo`
* `GetIP`
* `GetPort`
* `GetIPHostByteOrder`
* `NET_ProcessSocket`
* `NET_DiscardStaleSplitpackets`
* `NET_GetLoopPacket`
* `NET_ReceiveDatagram`
* `NET_LagPacket`