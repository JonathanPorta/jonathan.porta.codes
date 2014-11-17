---
layout: post
title:  "Minecraft Server Mangement with Ansible"
date:   2014-11-14 21:44:25
categories: minecraft ansible
permalink: /2014/11/14/minecraft-server-management-with-ansible
comments: true
---
Anyone who has had the privilege to setup and manage their own Minecraft server knows that it is kind of a pain in the ass. Sure, there is a large community that has grown up around the open source server versions, Bukkit and Spigot, but there are surprisingly few guides that focus on settings things up right and planning for maintaining the system in the future. Overall, I get the sense that most feel that "it's just a game, so don't take it seriously" Well, I've always been of the opinion that anything worth doing is worth doing right. I haven't always followed this MO, but I've learned the reality that doing something right is time saved in the future. I've seen this to be true with regard to leaky plumbing, proof-of-concept or hacked-together software, and thrown-together Minecraft servers.

After spending the last six months at a PaaS, I've observed server management scaled to handle very large volumes of traffic. I've gone from thinking of a servers as friends, to thinking of servers as cattle. So, naturally, when I sat down to spend an evening setting up a new Minecraft server, I wanted to do it right.

### Configuration and Provisioning Management
I have taken a liking to Ansible recently, and I have been using it in most of my personal projects. At work, we don't use Ansible, and that was part of the motivation to pick it up. I wanted to get some exposure outside of my day job.

### Minecraft + Ansible = Love
The playbook that I ended up writing is pretty straightforward. It isn't complete yet, but it goes most of the way of setting up a Spigot + Bungee Minecraft server. Currently it handles installing Spigot and Bungee. It uses systemd to manage the processes themselves, creating service files for each. This will ensure that the services are restarted if they fail, and consolidates all logging to journald. No more screwing around with dead screen instances!

There are some obviously missing components, like backup and user management. I am hoping that as I have need I will stay motivated to update my playbook to handle those situations as well.

### Check it out!
If you'd like to check it out, hit up the [repository][1] on my GitHub account.

[1]: https://github.com/JonathanPorta/ansible-minecraft
