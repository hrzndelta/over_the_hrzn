# Over the horizon
## About
This repo contains all my experimentations on building a multipurpose home servers running on 2 or more hardware. you could this repo as a template but don't just run things blindly, this repo is specificly made with my set of hardwares after all. This repo is also made so that my friends and family could audit stuff. Keeping me from being flagged as SUS and further reinforced my reputations as open source advocates amongs my friends :v

## Project structure
Planned

## Topology
Planned

## Roles
- The main server:
  This machine handles everything (except some that i'll be covering). But... currently, the current hardware only accomodates for game servers. There are a bunch of services i want to run once i get my hands the hardwares. I want to run something like a NAS services like samba and Nextcloud, AI chatbot using llama.cpp with both Q4_0 gguf and TurboQuant applied to the LLM, Gitea instance to reduce my reliance on GitHub, and many more. The hardware is not that weak but weak nonetheless. Some features that I'd like to see is not present on these systems because its consumer grade after all. Its a Z170 motherboard paired with i5-6600k, but heres the catch, it runs DDR3l. Since its during DRAM price crysis, I'm planning on using DDR4 based old prebuilt systems like ThinkCentre before. but after dealing with countless problematic sellers, I see DDR3 is the only way. So here we are (P.S: The DRAM price has going down NOT 1 week after my purchases. but since its my country, the sellers still putting high prices on stuff but slowly decreases, like, veerry sloooww)
- The gateway server:
  As the name suggests, this server handles the routing and authentications across all servers connected through it. this server runs both forward and reverse proxy, OAuth2 identity provider, bot challenge, and password manager (in case the main server is on maintenance, it'll keep running, i know this is stupid while running it on the gateway server) (also its a print server too). I choose using forward proxy setup instead of VPN because of performance and simplicity. i have friends that want to host their servers but dont have a public ip for them to use, so my idea is to route it to this server and have all their local ip routed to the internet. since i want to open the same corresponding ports, this isnt exacly a problem for a proxy setup. VPN requires both the server and the client to configure the network. but for proxy, setup once on server and it can be connected to apps and device that supports it (which is more than VPN).
- The IPMI server:
  This ones using my friend's old Raspberry Pi 3B since all the alternatives were out of reach, be it because of price or stock, and its essentially all the supported PiKVM configurations except the V1 DIY. Then coupled with a cheap 2-client KVM switch with the switch wired to the PiKVM via GPIO, its a perfect setup for managing both servers (I guess).
- The guest server:
  I've mentioned about routing my friends servers through mine before right?. Its quite simple actually, just route the entire traffic through proxy and then i just open ports that minecraft server uses and route everything web related through my reverse proxy.

## The future
In the future, I want to expand the servers even more. Like a third machine as a offsite backup and also the third node for high-availability. 

## Source
I have sourced my knowledges from these:
- [Wolfgang's Ansible Home Server](https://youtube.com/playlist?list=PLkxWXio1KmRoZd88WbrnSnQM5MJY5PjH2&si=gGDjhritgSGY_K5V)
- []()
- And alot more from search engines and DeepSeek
